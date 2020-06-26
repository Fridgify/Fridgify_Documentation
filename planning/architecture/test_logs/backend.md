```
Count rest items ... ok
Get recipients. Expecting dictionary of tokens ... ok
Create short link unsuccessfully. Expecting JSONDecodeError ... ok
Create short link successfully. Expecting expected link ... ok
Login with invalid token. Expecting 403 response ... ok
Login with valid token. Expecting token ... ok
Login with invalid credentials. Expecting a 403 response ... ok
Login with invalid request. Expecting a 400 response ... ok
Login with valid credentials. Expecting a token ... ok
Login with incorrect HTTP method. Expecting 405 response ... ok
Register with existing email. Expecting 409 response ... ok
Register with invalid body. Expecting a 400 response ... ok
Register with existing username. Expecting 409 response ... ok
Register with valid body. Expecting 201 response ... ok
Retrieve token with invalid method. Expecting 405 response ... ok
Retrieve token with valid token. Expecting token ... ok
Retrieve token with invalid token. Expecting 403 response ... ok
Add content with invalid token. Expecting 403 response ... ok
Add content with missing token. Expecting 401 response ... ok
Add content with no token. Expecting 401 response ... ok
Add content with valid token & body. Expecting 201 response ... /usr/local/lib/python3.7/site-packages/django/db/models/fields/__init__.py:1427: RuntimeWarning: DateTimeField FridgeContent.expiration_date received a naive datetime (2019-11-23 00:00:00) while time zone support is active.
RuntimeWarning)
ok
Add content with valid token/invalid body. Expecting 400 response ... ok
Add content with valid token/incomplete body. Expecting 400 response ... ok
Get content with no fridge access. Expecting 403 response ... ok
Get content with invalid token. Expecting 403 response ... ok
Get content with not token. Expecting 403 response ... ok
Get content with unauthorized user. Expecting 403 response ... ok
Get content with valid fridge, token. Expecting 200 response ... /usr/local/lib/python3.7/site-packages/django/db/models/fields/__init__.py:1369: RuntimeWarning: DateTimeField FridgeContent.expiration_date received a naive datetime (2019-12-12 00:00:00) while time zone support is active.
RuntimeWarning)
ok
Get multiple content with valid fridge, token. Expecting 200 response ... ok
Remove content with missing authorization. Expecting 401 response ... ok
Remove content with valid body. Expecting 200 response ... ok
Create a fridge, which already exists. Expecting 409 response ... ok
Create a fridge. Check for valid body. Expecting 201 response ... ok
Create a fridge with missing token. Expecting 403 response ... ok
Placeholder ... ok
Join fridge, already a member. Expecting 409 response ... ok
Join fridge with no existing token. Expecting 404 response ... ok
Join fridge, where token is expired. Expecting 410 response ... ok
Join fridge with no token. Expecting 400 response ... ok
Join fridge with valid token. Expecting 201 response ... ok
Placeholder ... ok
Generate code. Firebase Error. Expecting 500 response ... ok
Generate code successfully. Expecting 201 response ... ok
Generate code for non-existent fridge. Expecting 404 response ... ok
Generate code with incorrect token. Expecting 403 response ... ok
Generate code. Missing provider. Expecting 500 response ... ok
Change owner role as overseer. Expecting 403 response ... ok
Change role for self. Expecting 409 response ... ok
Change user to overseer as user. Expecting 200 response ... ok
Change overseer to user as owner. Expecting 200 response ... ok
Change role to unknown role. Expecting 406 response ... ok
List users successfully. Expecting 200 response ... ok
User A created only one fridge ... ok
User A created the expected fridge ... ok
User B created only one fridge ... ok
User B created the expected fridge ... ok
Get item w/ barcode. Expecting 200 response ... ok
Get item w/ barcode. Item does not exist. Expecting 404 response ... ok
Get item w/ barcode. Item ID is missing. Expecting 422 response ... ok
Get item w/ id. Item does not exist. Expecting 404 response ... ok
Get item w/ id successfully. Expecting 200 response ... ok
Get item w/ id. ID is missing. Expecting 422 response ... ok
Get items successfully. Expecting 200 response ... ok
Register for Fridgify service. Expecting 201 response ... /usr/local/lib/python3.7/site-packages/django/db/models/fields/__init__.py:1427: RuntimeWarning: DateTimeField Accesstokens.valid_till received a naive datetime (9999-12-31 23:59:59.999999) while time zone support is active.
RuntimeWarning)
ok
Register for Hopper service. Expecting 201 response ... ok
Subscribe to Fridgify. Expecting 200 response ... ok
Subscribe to Hopper. Expecting 200 response ... ok
Subscribe with no service given. Expecting 400 response ... ok
Subscribe with non-numeric service argument. Expecting 400 response ... ok
Placeholder ... ok
Name Stmts Miss Cover Missing
--------------------------------------------------------------------------------------------
fridgify_backend/__init__.py 0 0 100%
fridgify_backend/api_urls/__init__.py 0 0 100%
fridgify_backend/api_urls/authentication/__init__.py 0 0 100%
fridgify_backend/api_urls/fridge/__init__.py 0 0 100%
fridgify_backend/api_urls/fridge/content/__init__.py 0 0 100%
fridgify_backend/api_urls/fridge/management/__init__.py 0 0 100%
fridgify_backend/api_urls/items/__init__.py 0 0 100%
fridgify_backend/api_urls/messaging/__init__.py 0 0 100%
fridgify_backend/api_urls/stores/__init__.py 0 0 100%
fridgify_backend/api_urls/users/__init__.py 0 0 100%
fridgify_backend/models/backends/__init__.py 2 0 100%
fridgify_backend/models/backends/api_authentication.py 25 3 88% 40-43
fridgify_backend/models/backends/user_authentication.py 47 8 83% 47-49, 60-61, 83-86
fridgify_backend/utils/__init__.py 0 0 100%
fridgify_backend/utils/api_utils.py 15 0 100%
fridgify_backend/utils/const.py 16 16 0% 2-31
fridgify_backend/utils/decorators.py 89 26 71% 30, 54-66, 76, 84-93, 119
fridgify_backend/utils/dynamic_link.py 23 0 100%
fridgify_backend/utils/messaging/__init__.py 2 0 100%
fridgify_backend/utils/messaging/firebase/__init__.py 1 0 100%
fridgify_backend/utils/messaging/firebase/firebase.py 11 5 55% 15-26
fridgify_backend/utils/messaging/hopper/__init__.py 1 0 100%
fridgify_backend/utils/messaging/hopper/hopper.py 20 10 50% 21-32, 37-38
fridgify_backend/utils/messaging/message_content.py 28 0 100%
fridgify_backend/utils/messaging/message_handler.py 23 8 65% 17-24
fridgify_backend/utils/redirect_handler.py 13 8 38% 14-25
fridgify_backend/utils/token_utils.py 21 3 86% 32, 54-55
fridgify_backend/views/__init__.py 0 0 100%
fridgify_backend/views/authentication/__init__.py 0 0 100%
fridgify_backend/views/authentication/login.py 17 0 100%
fridgify_backend/views/authentication/register.py 39 6 85% 50-52, 70-73
fridgify_backend/views/authentication/token.py 14 0 100%
fridgify_backend/views/fridge/__init__.py 0 0 100%
fridgify_backend/views/fridge/content/__init__.py 0 0 100%
fridgify_backend/views/fridge/content/fridge_content.py 54 6 89% 156-158, 186-191
fridgify_backend/views/fridge/content/fridge_content_item.py 58 31 47% 92-96, 104-108, 119-133, 145-161
fridgify_backend/views/fridge/management/__init__.py 1 0 100%
fridgify_backend/views/fridge/management/create_fridge.py 41 7 83% 50-52, 65-66, 71-73
fridgify_backend/views/fridge/management/delete_fridge.py 19 7 63% 24-32
fridgify_backend/views/fridge/management/edit_fridge.py 27 18 33% 21-38
fridgify_backend/views/fridge/management/join_fridge.py 35 4 89% 92-95
fridgify_backend/views/fridge/management/qr_code.py 35 0 100%
fridgify_backend/views/fridge/management/users/__init__.py 2 0 100%
fridgify_backend/views/fridge/management/users/get_users.py 18 0 100%
fridgify_backend/views/fridge/management/users/management.py 55 10 82% 89-90, 98, 127-128, 139-148
fridgify_backend/views/items/__init__.py 0 0 100%
fridgify_backend/views/items/barcode.py 25 2 92% 50-51
fridgify_backend/views/items/items.py 16 0 100%
fridgify_backend/views/items/items_id.py 51 23 55% 67, 72-73, 78-99
fridgify_backend/views/messaging/__init__.py 0 0 100%
fridgify_backend/views/messaging/register.py 25 0 100%
fridgify_backend/views/messaging/subscribe.py 28 0 100%
fridgify_backend/views/redirect/__init__.py 1 0 100%
fridgify_backend/views/redirect/redirect.py 12 4 67% 25-29
fridgify_backend/views/stores/__init__.py 0 0 100%
fridgify_backend/views/users/__init__.py 0 0 100%
fridgify_backend/views/utils/__init__.py 3 0 100%
fridgify_backend/views/utils/error.py 8 1 88% 23
fridgify_backend/views/utils/ping.py 10 2 80% 25-26
fridgify_backend/views/utils/version.py 10 1 90% 25
--------------------------------------------------------------------------------------------
TOTAL 941 209 78%
----------------------------------------------------------------------
Ran 73 tests in 3.659s
OK
```