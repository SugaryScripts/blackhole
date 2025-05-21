Free hosting for prototype laravel
[9 Best Free Laravel Hosting Provider In 2024 \[Free And Paid\]](https://googiehost.com/blog/best-free-laravel-hosting/)

- users
	- create user
	- table
		- choose / create new user with current id
		- delete
- staff
	- create staff
	- table
		- choose / create new user with current id
		- delete
- dashboard
	- logged in
		- user: email / password --- username
		- staff: name / profile image



### Redesigned Schema Overview:

1. **`product_types` Table**: Defines product types (e.g., Frame, Lens, Softlens, Misc).
2. **`products` Table**: Contains core product information and links to product types.
3. **`product_type_attributes` Table**: Contains attributes specific to each product type.
4. **`product_variants` Table**: Handles the variations in products (e.g., different sizes, colors).
5. **`variant_attributes` Table**: Defines what attributes exist for each product variant.
6. **`product_inventory` Table**: Manages inventory and pricing.
7. **`product_images` Table**: Stores images for each product and variant.

---

### 1. **`product_types` Table**

This table will store the different types of products such as Frame, Lens, Softlens, and Misc.

|Column Name|Data Type|Description|
|---|---|---|
|product_type_id|INT|Primary Key, Unique ID for product type|
|name|VARCHAR(255)|Name of the product type (e.g., "Frame", "Lens")|
|description|TEXT|Description of the product type|
|created_at|DATETIME|Timestamp when the product type was created|

#### Example Data:

|product_type_id|name|description|created_at|
|---|---|---|---|
|1|Frame|Eyewear frames with customizable sizes|2024-11-26 10:00:00|
|2|Lens|Optical lenses with various powers|2024-11-26 10:05:00|
|3|Softlens|Contact lenses for vision correction|2024-11-26 10:10:00|
|4|Misc|Miscellaneous accessories and products|2024-11-26 10:15:00|

---

### 2. **`products` Table**

This table stores the core details about each product, including the product type.

|Column Name|Data Type|Description|
|---|---|---|
|product_id|INT|Primary Key, Unique ID for each product|
|name|VARCHAR(255)|Name of the product|
|product_type_id|INT|Foreign Key referencing the `product_types` table|
|description|TEXT|Detailed description of the product|
|price|DECIMAL(10,2)|Price of the product|
|created_at|DATETIME|Timestamp when the product was added|
|updated_at|DATETIME|Timestamp when the product was last updated|

#### Example Data:

|product_id|name|product_type_id|description|price|created_at|
|---|---|---|---|---|---|
|1|Ray-Ban Aviator|1|Classic aviator sunglasses|120.00|2024-11-26 10:00:00|
|2|Acuvue Oasys|2|Monthly soft lenses with UV protection|70.00|2024-11-26 10:05:00|
|3|Oakley Batwolf|1|Durable frame for sports use|150.00|2024-11-26 10:10:00|

---

### 3. **`product_type_attributes` Table**

This table defines the attributes that are specific to each product type (e.g., Frame, Lens, Softlens).

|Column Name|Data Type|Description|
|---|---|---|
|product_type_attr_id|INT|Primary Key, Unique ID for product type attribute|
|product_type_id|INT|Foreign Key referencing the `product_types` table|
|name|VARCHAR(255)|Name of the attribute (e.g., "Color", "Power")|
|data_type|VARCHAR(50)|Type of data (e.g., "String", "Number", "Boolean")|
|required|BOOLEAN|Whether the attribute is required for the product|
|created_at|DATETIME|Timestamp when the attribute was created|

#### Example Data:

|product_type_attr_id|product_type_id|name|data_type|required|created_at|
|---|---|---|---|---|---|
|1|1|Color|String|TRUE|2024-11-26 10:20:00|
|2|1|Material|String|TRUE|2024-11-26 10:25:00|
|3|2|Power|Number|TRUE|2024-11-26 10:30:00|
|4|2|UV Protection|Boolean|FALSE|2024-11-26 10:35:00|
|5|3|Power|Number|TRUE|2024-11-26 10:40:00|
|6|4|Type|String|FALSE|2024-11-26 10:45:00|

---

### 4. **`product_variants` Table**

This table stores the different variants available for each product (e.g., different colors, sizes, etc.). Variants allow for variations in attributes like size, material, etc.

|Column Name|Data Type|Description|
|---|---|---|
|variant_id|INT|Primary Key, Unique ID for the product variant|
|product_id|INT|Foreign Key referencing the `products` table|
|variant_name|VARCHAR(255)|Name/description of the variant (e.g., "Red", "Large")|
|sku|VARCHAR(255)|SKU (stock-keeping unit) for the variant|
|price|DECIMAL(10,2)|Price for this variant (can differ from base product)|
|stock_quantity|INT|Stock quantity for this specific variant|
|created_at|DATETIME|Timestamp when the variant was created|

#### Example Data:

|variant_id|product_id|variant_name|sku|price|stock_quantity|created_at|
|---|---|---|---|---|---|---|
|1|1|Red|RB-123-RED|120.00|50|2024-11-26 10:00:00|
|2|1|Blue|RB-123-BLU|125.00|30|2024-11-26 10:05:00|
|3|2|-4.00|ACUVUE-4|70.00|100|2024-11-26 10:10:00|

---

### 5. **`variant_attributes` Table**

This table defines the attributes for each product variant (e.g., the "Material" of a frame or the "Power" of a lens). Each variant can have its own specific attributes.

|Column Name|Data Type|Description|
|---|---|---|
|variant_attr_id|INT|Primary Key, Unique ID for the variant attribute|
|variant_id|INT|Foreign Key referencing the `product_variants` table|
|product_type_attr_id|INT|Foreign Key referencing the `product_type_attributes` table|
|value|VARCHAR(255)|Value for the variant's attribute (e.g., "Metal", "-4.00")|
|created_at|DATETIME|Timestamp when the attribute value was created|

#### Example Data:

|variant_attr_id|variant_id|product_type_attr_id|value|created_at|
|---|---|---|---|---|
|1|1|1|Red|2024-11-26 10:00:00|
|2|1|2|Metal|2024-11-26 10:05:00|
|3|2|1|Blue|2024-11-26 10:10:00|
|4|2|2|Plastic|2024-11-26 10:15:00|

---

### 6. **`product_inventory` Table**

This table manages stock and pricing for each product or variant. You can track quantity and pricing for both the base product and variants.

| Column Name    | Data Type     | Description                                                     |
| -------------- | ------------- | --------------------------------------------------------------- |
| inventory_id   | INT           | Primary Key, Unique ID for inventory record                     |
| product_id     | INT           | Foreign Key referencing the `products` table                    |
| variant_id     | INT           | Foreign Key referencing the `product_variants` table (nullable) |
| stock_quantity | INT           | Number of units in stock                                        |
| price          | DECIMAL(10,2) | Price for this inventory record                                 |
| created_at     | DATETIME      | Timestamp when the inventory record was created                 |

---

### 7. **`product_images` Table**

This table stores images for each product or variant.

| Column Name | Data Type    | Description                                                     |
| ----------- | ------------ | --------------------------------------------------------------- |
| image_id    | INT          | Primary Key, Unique ID for the image record                     |
| product_id  | INT          | Foreign Key referencing the `products` table                    |
| variant_id  | INT          | Foreign Key referencing the `product_variants` table (nullable) |
| image_url   | VARCHAR(255) | URL of the product image                                        |
| created_at  | DATETIME     | Timestamp when the image was uploaded                           |
