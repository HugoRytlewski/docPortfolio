# Introduction
Liste de toutes les routes ainsi que de leurs fonctionnalités

# Fixtures
Pour load les fixtures, faire :

```bash
php bin/console doctrine:fixtures:load
```

# API Reference

# CommunityController.php
## Get all communities

```http
  GET /api/community
  ```

| Parameter | Type     | Description                             |
| :-------- | :------- | :-------------------------------------- |
|  `page`   |   `int`  | **Optional**. Page number for pagination|

This endpoint retrieves all communities. 
If the page parameter is provided, it returns the corresponding page of communities.

## Create a community

```http
  POST /api/community/create
```

This endpoint creates a new community. Only an admin can create a community.

## Update a community

```http
  POST /api/community/update/{id}
  ```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id     ` | `string` | **Required**. Id of the community to update |

This endpoint updates a community. Only an admin or a core team member can update a community.

## Read a community

```http
  GET /api/community/read/{id}
  ```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| `id`      | `string` | **Required**. Id of the community to read |

This endpoint retrieves a community by its ID.

## Delete a community

```http
  DELETE /api/community/delete/{id}
```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `api_key` | `string` | **Required**. Id of the community to delete |

This endpoint deletes a community. Only an admin can delete a community.

## Get community statistics

```http
  POST /api/community/get-stats
  ```

This endpoint retrieves the statistics of a community.

## List community events

```http
  POST /api/community/listCommunityEvents
```

This endpoint retrieves all events of a community.

# EventController.php
## List all events

```http
  GET /api/event
```

|Parameter	|Type	|Description                              |
|-----------|-------|---------------------------------------- |
|page	    |int	|**Optional**. Page number for pagination.|

Lists all events. If the page parameter is provided, it paginates the results based on the page number.

## Create an event

```http
  POST /api/event/create
```

Allows the creation of a new event. Access is restricted to admins and core team members only.

## Update an event

```http
  POST /api/event/update/{id}
```

|Parameter	|Type	  |Description                             |
|-----------|---------|----------------------------------------|
|id	        |string	  |**Required**. ID of the event to update.|

Updates an event's details. Only accessible by admins.

## List validated events

```http
  GET /api/event/listValidate
```

|Parameter	|Type	|Description                              |          
|-----------|-------|-----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination.|

Lists all validated events. Supports pagination if the page parameter is provided.

## Get all events

```http
  GET /api/event/getAllEvents
```

Retrieves all events without pagination.

## Read event details

```http
  GET /api/event/read/{id}
```

|Parameter	|Type	   |Description                           |        
|-----------|----------|--------------------------------------|
|id	        |string    |**Required**. ID of the event to read.|

Fetches details of a specific event by its ID.

## Delete an event

```http
  DELETE /api/event/delete/{id}
```

|Parameter	|Type	|Description                             |   
|-----------|-------|----------------------------------------|
|id	        |string	|**Required**. ID of the event to delete.|

Deletes an event. Restricted to admins and core team members.

## Validate an event

```http
  PATCH /api/event/validate/{id}
```

|Parameter	|Type	|Description                               |     
|-----------|-------|------------------------------------------|
|id	        |string	|**Required**. ID of the event to validate.|

Validates an event, making it official. Only accessible by admins.

## List event participants

```http
  GET /api/event/readRegistration/{id}
```

|Parameter	|Type	|Description                                            |    
|-----------|-------|-------------------------------------------------------|
|id	        |string	|**Required**. ID of the event to list participants for.|

Lists all participants of a specific event. Access is restricted to admins and core team members.

# LocationController.php
## List Locations

```http
  GET /api/location
```

|Parameter	|Type	|Description                             |       
|-----------|-------|----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination|

Lists all locations. If a page parameter is provided, it returns a paginated list of locations. Unauthorized access is denied.

## Create Location

```http
POST /api/location/create
```

Creates a new location. This endpoint is restricted to users with admin privileges.

## Update Location

```http
  POST /api/location/update/{id}
```

|Parameter	|Type	|Description                               | 
|-----------|-------|------------------------------------------|
|id	        |string	|**Required**. Id of the location to update|

Updates the details of an existing location. This action is restricted to admins.

## Read Location Details

```http
  GET /api/location/read/{id}
```

|Parameter	|Type	|Description                             |   
|-----------|-------|----------------------------------------|
|id	        |string	|**Required**. Id of the location to read|

Fetches the details of a specific location by its ID. Unauthorized access is denied.

## Delete Location

```http
DELETE /api/location/delete/{id}
```

|Parameter	|Type	|Description                               | 
|-----------|-------|------------------------------------------|
|id	        |string	|**Required**. Id of the location to delete|

Deletes a location. This endpoint is restricted to admins.

# MeController.php
## Retrieve User Details

```http
  GET /me
```

Retrieves details of the currently authenticated user.

## Retrieve User's Community Details

```http
  GET /me/community
```

Retrieves details of the communities associated with the currently authenticated user.

## Retrieve User's Registrations

```http
  GET /me/registration
```

Retrieves details of the events registered by the currently authenticated user.

# ModalityController.php
## List Modalities

```http
  GET /api/modality
