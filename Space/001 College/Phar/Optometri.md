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
 a
 - Staff
	 - Absent
	 - Invoices
	 - Shift
 - Company
	 - Bill (electricity, water, staff payment, inventory stocks supply)
	 - Branch
 - Phone & PC are the same?
 - Possibility of merge multiple company into one database
 - ~~Staff Author for each transaction or changes~~?


- Feature: Tags or Categories


users
	edit
		assigned staff
		email
		password
	create new user
		assigned staff
		email
		password
	create with staff
		name
		email
		address
		password
		....
Role & permission
	Associate with users
	Staff use title instead
	hard coded role & permission via edit user
active inactive unregistered
