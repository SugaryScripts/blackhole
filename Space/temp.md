Sure! To accommodate categories and optional subcategories for products, you can adjust the schema as follows:

### Updated Database Schema

#### 1. **Categories Table**
| Column Name   | Data Type    | Description                          |
|---------------|--------------|--------------------------------------|
| category_id   | INT (PK)     | Unique identifier for the category    |
| name          | VARCHAR(100) | Category name                        |
| parent_id     | INT (FK)     | Identifier for the parent category (nullable for top-level categories) |

### Revised **Products Table**
| Column Name   | Data Type    | Description                          |
|---------------|--------------|--------------------------------------|
| product_id    | INT (PK)     | Unique identifier for the product    |
| name          | VARCHAR(100) | Product name                         |
| description   | TEXT         | Product description                  |
| price         | DECIMAL(10,2)| Product price                        |
| stock_quantity| INT          | Quantity available in stock          |
| created_at    | TIMESTAMP    | Product creation timestamp           |
| updated_at    | TIMESTAMP    | Last update timestamp                |
| user_id       | INT (FK)     | Identifier for the seller (user_id) |
| category_id   | INT (FK)     | Associated main category (foreign key) |
| subcategory_id | INT (FK, NULL)| Associated subcategory (foreign key, nullable) |

### Updated **ProductCategories Table**
This table is no longer needed since categories and subcategories can be directly linked in the **Products** table.

### Relationships
- **Categories** can have a hierarchical structure where a category can have multiple subcategories (self-referential relationship using `parent_id`).
- Each **Product** can be associated with one main **Category** and an optional **Subcategory**.

### Example Usage
1. **Top-Level Category** (e.g., "Electronics"):
   - `category_id = 1`, `name = "Electronics"`, `parent_id = NULL`
  
2. **Subcategory** (e.g., "Mobile Phones"):
   - `category_id = 2`, `name = "Mobile Phones"`, `parent_id = 1`

3. **Product** (e.g., "iPhone 13"):
   - `product_id = 1`, `name = "iPhone 13"`, `category_id = 1`, `subcategory_id = 2`

### Summary
This design allows for flexibility in categorizing products, enabling them to belong to both a main category and an optional subcategory. You can add more levels if needed by extending the `parent_id` approach. Adjust any field types or sizes as necessary based on your specific application needs!