# My Essential API Case Study

## Use Cases

### Create a feed image

#### Primary course (happy path)

1. Recive one request of type **POST** on route **/v1/feed**
4. **Create** a feed with data provided
5. Return **204**, without data

#### Error course (sad path):

1. Return error **404** if API doesnt exist
3. Return error **400** if url dont will provided by client
4. Return error **500** if error to try create feed image


## Model Specs

### Feed Image

| Property      | Type                |
|---------------|---------------------|
| `id`          | `UUID`              |
| `description` | `String` (optional) |
| `location`    | `String` (optional) |
| `url`	        | `URL`               |


### Create a feed image comment

#### Primary course (happy path)

1. Recive one request of type **POST** on route **/v1/image/comments**
4. **Create** a feed comment with data provided
5. Return **204**, without data

#### Error course (sad path):

1. Return error **404** if API doesnt exist
3. Return error **400** if imageId, message dont will provided by client
4. Return error **500** if error to try create feed image


## Model Specs

### Feed Comments

| Property      | Type                    |
|---------------|-------------------------|
| `id`          | `UUID`                  |
| `imageId`     | `UUID`                  |
| `message`     | `String`                |
| `created_at`  | `Date` (ISO8601 String) |