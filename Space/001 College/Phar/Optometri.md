### Pharma Predictions
| check | works            | tasks                                                                           | features                                 | 1-5 |
| ----- | ---------------- | ------------------------------------------------------------------------------- | ---------------------------------------- | --- |
|       | init **project** | - Database<br>- Front-end Scaffolding                                           |                                          | 3   |
|       | **App** Settings | - Company Detail                                                                | - Company Profile                        | 1   |
|       | Branch           | - Manage Branch                                                                 | - Company Branch                         | 1   |
|       | **Auth**         | - Role & Permission<br>- Login Logout Register<br>- Manage Staff/User           | - Manage User<br>- User Access<br>- Auth | 2   |
|       | **Profile**      | - User Detail<br>- Profile Picture                                              | - User Profile                           | 1   |
|       | **Membership**   | - CRUD Membership                                                               | - Manage Membership                      | 1   |
|       | **Promos**       |                                                                                 |                                          | 4   |
|       | **Discounts**    | - By product<br>- By category<br>- By sub-category<br>- By promo<br>- By member |                                          | 5   |
|       | **Products**     | - Category<br>- Sub-Category<br>- Brands                                        | - Manage Products                        | 4   |
|       | Inventory        | - Stocks                                                                        | - Gudang / Inventory<br>- Stock / qty    | 3   |
|       | Transaction      | - Transaction<br>- History                                                      | - Transaction<br>- History               | 5   |
|       | Dashboard        | - Profit / Loss                                                                 |                                          | 2   |
|       | cloud            |                                                                                 |                                          |     |
|       | local            | Tiap perubahan, gk bs update DB                                                 |                                          |     |
|       | security         |                                                                                 |                                          |     |
|       | laporan keuangan |                                                                                 |                                          |     |
|       |                  |                                                                                 |                                          |     |
1 = 1-2 day
2 = 1/2 week
3 = 1 week
4 = 1-2 week
5 = 2 week

i. Manajemen pelanggan toko
ii. Transaksi penjualan
iii. Rekam medis
iv. Laporan Keuangan dan Pajak
v. Stock Opname Barang
vi. Absensi pegawai

#### Database
- User
- Membership
- Staff
- Product
- Settings
- Medical_Records
	- 
