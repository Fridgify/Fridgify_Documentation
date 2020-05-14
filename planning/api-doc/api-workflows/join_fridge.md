# Workflow - Joining a fridge

This document is going to talk about the workflow of inviting and joining fridges. <br/>
In this document the target fridge is called **Fridge A**, the inviter is called **User A**, while the invitee is called **User B**.
<br/>

## Step 1: Invite People

To be able to join an existing fridge, **User B** needs an invitation. **User A** therefore has to create one inside the client app. <br/>

### Scenario A: Invite with QR-Code
Let's suppose **User A** wants to create a QR-Code, which shall be scanned by **User B**. To create a QR-Code the client app has to first make the following request:
```REST
GET /fridge/management/<fridge-id>/qr-code
```
This creates a dynamic link, which allows users to join a fridge. The response looks like the following:
```json
{
    "dynamic_link": "https://fridgify.page.link/abcdefghijk",
    "validation_time": 43200
}
```
Generally a dynamic link is valid for 12 hours, after that users are not able to join a fridge with it.<br/>
After retrieving the dynamic link, the client app creates a QR-Code, which contains the link.

### Scenario B: Invite with Link
Link invitations have the exact same workflow as invitations by QR-Code, except the client app is not required to generate a QR-Code.

## Step 2: Join Fridge

After **User A** created an invitation, **User B** opens up the QR-Code or link, which opens the browser. The link redirects him
1. to the app, where he can accept the invitation or
2. to the *Google Play Store*/*Apple Play Store*.

We are primarily going to talk about scenario 1, as after installing the app in scenario 2, the workflow should be the same. 

The mobile application handles the redirect, which contains a so called deep link. This deep link is used later on, when the user confirmed the invitation, as the deep link should be used for the request. This could look like the following:
```
GET /fridge/management/join?token=AJoinToken
```
Upon executing the request, the backend checks for the validity of the Join-Token and determines whether to add the user to the fridge or not. If the request was successful, the client should receive a response with status code **201**.