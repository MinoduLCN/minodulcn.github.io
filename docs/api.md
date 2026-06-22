# Backend API documentation

When running the project in **development mode**, the full Swagger/OpenAPI documentation is available interactively at:

```
http://localhost:3000/api-docs
```

This interactive documentation allows you to:
- Explore all available endpoints
- View detailed request/response schemas
- Test API endpoints directly from your browser
- Understand the complete API structure

> **Note:** The Swagger UI is only available when the application is running in development environment (`NODE_ENV=development`).

---

## Authentication

Most API endpoints are protected and require a Bearer token for authentication. The token can be obtained by using the `signin` or `signup` endpoints.

- **Security Scheme**: `bearer` (JWT)
- **Format**: `Authorization: Bearer <your-jwt-token>`

---

## API Reference

### Auth
Endpoints for user authentication and account management.

#### POST `/v1/auth/signin`
Login to your account.

**Request Body:**
```json
{
  "phone": "string (required) - User phone number",
  "password": "string (required) - User password"
}
```

**Response:** `201 Created` - Authentication successful.

---

#### POST `/v1/auth/signup`
Create a new account.

**Request Body:**
```json
{
  "fullName": "string (required) - User full name",
  "phone": "string (required) - User phone number",
  "gender": "string (required) - User gender",
  "password": "string (required) - User password"
}
```

**Response:** `201 Created` - Account created successfully.

---

#### GET `/v1/auth/logout`
Logout from the current session.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Logout successful.

---

### User
Endpoints for managing users and retrieving user information.

#### GET `/v1/users`
List all users.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all users.

---

#### POST `/v1/users`
Create a new user.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "fullName": "string (required) - User full name",
  "phone": "string (required) - User phone number",
  "gender": "string (required) - User gender",
  "password": "string (required) - User password",
  "isContactPerson": "string (required) - Is the user the community contact person?"
}
```

**Response:** `201 Created` - User created successfully.

---

#### PATCH `/v1/users`
Update the current user's data.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "fullName": "string (required) - User full name",
  "gender": "string (required) - User gender (Male, Female, Other)",
  "phone": "string (required) - User phone number",
  "isContactPerson": "string (required) - Is the user the community contact person?"
}
```

**Response:** `200 OK` - User updated successfully.

---

#### GET `/v1/users/dashboard`
Get the admin dashboard data.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns admin dashboard statistics.

---

#### GET `/v1/users/current`
Get details of the current authenticated user.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns current user details.

---

#### GET `/v1/users/{id}`
Get information for a specific user.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (number, required) - User ID

**Response:** `200 OK` - Returns user information.

---

#### PATCH `/v1/users/{id}`
Update data for a specific user.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (number, required) - User ID

**Request Body:**
```json
{
  "fullName": "string (required) - User full name",
  "gender": "string (required) - User gender (Male, Female, Other)",
  "phone": "string (required) - User phone number",
  "isContactPerson": "string (required) - Is the user the community contact person?"
}
```

**Response:** `200 OK` - User updated successfully.

---

#### GET `/v1/users/contact-person`
Get contact person information.

**Authentication:** Required (Bearer Token)

**Query Parameters:**
- `id` (number, required) - User ID

**Response:** `200 OK` - Returns contact person information.

---

#### PUT `/v1/users/password`
Modify the current user's password.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "password": "string (required) - New user password"
}
```

**Response:** `200 OK` - Password updated successfully.

---

### Role
Endpoints for managing roles.

#### GET `/v1/roles`
List all roles.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all roles.

---

#### GET `/v1/roles/{id}`
Get information for a specific role.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Role ID

**Response:** `200 OK` - Returns role information.

---

### Product Management

#### Products

##### GET `/v1/products`
List all products.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all products.

---

##### POST `/v1/products`
Create a new product.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the product |
| `description` | string | Yes | Description of the product |
| `price` | number | Yes | Price of the product |
| `sales_unit` | string | Yes | Product sales unit (e.g., kg, piece, liter) |
| `categoryId` | number | Yes | Product category ID |
| `image` | file (binary) | Yes | Image file to upload |

**Response:** `201 Created` - Product created successfully.

---

##### GET `/v1/products/{id}`
Get information for a specific product.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Product ID

**Response:** `200 OK` - Returns product information.

---

##### PATCH `/v1/products/{id}`
Update a specific product.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Product ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the product |
| `description` | string | Yes | Description of the product |
| `price` | number | Yes | Price of the product |
| `sales_unit` | string | Yes | Product sales unit |
| `categoryId` | number | Yes | Product category ID |
| `image` | file (binary) | No | Image file to upload |

**Response:** `200 OK` - Product updated successfully.

---

##### DELETE `/v1/products/{id}`
Delete a specific product.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Product ID

**Response:** `200 OK` - Product deleted successfully.

---

#### Product Categories

##### GET `/v1/product-categories`
List all product categories.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all product categories.

---

##### POST `/v1/product-categories`
Create a new product category.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the category |
| `image` | file (binary) | No | Image file to upload |

**Response:** `201 Created` - Category created successfully.

---

##### GET `/v1/product-categories/{id}`
Get information for a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Response:** `200 OK` - Returns category information.

---

##### PATCH `/v1/product-categories/{id}`
Update a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the product category |
| `image` | file (binary) | No | Image file to upload |

**Response:** `200 OK` - Category updated successfully.

---

##### DELETE `/v1/product-categories/{id}`
Delete a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Response:** `200 OK` - Category deleted successfully.

---

### Product Offers & Demands

#### Product Offers

##### GET `/v1/product-offers`
List all product offers.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all product offers.

---

##### POST `/v1/product-offers`
Create a new product offer.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "productId": "number (required) - Product ID",
  "farmerId": "number (required) - Farmer ID",
  "quantity": "number (required) - Quantity available"
}
```

