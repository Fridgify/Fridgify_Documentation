# Notification Services

This document is going to provide you with an overview of the notification services implemented in **Fridgify**.

## Base System

**Fridgify's** native notification system uses *Firebase Cloud Messaging*, a service provided by Google's Firebase. As the backend implements all the notification logic, the client is only required to do a few tasks. First of all, for notifications to work, the backend needs a client token, which is aquired by Firebase. <br>
Client apps have to therefore request a *client token* from *Firebase*. Look into the *Firebase* documentation to learn more about it. Here is some example code for Kotlin, which uses the *Firebase* package.
```kotlin
FirebaseInstanceId.getInstance()
    .instanceId
    .addOnCompleteListener(OnCompleteListener { task ->
        if (!task.isSuccessful) {
            return@OnCompleteListener
        }

        // Get new Instance ID token
        val token = task.result?.token
    })
```
After acquiring a client token, the client application has to make a request to the backend, to register this token. 
```
POST /messaging/register
Headers:
  Authorization: [API-Token]
Body:
  {
      "client_token": [Firebase Token]
  }
```
Doing this registers a user for notifications. <br/>

**Future Plans**<br/>
In future use cases, clients should be able to unregister. Therefore the backend should provide an endpoint to unregister any tokens, which were previously registered.

## Hopper Notifications

If users are interested in using the **Hopper** service, they first of all have to subscribe. Make the following call to retrieve a subscription link.
```
GET /messaging/subscribe?service=2
Headers:
  Authorization: [API-Token]
Required: service parameter [1 - Fridgify, 2 - Hopper]
```
You will retrieve a body, which could look like the following:
```json
{
    "subscribe_url": "https://example.com"
}
```
Users have to open up the subscription url and follow the process. After completing the subscription the user will be redirected to a deep link, which could look like the following:
```
https://api-dev.fridgify.com/?user_id=6&status=success&id=5ed7d0fa04fd3cde8f3f6b57
```
Extract the *id* parameter and use this to register the messaging service in **Fridgify**.
```
POST /messaging/register
Headers:
  Authorization: [API-Token]
Body:
  {
      "client_token": [hopper id (token)],
      "service": 2
  }
```
Hint: I mean **service** as in -> Dienst. Instead of sevice as in food. :+1:
If this is done successfully, users are able to receive notifications in **Hopper**.

## Types of Notifications

### Daily Update - Soon To Be Expired Items

Every day at (currently) 8:00 AM a job is executed, which notifies every user, who is registered for notifications, about soon to be expired items. Currently the range is 3 days, meaning every item, which is about to expire in 3 days, is considered in the notification. 

## Useful Links

* [Firebase](https://firebase.google.com/)
* [Firebase - Cloud Messaging](https://firebase.google.com/docs/cloud-messaging)
* [Hopper Documentation](https://developer.hoppercloud.net/#/)
