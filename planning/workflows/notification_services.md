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

Still in need of implementation.

## Types of Notifications

### Daily Update - Soon To Be Expired Items

Every day at (currently) 8:00 AM a job is executed, which notifies every user, who is registered for notifications, about soon to be expired items. Currently the range is 3 days, meaning every item, which is about to expire in 3 days, is considered in the notification. 

## Useful Links

* [Firebase](https://firebase.google.com/)
* [Firebase - Cloud Messaging](https://firebase.google.com/docs/cloud-messaging)
* [Hopper Documentation](https://developer.hoppercloud.net/#/)