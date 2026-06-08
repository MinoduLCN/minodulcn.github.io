---
layout: page
title: Backoffice
---

## Minodu – Administrator Backoffice Documentation
{:.no_toc}

|---|---|
| **Version** | 1.0 |
| **Date** | May 2026 |
| **Language** | English |
| **Audience** | MINODU system administrators |

## Content
{:.no_toc}
* TOC
{:toc}

---

## Authentification – Login
The login page is the single entry point to the MINODU backoffice. Only users with the **ADMIN** role and an **ACTIVATED** account can access the platform.

### 1.1 Features
- Authentication using phone/username and password
- Show/hide password using the eye icon
- Session management via tokens (JWT)
- Custom error messages depending on the failure type
- Protection against unauthorized access

### 1.2 Screenshots
![Login_page](../assets/images/backoffice_loginpage.png)
Login page – full form

---

## Home – Dashboard

The first page displayed after login. It provides a statistical overview of the MINODU community with key indicators updated dynamically in real time.

### 2.1 Features
- Display of the community name
- Publications counter
- Products counter
- Registered members counter
- Last login timestamp
- Logout button with confirmation modal
- Real-time data updates

### 2.2 Sections
#### Section 1 – Header with logout
{:.no_toc}

|---|---|
| **Title** | Welcome message with the admin name |
| **Action** | “Logout” button → opens confirmation modal |

#### Section 2 – Statistics cards
{:.no_toc}

| Card | Description |
|---|---|
| **Card 1** | Community name |
| **Card 2** | Total number of publications |
| **Card 3** | Total number of products |
| **Card 4** | Total number of registered members |

#### Section 3 – Marketplace presentation
{:.no_toc}
Descriptive section of the platform with a general description and information about the MINODU marketplace.

#### Section 4 – Logout confirmation modal
{:.no_toc}
Confirmation popup before logout. Buttons: **Confirm / Cancel**.

#### Section 5 – Recent publications list
{:.no_toc}

Displays recent publications from the community.

### 2.3 Screenshots

| Description | Screenshot |
| ---- | ---- |
| Complete dashboard | ![dashboard](../assets/images/backoffice_dashboard.png) |
| Logout confirmation modal | ![logout](../assets/images/backoffice_logout-confirmation.png) |

---

## Publications
Module for managing the MINODU community’s editorial content. This module is divided into four subsections: publication list, categories, tags, and the detailed view of a publication.

### 3.1 Publication List

**Full CRUD – publications with media and attachments**

Displays and manages all community publications. The administrator has access to all CRUD operations as well as advanced search and filtering tools.

#### Features
{:.no_toc}

- **Read:** paginated publications table
- **Create:** add via dedicated modal
- **Update:** edit all properties
- **Delete:** with confirmation modal
- **Search:** filter by title, author, category, and tags
- **Uploads:** images, French/Kabyè audio, PDF, resources

#### Sections
{:.no_toc}

**Section 1 – Title bar and actions**

|---|---|
| **Title** | “Publications” |
| **Action** | “Add” button |

**Section 2 – Filters and search**

|---|---|
| **Search** | Text field – filter by title, author, category, and tags |

**Section 3 – Publications table**

|---|---|
| **Column 1** | Publication title |
| **Column 2** | Category |
| **Column 3** | Author |
| **Column 4** | Actions: Edit \| Delete |
| **Navigation** | Pagination between pages |

**Section 4 – Add/Edit modal**

|---|---|
| **Field 1** | Author (required) |
| **Field 2** | Title (required) |
| **Field 3** | Description (long text) |
| **Field 4** | Category (selector) |
| **Upload 1** | Main image (PNG/JPEG) |
| **Field 5** | Tags (multiple selection) |
| **Upload 2** | French audio |
| **Upload 3** | Kabyè audio |
| **Upload 4** | PDF file |
| **Actions** | Save \| Cancel |

**Section 5 – Delete modal**  
Confirmation before permanent deletion. Buttons: **Confirm / Cancel**.

#### Feedback messages
{:.no_toc}
- “Publication added successfully!”
- “Publication updated successfully!”
- “Publication deleted successfully!”

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| ---- | ---- |
| Publications – full table with pagination | ![publications](../assets/images/backoffice_publications.png) |
| Publications – Add/Edit modal | ![publications_modal](../assets/images/backoffice_publications_modal.png) |
| Publications – delete confirmation modal | ![publicatons_delete](../assets/images/backoffice_publications_delete.png) |

### 3.2 Publication Categories
**CRUD – bilingual French/Kabyè support**  
Management of categories that organize publications. Each category has a name in two languages (French and Kabyè) and can be illustrated with an image.

#### Features
{:.no_toc}