**Response:** `201 Created` - Product offer created successfully.

---

##### GET `/v1/product-offers/archived`
List all archived product offers.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of archived product offers.

---

##### GET `/v1/product-offers/farmer/{id}`
List product offers filtered by farmer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Farmer ID

**Response:** `200 OK` - Returns filtered product offers.

---

##### GET `/v1/product-offers/product/{id}`
List product offers filtered by product.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Product ID

**Response:** `200 OK` - Returns filtered product offers.

---

##### GET `/v1/product-offers/{id}`
Get information for a specific offer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Offer ID

**Response:** `200 OK` - Returns offer information.

---

##### PATCH `/v1/product-offers/{id}`
Update a specific product offer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Offer ID

**Request Body:**
```json
{
  "productId": "number (optional) - Product ID",
  "farmerId": "number (optional) - Farmer ID",
  "quantity": "number (optional) - Quantity available"
}
```

**Response:** `200 OK` - Offer updated successfully.

---

##### DELETE `/v1/product-offers/{id}`
Delete a specific product offer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Offer ID

**Response:** `200 OK` - Offer deleted successfully.

---

##### PUT `/v1/product-offers/archive/{id}`
Archive a specific product offer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Offer ID

**Response:** `200 OK` - Offer archived successfully.

---

##### PUT `/v1/product-offers/unarchive/{id}`
Unarchive a specific product offer.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Offer ID

**Response:** `200 OK` - Offer unarchived successfully.

---

#### Product Demands

##### GET `/v1/product-demands`
List all product demands.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all product demands.

---