```

Retrieves a list of modalities.

# QuestionController.php
**FONCTIONS NON UTILISEES**
## List Questions

```http
  GET /api/question
```

|Parameter	|Type	|Description                              |  
|-----------|-------|-----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination.|

Retrieves a list of questions. If the page parameter is provided, it returns the corresponding page of questions.

## Create Question

```http
  POST /api/question/create
```

Creates a new question. This endpoint is restricted to users with admin privileges.

## Read Question

```http
  GET /api/question/read/{id}
```

|Parameter	|Type	|Description                              |
|-----------|-------|-----------------------------------------|
|id	        |string	|**Required**. ID of the question to read.|

Retrieves details of a specific question by its ID.

## Update Question

```http
  POST /api/question/update/{id}
```

|Parameter	|Type	|Description                                |    
|-----------|-------|-------------------------------------------|
|id	        |string	|**Required**. ID of the question to update.|

Updates the details of an existing question. This action is restricted to admins.

## Delete Question

```http
 DELETE /api/question/delete/{id}
```

|Parameter	|Type	|Description                                |    
|-----------|-------|-------------------------------------------|
|id	        |string	|**Required**. ID of the question to delete.|

Deletes a question. This endpoint is restricted to admins.

# RegistrationController.php
## List Registrations

```http
  GET /api/registration
```

|Parameter	|Type	|Description                              |  
|-----------|-------|-----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination.|

Retrieves a list of registrations. If the page parameter is provided, it returns the corresponding page of registrations.

## Create Registration

```http
  POST /api/registration/create
```

Creates a new registration. This endpoint requires authentication.

## Update Registration

```http
  POST /api/registration/update/{id}
```

|Parameter	|Type	|Description                                    |    
|-----------|-------|-----------------------------------------------|
|id	        |string	|**Required**. ID of the registration to update.|

Updates the details of an existing registration. This action is restricted to collaborators.

## Read Registration

```http
  GET /api/registration/read/{id}
```

|Parameter	|Type	|Description                                  |  
|-----------|-------|---------------------------------------------|
|id	        |string	|**Required**. ID of the registration to read.|

Retrieves details of a specific registration by its ID.

## Delete Registration

```http
  DELETE /api/registration/delete/{id}
```

|Parameter	|Type	|Description                                    |    
|-----------|-------|-----------------------------------------------|
|id	        |string	|**Required**. ID of the registration to delete.|

Deletes a registration. This action is restricted to unverified users.

## Present Registration

```http
  POST /api/registration/present/{id}
```

|Parameter	|Type	|Description                                             |   
|-----------|-------|--------------------------------------------------------|
|id	        |string	|**Required**. ID of the registration to mark as present.|

Marks a registration as present. This action is restricted to collaborators.

## Check Registration

```http
  GET /api/registration/is_register/{id}
```

|Parameter	|Type	|Description                                   | 
|-----------|-------|----------------------------------------------|
|id	        |string	|**Required**. ID of the registration to check.|

Checks if a user is registered for a specific event. This action is restricted to unverified users.

# AnswerController.php
## List Answers

```http
  GET /api/answer
```

|Parameter	|Type	|Description                              |  
|-----------|-------|-----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination.|

Retrieves a list of answers. If the page parameter is provided, it returns the corresponding page of answers.

## Create Answer

```http
  POST /api/answer/create
```

Creates a new answer. This endpoint requires authentication.

## Read Answer

```http
  GET /api/answer/read/{id}
```

|Parameter	|Type	|Description                            |    
|-----------|-------|---------------------------------------|
|id	        |string	|**Required**. ID of the answer to read.|

Retrieves details of a specific answer by its ID.

# SurveyAnswerController.php
## List Survey Answers

```http
  GET /api/survey-answer
```

|Parameter	|Type	|Description                              |  
|-----------|-------|-----------------------------------------|
|page	    |int	|**Optional**. Page number for pagination.|

Retrieves a list of survey answers. If the page parameter is provided, it returns the corresponding page of survey answers.

## Create Survey Answer

```http
  POST /api/survey-answer/create
```

Creates a new survey answer. This endpoint requires authentication.

## Read Survey Answer

```http
  GET /api/survey-answer/read/{id}
```

|Parameter	|Type	|Description                            |    
|-----------|-------|---------------------------------------|
|id	        |string	|**Required**. ID of the answer to read.|

Retrieves details of a specific survey answer by its ID.

## Delete Survey Answer

```http
  DELETE /api/survey-answer/delete/{id}
```

|Parameter	|Type	|Description                              |  
|-----------|-------|-----------------------------------------|
|id	        |string	|**Required**. ID of the answer to delete.|

Deletes a survey answer by its ID.

## Read Answer Survey

```http
  GET /api/survey-answer/readAnwserSurvey/{id}
```

|Parameter	|Type	|Description                                         |   
|-----------|-------|----------------------------------------------------|
|id	        |string	|**Required**. ID of the survey to read answers from.|

Retrieves answers to a specific survey by its ID.

## Add Answer to Question

```http
  POST /api/survey-answer/AddAnwserQuestion