- Medical_History
- Transactions
Example of store
[Optika Lunett | Clear Out Sale](https://optikalunett.com/collections/clearout-sale)



#### Web
- Company
- Staff - role
- Group of discounts
- Garages
	- name - address - telephone
	- List Item
- Vehicles
	- Name - type - brand - license number
- Branch
- Member
	- id - name - phone - email - ktp - gender - birth - address - exp_date - status
- Category
	- name - profit_sharing - color
	- Sub Categories
- Delivery Partner
	- name - profit_sharing - color
	- Sub Categories
- Item
	- Category - 
- Inventory

reporting - inventory - transaksi - membership

#### Android
- Absensi
	- Scan & check in/out
- Login

#### List Templates
- Able Light $9
	- [Light Able Admin & Dashboard Template by phoenixcoded | ThemeForest](https://themeforest.net/item/light-able-admin-dashboard-template/51628885)
	- [Preview](https://html.phoenixcoded.net/light-able/bootstrap/dashboard/index.html)
- Able Pro $17
	- [Able Pro Bootstrap Admin Dashboard Template Preview - ThemeForest](https://preview.themeforest.net/item/able-pro-bootstrap-admin-dashboard-template/full_screen_preview/50170229)
	- [Preview](https://preview.themeforest.net/item/able-pro-bootstrap-admin-dashboard-template/full_screen_preview/50170229)
	  Theme: Accent color picker
	  Add extra space on heading for background color (or image if u can of course)
	  Landing pages
	  pro and light are slightly different, i even can't noticed it yet
- Tailwise $22
	- [Tailwise - Tailwind CSS HTML, Vue, React, Laravel Admin Dashboard Kit + Figma Design File by Left4code](https://themeforest.net/item/tailwise-intuitive-tailwind-dashboard-kit/48659596)
	- [Preview](https://tailwise.vercel.app/)
	- Sleek & modern design
	- Theme: color palette, (note: background on auth or profile maybe)
- Digiboard $14
	- [Digiboard - Multipurpose Admin Dashboard Template HTML + VueJs + Reactjs +Nextjs + Nuxtjs + Laravel by Codebasket](https://themeforest.net/item/digiboard-multipurpose-admin-dashboard-template/47154328)
	- [Preview](https://digiboard-html.codebasket.xyz/index.html)
	- Theme -> primary color, background side/main page content
	- Boxy and minimalistic

 ### EPOS
 Features:
 - Staff
 - Users
 - Absent
 - Category
 - Brand
 - Frame
	 - bridge
	 - weight
	 - shape
 - Accessory
	 - name
 - Soft lens
	 - ?
 - Lens (Each prescription has different price)
	 - left right eye are can be different
	 - axis
	 - cylinder
	 - sphere
 - Cashier
	 - Choose Product
		 - Check stock
	 - Add detail lens
	 - Biodata 
	 - Add to cart
	 - Receipt DONE




Security
User (customer)  → pembelian (transaksi) ??
	customer can have account?
User & Staff
	User need activation first
	User always belongs to a staff
	Staff can be optionally have user
Frame
	stock keeping unit for tracking inventory
		is it on each item or each product type/name
		fill the kpu at her/his own => must matches with the real frame
	category & brand
	SKU for lens? soft lens? accessory?
Lens
	belongs to frame
	for medical record
	
tax -> per product, per transaction?
discount -> per product, category, brand, event, date, membership
Softlens
Aksesoris

Medical  record -> is it need to saved all history transaction (previous prescription || with product (brand, model, category)) OR just need newest latest prescription

FRAME
```php
$table->string('sku')->unique();  
$table->string('name');  
$table->string('description')->nullable();  
  
$table->decimal('price', 10, 2);  
$table->decimal('cost_price', 10, 2);  
  
$table->string('model')->nullable();  
$table->string('color')->nullable();  
$table->enum('gender', ['men', 'women', 'unisex', 'kids'])->nullable();  
$table->string('material')->nullable();  
  
$table->string('frame_shape')->nullable();  
$table->string('frame_size')->nullable();  
  
$table->integer('lens_width')->nullable();  
$table->integer('bridge_width')->nullable();  
$table->integer('temple_length')->nullable();  
$table->decimal('weight', 5, 2)->nullable();  
$table->integer('stock_quantity')->default(0);
```
LENS
```php
$table->string('lens_material')->nullable();  
$table->string('lens_color')->nullable();  
$table->string('lens_tech')->nullable();  
$table->boolean('uv_protection')->default(false);  
$table->boolean('polarized')->default(false);  
  
$table->enum('prescription_type', ['Single Vision', 'Bifocal', 'Progressive', 'Readers', 'Plano'])->nullable();  
$table->enum('visual_impairment', ['Myopia', 'Hyperopia', 'Astigmatism', 'Presbyopia', 'None'])->nullable();  
// SPH (sphere) power for left lens  
$table->decimal('left_sphere_power', 4, 2)->default(0);  
// SPH (sphere) power for right lens  
$table->decimal('right_sphere_power', 4, 2)->default(0);  
// CYL (cylinder) power for astigmatism (left)  
$table->decimal('left_cylinder_power', 4, 2)->default(0);  
// CYL (cylinder) power for astigmatism (right)  
$table->decimal('right_cylinder_power', 4, 2)->default(0);  
// Axis for astigmatism (left)  
$table->integer('left_axis')->default(0);  
// Axis for astigmatism (right)  
$table->integer('right_axis')->default(0);  
// Additional power for bifocals/progressives  
$table->decimal('add_power', 4, 2)->default(0);  
  
$table->enum('coating', [  
    'Anti-Reflective', 'Scratch-Resistant', 'Blue Light Blocking', 'UV Coating', 'None'  
])->default('None');  
// Optional tint level  
$table->enum('tint_level', [  
    'Light', 'Medium', 'Dark', 'None'  
])->default('None');
```


# Second Eval
Frame