##### POST `/v1/product-demands`
Create a new product demand.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "productId": "number (required) - Product ID",
  "partnerId": "number (required) - Partner ID",
  "quantity": "number (required) - Quantity demanded",
  "deadline": "string (required) - Deadline date (ISO format)"
}
```

**Response:** `201 Created` - Product demand created successfully.

---

##### GET `/v1/product-demands/archived`
List all archived product demands.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of archived product demands.

---

##### GET `/v1/product-demands/partner/{id}`
List demands filtered by partner.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Partner ID

**Response:** `200 OK` - Returns filtered product demands.

---

##### GET `/v1/product-demands/product/{id}`
List demands filtered by product.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Product ID

**Response:** `200 OK` - Returns filtered product demands.

---

##### GET `/v1/product-demands/{id}`
Get information for a specific demand.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Demand ID

**Response:** `200 OK` - Returns demand information.

---

##### PATCH `/v1/product-demands/{id}`
Update a specific product demand.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Demand ID

**Request Body:**
```json
{
  "productId": "number (optional) - Product ID",
  "partnerId": "number (optional) - Partner ID",
  "quantity": "number (optional) - Quantity demanded",
  "deadline": "string (optional) - Deadline date (ISO format)"
}
```

**Response:** `200 OK` - Demand updated successfully.

---

##### DELETE `/v1/product-demands/{id}`
Delete a specific product demand.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Demand ID

**Response:** `200 OK` - Demand deleted successfully.

---

##### PUT `/v1/product-demands/{id}/archive`
Archive a specific product demand.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Demand ID

**Response:** `200 OK` - Demand archived successfully.

---

##### PUT `/v1/product-demands/{id}/unarchive`
Unarchive a specific product demand.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Demand ID

**Response:** `200 OK` - Demand unarchived successfully.

---

### Post Management

#### Posts

##### GET `/v1/posts`
List all posts.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all posts.

---

##### POST `/v1/posts`
Create a new post.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `idCategory` | number | Yes | Post category ID |
| `author` | string | Yes | Post author |
| `title` | string | Yes | Post title |
| `description` | string | Yes | Post description |
| `image` | file (binary) | No | Post image |
| `attachment` | file (binary) | Yes | Post attachment file |
| `attachmentKb` | file (binary) | Yes | Post attachment in Kabye language |
| `attachmentPdf` | file (binary) | Yes | Post attachment in PDF format |
| `tags` | string | Yes | Post tags list (comma-separated or array) |
| `resources` | string | No | Post resources list (comma-separated or array) |

**Response:** `201 Created` - Post created successfully.

---

##### GET `/v1/posts/resource/{id}`
List posts filtered by a specific resource.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Resource ID

**Response:** `200 OK` - Returns filtered posts.

---

##### GET `/v1/posts/tag/{id}`
List posts filtered by a specific tag.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Tag ID

**Response:** `200 OK` - Returns filtered posts.

---

##### GET `/v1/posts/{id}`
Get information for a specific post.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Post ID

**Response:** `200 OK` - Returns post information.

---

##### PATCH `/v1/posts/{id}`
Update a specific post.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Post ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `idCategory` | number | Yes | Post category ID |
| `author` | string | Yes | Post author |
| `title` | string | Yes | Post title |
| `description` | string | Yes | Post description |
| `image` | file (binary) | No | Post image |
| `attachment` | file (binary) | No | Post attachment file |
| `attachmentKb` | file (binary) | No | Post attachment in Kabye language |
| `attachmentPdf` | file (binary) | No | Post attachment in PDF format |
| `tags` | string | Yes | Post tags list |
| `resources` | string | No | Post resources list |

**Response:** `200 OK` - Post updated successfully.

---

##### DELETE `/v1/posts/{id}`
Delete a specific post.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Post ID

**Response:** `200 OK` - Post deleted successfully.

---

#### Post Categories

##### GET `/v1/post-categories`
List all post categories.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all post categories.

---

##### POST `/v1/post-categories`
Create a new post category.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the category |
| `nameKb` | string | Yes | Name of the category in Kabye |
| `image` | file (binary) | No | Image file to upload |

**Response:** `201 Created` - Category created successfully.

---

##### GET `/v1/post-categories/{id}`
Get information for a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Response:** `200 OK` - Returns category information.

---

##### PATCH `/v1/post-categories/{id}`
Update a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the category |
| `nameKb` | string | Yes | Name of the category in Kabye |
| `image` | file (binary) | No | Image file to upload |

**Response:** `200 OK` - Category updated successfully.

---

##### DELETE `/v1/post-categories/{id}`
Delete a specific category.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Category ID

**Response:** `200 OK` - Category deleted successfully.

---

#### Post Tags

##### GET `/v1/tags`
List all tags.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all tags.

---

##### POST `/v1/tags`
Create a new tag.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | No | Name of the tag |
| `image` | file (binary) | Yes | Image file to upload |

**Response:** `201 Created` - Tag created successfully.

---

##### GET `/v1/tags/{id}`
Get information for a specific tag.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Tag ID

**Response:** `200 OK` - Returns tag information.

---

##### PATCH `/v1/tags/{id}`
Update a specific tag.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Tag ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the tag |
| `image` | file (binary) | No | Image file to upload |

**Response:** `200 OK` - Tag updated successfully.

---

##### DELETE `/v1/tags/{id}`
Delete a specific tag.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Tag ID

**Response:** `200 OK` - Tag deleted successfully.

---

#### Post Resources

##### GET `/v1/resource`
List all resources.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all resources.

---

##### POST `/v1/resource`
Create a new resource.

**Authentication:** Required (Bearer Token)

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the resource |
| `image` | file (binary) | Yes | Image file to upload |

**Response:** `201 Created` - Resource created successfully.

---

##### GET `/v1/resource/{id}`
Get information for a specific resource.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Resource ID

**Response:** `200 OK` - Returns resource information.

---

##### PATCH `/v1/resource/{id}`
Update a specific resource.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Resource ID

**Content-Type:** `multipart/form-data`

**Request Body:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `name` | string | Yes | Name of the resource |
| `image` | file (binary) | No | Image file to upload |

**Response:** `200 OK` - Resource updated successfully.

---

##### DELETE `/v1/resource/{id}`
Delete a specific resource.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Resource ID

**Response:** `200 OK` - Resource deleted successfully.

---

### Configuration

#### GET `/v1/config`
Get the current configuration.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns current community configuration.

---

#### PATCH `/v1/config`
Update the default configuration.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "name": "string (optional) - Community name",
  "intro": "string (optional) - Community introduction",
  "adresse": "string (optional) - Community address",
  "location": "string (optional) - Community location",
  "whatsappLink": "string (optional) - Advice center WhatsApp link",
  "stationLink": "string (optional) - Teleagriculture station link"
}
```

