# Firebase - Notes

## General

Firebase is a messaging service. Requires a project for firebase. We could either use the SDK, looks like using this would require to use their database? Could use the official HTTP v1 API.

## Authentication

1. Get service account JSON file from Firebase Project
2. Set ENV Variable GOOGLE_APPLICATION_CREDENTIALS
3. Retrieve OAuth 2.0 Accesstoken (Authorize access to FCM, request scope https://www.googleapis.com/auth/firebase.messaging
4. Add retrieved token to headers
```python
headers = {
  'Authorization': 'Bearer' + token,
  'Content-Type': 'application/json; UTF-8',
}
```

## Send messages

Sending messages requires a registration token (comes from client). So we need an endpoint, where the client sends us his registration token for FCM.

Sending to multiple clients via multicast just requires a list of registration tokens (useful for stuff, up to 100).

Clients can 'subscribe' to topics. Send conditonally with topics to clients, which subscribed to that topic.

Sending batch of messages via list (up to 500).

Can also set specific configs for different devices.

## Useful links

https://firebase.google.com/docs/cloud-messaging/send-message?authuser=0 <br/>
https://firebase.google.com/docs/cloud-messaging/auth-server?authuser=0