- **Read:** list of all categories
- **Create:** new category with image
- **Update:** edit name (FR/Kabyè) and image
- **Delete:** with confirmation
- **Bilingual support:** French and Kabyè fields required

#### Sections
{:.no_toc}

**Section 1 – Header**

|---|---|
| **Title** | “Categories” |
| **Action** | “Add” button |

**Section 2 – Categories table**

|---|---|
| **Column 1** | Name in French |
| **Column 2** | Name in Kabyè |
| **Column 3** | Actions: Edit \| Delete |

**Section 3 – Add/Edit modal**

| **Field 1** | Name in French (required) |
| **Field 2** | Name in Kabyè (required) |
| **Upload** | PNG/JPEG image + preview |
| **Actions** | Save \| Cancel |

#### Feedback messages
{:.no_toc}
- “Category added successfully!”
- “Category updated successfully!”
- “Category deleted successfully!”

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| ---- | ---- |
| Publication Categories – table | ![categories_table](../assets/images/backoffice_categories_table.png) |
| Publication Categories – Add/Edit | ![categories_add-edit](../assets/images/backoffice_categories_add-edit.png) |

### 3.3 Publication Tags
**CRUD – labels with avatars**  
Tags are labels associated with publications to improve organization and search. Each tag can have an illustrative image/avatar.

#### Features
{:.no_toc}

- **Read:** table with avatars
- **Create:** add with image
- **Update:** edit name and image
- **Delete:** with confirmation
- **Avatars:** each tag can have an illustration

#### Sections
{:.no_toc}

**Section 1 – Header and actions**

| --- | --- |
| **Title** | “Tags” |
| **Action** | “Add” button |

**Section 2 – Tags table**

|---|---|
| **Column 1** | Avatar (tag image) |
| **Column 2** | Tag name |
| **Column 3** | Actions: Edit \| Delete |

**Section 3 – Add/Edit modal**

|---|---|
| **Field 1** | Tag name (required) |
| **Upload** | PNG/JPEG image/avatar + preview |
| **Actions** | Save \| Cancel |

#### Feedback messages
{:.no_toc}
- “Tag added successfully!”
- “Tag updated successfully!”
- “Tag deleted successfully!”

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Publication tags – table | ![tags_table](../assets/images/backoffice_tags_table.png) |
| Publication Tags – Add/Edit modal | ![tags_add-edit](../assets/images/backoffice_tags_add-edit.png) |

### 3.4 Publication Details
**Detailed view – full consultation and editing**  
Page for in-depth consultation and editing of a single publication, accessible from the list through the “View” button. All properties and media are displayed and editable.

#### Features
{:.no_toc}
- **Consultation:** display all details
- **Update:** edit title, description, category, tags, images, and attachments
- **Navigation:** breadcrumb (Publications > Details)
- **Author:** complete author information
- **Upload:** change images and attachments

#### Sections
{:.no_toc}

**Section 1 – Header with navigation**

|---|---|
| **Breadcrumb** | Publications → Details |
| **Info** | Author name and information |

**Section 2 – General information**

|---|---|
| **Title** | Full publication title |
| **Description** | Full text |
| **Category** | Assigned category |

**Section 3 – Media and attachments**

|---|---|
| **Image** | Main publication image |
| **Tags** | List of associated tags |
| **Audio** | Audio files (FR and Kabyè) |
| **PDF** | Attached PDF documents |

**Section 4 – Action buttons**

|---|---|
| **Action 1** | Edit publication |
| **Action 2** | Return to list |

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Publication Details – full view (information + media) | ![publication_details](../assets/images/backoffice_publication-details.png) |

---

## Products
Module for managing the MINODU platform’s product catalog. It includes management of products themselves and their categories.

### 4.1 Product List
**Full CRUD – product catalog with images**  
Displays and manages the complete product catalog. The administrator can add, edit, and delete products, manage their properties (name, description, category, price, sales unit), and manage their images.

#### Features
{:.no_toc}

- **Read:** paginated table with all products
- **Create:** add via modal with image
- **Update:** edit all properties
- **Delete:** with confirmation
- **Images:** upload and manage PNG/JPEG files

#### Sections
{:.no_toc}

**Section1 – Header and actions**

|---|---|
| **Title** | “Products” |
| **Action** | “Add” button |

**Section 2 – Products table**

|---|---|
| **Column 1** | Product image |
| **Column 2** | Product name |
| **Column 3** | Category |
| **Column 4** | Price |
| **Column 5** | Actions: Edit \| Delete |

**Section 3 – Add/Edit modal**

|---|---|
| **Field 1** | Product name (required) |
| **Field 2** | Description |
| **Field 3** | Category (selector) |
| **Field 4** | Price (decimal value) |
| **Field 5** | Sales unit |
| **Upload** | PNG/JPEG image |
| **Actions** | Save \| Cancel |