**Response:** `200 OK` - Configuration updated successfully.

---

### Weather

#### GET `/v1/weather`
List weather data.

**Query Parameters:**
- `limit` (number, required) - Number of records to retrieve

**Authentication:** Not required

**Response:** `200 OK` - Returns list of weather data.

---

#### POST `/v1/weather`
Sync weather from the teleagriculture station.

**Authentication:** Not required

**Request Body:**
```json
{
  "temp": "number (optional) - Main temperature in °C (example: 22)",
  "temp1": "number (optional) - Secondary temperature in °C (example: 21.8)",
  "hum": "number (optional) - Main humidity percentage (example: 45)",
  "hum1": "number (optional) - Secondary humidity percentage (example: 47.2)",
  "press": "number (optional) - Atmospheric pressure in hPa (example: 1013.25)",
  "lux": "number (optional) - Luminosity in lux (example: 320.5)",
  "ambient": "number (optional) - Ambient light sensor raw value (example: 215)",
  "CO": "number (optional) - Carbon monoxide concentration in ppm (example: 0.5)",
  "NO2": "number (optional) - Nitrogen dioxide concentration in ppb (example: 12)",
  "wind_dir": "number (optional) - Wind direction in degrees (example: 180)",
  "wind_spd": "number (optional) - Wind speed in m/s (example: 5.2)",
  "uv": "number (optional) - UV index (example: 6)",
  "battery": "number (optional) - Battery level in % (example: 85)",
  "time": "string (optional) - Time of the measurement (ISO format)"
}
```

**Response:** `201 Created` - Weather data synced successfully.

---

#### GET `/v1/weather/current`
Get the current weather details.

**Authentication:** Not required

**Response:** `200 OK` - Returns current weather information.

---

#### GET `/v1/weather/download`
Download weather data as a spreadsheet.

**Authentication:** Not required

**Response:** `200 OK` - Returns weather data in spreadsheet format (file download).

---

### Partners

#### GET `/v1/partners`
List all partners.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all partners.

---

#### POST `/v1/partners`
Create a new partner.

**Authentication:** Required (Bearer Token)

**Request Body:**
```json
{
  "name": "string (required) - Partner's name",
  "adresse": "string (required) - Partner's address (city, village, etc.)",
  "phone": "string (required) - Partner's phone number"
}
```

**Response:** `201 Created` - Partner created successfully.

---

#### GET `/v1/partners/{id}`
Get information for a specific partner.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Partner ID

**Response:** `200 OK` - Returns partner information.

---

#### PATCH `/v1/partners/{id}`
Update a specific partner.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Partner ID

**Request Body:**
```json
{
  "name": "string (optional) - Partner's name",
  "adresse": "string (optional) - Partner's address (city, village, etc.)",
  "phone": "string (optional) - Partner's phone number"
}
```

**Response:** `200 OK` - Partner updated successfully.

---

#### DELETE `/v1/partners/{id}`
Delete a specific partner.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Partner ID

**Response:** `200 OK` - Partner deleted successfully.

---

### Utilities

#### Backup

##### GET `/backup/create`
Create a system backup (files & database dump).

**Authentication:** Not required

**Response:** `200 OK` - Backup created successfully.

---

#### Nginx Logs

##### GET `/v1/nginx-logs`
Read raw Nginx log files.

**Authentication:** Required (Bearer Token)

**Query Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `lines` | number | No | Number of lines to retrieve (default: 500) |
| `type` | string | No | Type of log to read: `access`, `error`, or `default` |

**Response:** `200 OK` - Returns the requested Nginx logs.

---

##### DELETE `/v1/nginx-logs`
Empty all log files.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - All log files emptied successfully.

---

#### Forum

##### GET `/v1/forum`
List all forum entries.

**Authentication:** Required (Bearer Token)

**Response:** `200 OK` - Returns list of all forum entries.

---

##### DELETE `/v1/forum/{id}`
Remove a specific forum entry.

**Authentication:** Required (Bearer Token)

**Path Parameters:**
- `id` (string, required) - Forum entry ID

**Response:** `200 OK` - Forum entry removed successfully.
