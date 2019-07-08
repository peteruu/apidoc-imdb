--- 

title: Swagger Petstore 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

This is a sample server Petstore server.  You can find out more about     Swagger at [http://swagger.io](http://swagger.io) or on [irc.freenode.net, #swagger](http://swagger.io/irc/).      For this sample, you can use the api key `special-key` to test the authorization     filters. 

**Version:** 1.0.0 

[Find out more about Swagger](http://swagger.io) 

# /PET
## ***PUT*** 

**Summary:** Update an existing pet

### HTTP Request 
`***PUT*** /pet` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid ID supplied |
| 404 | Pet not found |
| 405 | Validation exception |

## ***POST*** 

**Summary:** Add a new pet to the store

### HTTP Request 
`***POST*** /pet` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 405 | Invalid input |

# /PET/FINDBYSTATUS
## ***GET*** 

**Summary:** Finds Pets by status

**Description:** Multiple status values can be provided with comma separated strings

### HTTP Request 
`***GET*** /pet/findByStatus` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| status | query | Status values that need to be considered for filter | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid status value |

# /PET/FINDBYTAGS
## ***GET*** 

**Summary:** Finds Pets by tags

**Description:** Muliple tags can be provided with comma separated strings. Use         tag1, tag2, tag3 for testing.

### HTTP Request 
`***GET*** /pet/findByTags` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| tags | query | Tags to filter by | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid tag value |

# /PET/{PETID}
## ***GET*** 

**Summary:** Find pet by ID

**Description:** Returns a single pet

### HTTP Request 
`***GET*** /pet/{petId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| petId | path | ID of pet to return | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid ID supplied |
| 404 | Pet not found |

## ***POST*** 

**Summary:** Updates a pet in the store with form data

### HTTP Request 
`***POST*** /pet/{petId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| petId | path | ID of pet that needs to be updated | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 405 | Invalid input |

## ***DELETE*** 

**Summary:** Deletes a pet

### HTTP Request 
`***DELETE*** /pet/{petId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| api_key | header |  | No |  |
| petId | path | Pet id to delete | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid ID supplied |
| 404 | Pet not found |

# /PET/{PETID}/UPLOADIMAGE
## ***POST*** 

**Summary:** uploads an image

### HTTP Request 
`***POST*** /pet/{petId}/uploadImage` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| petId | path | ID of pet to update | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |

# /STORE/INVENTORY
## ***GET*** 

**Summary:** Returns pet inventories by status

**Description:** Returns a map of status codes to quantities

### HTTP Request 
`***GET*** /store/inventory` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |

# /STORE/ORDER
## ***POST*** 

**Summary:** Place an order for a pet

### HTTP Request 
`***POST*** /store/order` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid Order |

# /STORE/ORDER/{ORDERID}
## ***GET*** 

**Summary:** Find purchase order by ID

**Description:** For valid response try integer IDs with value >= 1 and <= 10.         Other values will generated exceptions

### HTTP Request 
`***GET*** /store/order/{orderId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderId | path | ID of pet that needs to be fetched | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid ID supplied |
| 404 | Order not found |

## ***DELETE*** 

**Summary:** Delete purchase order by ID

**Description:** For valid response try integer IDs with positive integer value.         Negative or non-integer values will generate API errors

### HTTP Request 
`***DELETE*** /store/order/{orderId}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| orderId | path | ID of the order that needs to be deleted | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid ID supplied |
| 404 | Order not found |

# /USER
## ***POST*** 

**Summary:** Create user

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***POST*** /user` 

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

# /USER/CREATEWITHARRAY
## ***POST*** 

**Summary:** Creates list of users with given input array

### HTTP Request 
`***POST*** /user/createWithArray` 

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

# /USER/CREATEWITHLIST
## ***POST*** 

**Summary:** Creates list of users with given input array

### HTTP Request 
`***POST*** /user/createWithList` 

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

# /USER/LOGIN
## ***GET*** 

**Summary:** Logs user into the system

### HTTP Request 
`***GET*** /user/login` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | query | The user name for login | Yes |  |
| password | query | The password for login in clear text | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid username/password supplied |

# /USER/LOGOUT
## ***GET*** 

**Summary:** Logs out current logged in user session

### HTTP Request 
`***GET*** /user/logout` 

**Responses**

| Code | Description |
| ---- | ----------- |
| default | successful operation |

# /USER/{USERNAME}
## ***GET*** 

**Summary:** Get user by user name

### HTTP Request 
`***GET*** /user/{username}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | path | The name that needs to be fetched. Use user1 for testing.  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | successful operation |
| 400 | Invalid username supplied |
| 404 | User not found |

## ***PUT*** 

**Summary:** Updated user

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***PUT*** /user/{username}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | path | name that need to be updated | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid user supplied |
| 404 | User not found |

## ***DELETE*** 

**Summary:** Delete user

**Description:** This can only be done by the logged in user.

### HTTP Request 
`***DELETE*** /user/{username}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| username | path | The name that needs to be deleted | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 400 | Invalid username supplied |
| 404 | User not found |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