#### Feedback messages
{:.no_toc}
- “Product added successfully!”
- “Product updated successfully!”
- “Product deleted successfully!”

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Products – full table | ![products_table](../assets/images/backoffice_products_table.png) |
| Products – Add/Edit modal | ![products_add-edit](../assets/images/backoffice_products_add-edit.png) |

### 4.2 Product Categories

**CRUD – categories with illustrative images**  
Management of categories that organize products (e.g., vegetables, fruits, grains, etc.). Each category can be illustrated with an image.

#### Features
{:.no_toc}
- **Read:** list of all categories
- **Create:** add with image
- **Update:** edit name and image
- **Delete:** with confirmation
- **Images:** PNG/JPEG support

#### Sections
{:.no_toc}

**Section 1 – Header**

|---|---|
| **Title** | “Categories” |
| **Action** | “Add a category” button |

**Section 2 – Categories table**

|---|---|
| **Column 1** | Illustration image |
| **Column 2** | Category name |
| **Column 3** | Actions: Edit \| Delete |

**Section 3 – Add/Edit modal**

|---|---|
| **Field** | Category name (required) |
| **Upload** | PNG/JPEG image + preview |
| **Actions** | Save \| Cancel |

#### Feedback messages
{:.no_toc}
- “Product category added!”
- “Product category updated!”
- “Product category deleted!”

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Product Categories – table | ![product_cat_table](../assets/images/backoffice_product_cat_table.png) |
| Product Categories – Add/Edit modal | ![product_cat_add-edit](../assets/images/backoffice_product_cat_add-edit.png) |

---

## Marketplace
Module for managing the MINODU marketplace. It brings together product offers published by producers/companies and product requests submitted by customers.

### 5.1 Product Offers
**Supply marketplace – published availability**  
Management of product offers: the availability that producers and companies highlight on the platform.

#### Features
{:.no_toc}
- **Read:** table of available offers
- **Create:** add a new offer
- **Update:** edit offer details
- **Delete:** remove an offer

#### Sections
{:.no_toc}

**Section 1 – Header**

|---|---|
| **Title** | “Product availability” |
| **Action** | “Add” button |

**Section 2 – Offers table**

|---|---|
| **Column 1** | Product |
| **Column 2** | Available quantity |
| **Column 3** | Producer price |
| **Navigation** | Pagination |

**Section 3 – Add/Edit modal**

|---|---|
| **Field 1** | Product selection |
| **Field 2** | Available quantity |
| **Field 3** | Producer |
| **Actions** | Save \| Cancel |

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Product Offers – full table | ![product_offers_table](../assets/images/backoffice_product_offers_table.png) |
| Product Offers – Add/Edit modal | ![product_offers_add-edit](../assets/images/backoffice_product_offers_add-edit.png) |

### 5.2 Product Requests
**Demand marketplace – customer needs**  
Management of product requests: needs expressed by customers looking for products on the MINODU platform.

#### Features
{:.no_toc}
- **Read:** table of received requests
- **Status:** track request status
- **Details:** see who requests what and when
- **Tracking:** archive or process requests

#### Sections
{:.no_toc}

**Section 1 – Header**

|---|---|
| **Title** | “Product Requests” |

**Section 2 – Requests table**

|---|---|
| **Column 1** | Requested product |
| **Column 2** | Requested quantity |
| **Column 3** | Partner |
| **Column 4** | Deadline date |
| **Column 5** | Actions: Edit \| Archive \| Delete |
| **Navigation** | Pagination |

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Product Requests – full table | ![prodcuct_requests_table](../assets/images/backoffice_product-requests_table.png) |
| Product Requests – Add/Edit modal | ![prodcuct_requests_add-edit](../assets/images/backoffice_product-requests_add-edit.png) |

---

## Users
Management of all users registered on the MINODU platform. Allows administrators to consult profiles and manage roles, statuses, and permissions.

#### Features
{:.no_toc}
- **Read:** paginated list
- **Actions:** edit

#### Sections
{:.no_toc}

**Section 1 – Header**

|---|---|
| **Title** | “Users” |

**Section 2 – Users table**

|---|---|
| **Column 1** | Name |
| **Column 2** | Phone |
| **Column 3** | Role |
| **Column 4** | Contact person |
| **Column 5** | Actions: Edit |
| **Navigation** | Pagination |

#### Screenshots
{:.no_toc}

| Description | Screenshot |
| --- | --- |
| Users – table | ![users_table](../assets/images/backoffice_users_table.png) |
| Users – Add/Edit modal | ![users_add-edit](../assets/images/backoffice_users_add-edit.png) |

---

## Partners