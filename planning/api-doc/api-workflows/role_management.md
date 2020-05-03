# Fridge Roles

This document is going to explain the role system of Fridgify, as well as how to manage said roles.

## Fridge Roles

| Role Name | Add Item | Remove Item | Change Item Volume | Change Member Roles | Remove From Fridge | Edit Fridge Information | Delete Fridge |
| :- | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| **Fridge User** | ✓ | ✓ | ✓ | X | X | X | X |
| **Fridge Overseer** | ✓ | ✓ | ✓ | ✓ (1, 2) | ✓ (3) | X | X |
| **Fridge Owner** | ✓ | ✓ | ✓ | ✓ (1) | ✓ | ✓ | ✓ |

(1) You cannot change the role of your own user. <br/>
(2) You cannot change the role of a Fridge Owner. <br/>
(3) Only **Fridge Users**

Each fridge has only one **Fridge Owner**. The **Fridge Owner** is the creator of the fridge. <br/>
**Fridge Overseers** can be declared by the **Fridge Owner** or by other **Fridge Overseers**.

## Endpoints

### PATCH /fridge/management/\<fridge-id>/users/\<user-id>

Calling this *REST*-Endpoint allows a user to change a role of a different fridge member. Only **Fridge Owners** and **Fridge Overseers** are allowed to access this endpoint. If a **Fridge User** accesses this endpoint, the endpoint returns a **403 Forbidden** response.

You need a valid API-Token as you need for nearly every request. The body should contain the role.

Example: <br/>
User A (**Fridge Owner** of Fridge 1) wants to change User B (id: 10) to a **Fridge Overseer**. He performs a PATCH request against */fridge/management/1/users/10*. The body could have the following form:

Body 1 [Role as a String]: <br/>
```json
{
    "role": "Fridge Overseer"
}
```

Body 2 [Role as an Integer]: <br/>
```json
{
    "role": 1
}
```

If the change of the role was successful, the request responds with a **200 OK**.

Currently we have the following mappings for roles:

Fridge Owner - 0 <br/>
Fridge Overseer - 1 <br/>
Fridge User - 2 <br/>

### DELETE /fridge/management/\<fridge-id>/users/\<user-id>

Calling this *REST*-Endpoint allows a user to remove a different user from his fridge. It is important to keep in mind, that **Fridge Overseers** are only allowed to remove **Fridge Users**. If they try to remove other **Fridge Overseers** or the **Fridge Owner**. **403 Forbidden** should be expected as a response.

### GET /fridge/management/\<fridge-id>/users/

Calling this *REST*-Endpoint allows a user to show every member of the fridge, with their role, if he is part of the fridge.

Example Response:
```json
[
    {
        "user": {
            "username": "testUser",
            "name": "Test",
            "surname": "User",
            "email": "test@user.de",
            "birth_date": "2000-10-17"
        },
        "role": "Fridge Owner"
    },
    {
        "user": {
            "username": "dummy_name",
            "name": "Dummy",
            "surname": "Name",
            "email": "dummy@d.de",
            "birth_date": "2000-10-17"
        },
        "role": "Fridge Overseer"
    }
]
```