```

Adds an answer to a question. This endpoint requires authentication.

## Export Survey Data

```http
  GET /api/survey-answer/export/{id}
```

|Parameter	|Type	|Description                                        |
|-----------|-------|---------------------------------------------------|
|id	        |string	|**Required**. ID of the survey to export data from.|

Exports survey data by its ID.

## Find Data by ID

```http
  GET /api/survey-answer/findData/{id}
```

|Parameter	|Type	|Description                      | 
|-----------|-------|---------------------------------|
|id	        |string	|**Required**. ID to find data by.|

Finds data by its ID.

# SurveyController.php
## Get all surveys

```http
  GET /api/survey
  ```

| Parameter | Type     | Description                             |
| :-------- | :------- | :-------------------------------------- |
|  `page`   |   `int`  | **Optional**. Page number for pagination|

This endpoint retrieves all surveys. 
If the page parameter is provided, it returns the corresponding page of surveys.

## Read a survey

```http
  GET /api/survey/read/{id}
  ```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| `id`      | `string` | **Required**. Id of the survey to read |

This endpoint retrieves a survey by its ID.

# TypeEventController.php
## Get all types of events

```http
  GET /api/type-event
  ```

| Parameter | Type     | Description                             |
| :-------- | :------- | :-------------------------------------- |
|  `page`   |   `int`  | **Optional**. Page number for pagination|

This endpoint retrieves all types of events. 
If the page parameter is provided, it returns the corresponding page of types of events.

## Create a type of event

```http
  POST /api/type-event/create
```

This endpoint creates a new type of event.

## Update a type of event

```http
  POST /api/type-event/update/{id}
  ```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id     ` | `string` | **Required**. Id of the type of event to update |

This endpoint updates a type of event.

## Read a type of event

```http
  GET /api/type-event/read/{id}
  ```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| `id`      | `string` | **Required**. Id of the type of event to read |

This endpoint retrieves a type of event by its ID.

## Delete a type of event

```http
  DELETE /api/type-event/delete/{id}
```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id`      | `string` | **Required**. Id of the type of event to delete |

This endpoint deletes a type of event.

# GuestController.php
## Get all guests

```http
  GET /api/guest
  ```

| Parameter | Type     | Description                             |
| :-------- | :------- | :-------------------------------------- |
|  `page`   |   `int`  | **Optional**. Page number for pagination|

This endpoint retrieves all guests. 
If the page parameter is provided, it returns the corresponding page of guests.

## Create a guest

```http
  POST /api/guest/create
```

This endpoint creates a new guest.

## Update a guest

```http
  POST /api/guest/update/{id}
  ```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id     ` | `string` | **Required**. Id of the guest to update     |

This endpoint updates a guest.

## Read a guest

```http
  GET /api/guest/read/{id}
  ```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| `id`      | `string` | **Required**. Id of the guest to read     |

This endpoint retrieves a guest by its ID.

## Delete a guest

```http
  DELETE /api/guest/delete/{id}
```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id`      | `string` | **Required**. Id of the guest to delete     |

This endpoint deletes a guest.

## Connect as a guest

```http
  POST /api/guest/connect-guest
```

This endpoint allows a guest to authenticate.

## Forgotten password

```http
  POST /api/guest/forgotten-password
```

This endpoint handles the request for forgotten password.

## Reset password

```http
  POST /api/guest/reset-password
```

This endpoint handles the request for resetting the password.

# UserController.php
## Get all users

```http
  GET /api/users
  ```

| Parameter | Type     | Description                             |
| :-------- | :------- | :-------------------------------------- |
|  `page`   |   `int`  | **Optional**. Page number for pagination|

This endpoint retrieves all users. 
If the page parameter is provided, it returns the corresponding page of users.

## Create a user

```http
  POST /api/users/create
```

This endpoint creates a new user.

## Update a user

```http
  POST /api/users/update/{id}
  ```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id     ` | `string` | **Required**. Id of the user to update      |

This endpoint updates a user.

## Set user community

```http
  POST /api/users/set-community/{id}
```

This endpoint associates a community with a user.

## Delete user community

```http
  DELETE /api/users/delete-community/{id}
```

This endpoint disassociates a community from a user.

## Update user role

```http
  POST /api/users/updateRole/{id}
  ```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id     ` | `string` | **Required**. Id of the user to update role |

This endpoint updates the role of a user.

## Read a user

```http
  GET /api/users/read/{id}
  ```

| Parameter | Type     | Description                               |
| :-------- | :------- | :---------------------------------------- |
| `id`      | `string` | **Required**. Id of the user to read      |

This endpoint retrieves a user by its ID.

## Delete a user

```http
  DELETE /api/users/delete/{id}
```

| Parameter | Type     | Description                                 |
| :-------- | :------- | :------------------------------------------ |
| `id`      | `string` | **Required**. Id of the user to delete      |

This endpoint deletes a user.

## Send email to users

```http
  GET /api/users/sendMail/{id}
  ```

| Parameter | Type     | Description                                |
| :-------- | :------- | :----------------------------------------- |
| `id`      | `string` | **Required**. Id of the event to send email|

This endpoint sends an email to users associated with a specific event.
