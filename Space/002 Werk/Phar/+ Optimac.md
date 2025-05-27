
Todo Branch Management
Master
Dev
Demo
release/OPTIK_DEWI

Backup data

Delete rules
Future fix for soft delete with constraint unique
```php
$request->validate([
    'email' => [
        'required',
        'email',
        Rule::unique('users')->whereNull('deleted_at'),
    ],
]);
Schema::table('users', function (Blueprint $table) {
    $table->dropUnique('users_email_unique');
    $table->unique(['email', 'deleted_at']);
});
```


#### Future Fix
Update product price
- [x] Transaction total amount updated
- [ ] Product item on transaction updated
Delete product
- Remove delete on used product
- [ ] Retain the delete button again without deleting transaction record 
UI
- [ ] Hide/show sidebar saved into cookies
- [ ] Dark/light mode
Feature
- [ ] Report: Choose your own column
- [ ] Report/Transaction: Currency on amount
- [ ] Cashier: Checkbox/Dropdown choose add medical or not
- [ ] Customer Table: status human readable
- [ ] Cashier: Add customer on spot
- [ ] Cashier: optimize, if possible, less loading
- [ ] Add Feedback button
- [ ] spatie backup

#### Environment
```
demo
local
```
```
soft delete tables
user, staff
brands, frames-var, lens-var, contact-var, acc-var,
frame-stk, lens-stk, contact-stk, acc-stk,
frame-img, lens-img, contact-img, acc-img,
insurance, transaction, transaction-item, payments,
optical-medical-record,

```
#### dev
- [ ] Customer search no case sensitive
- [ ] Data type on cashier forms
#### to do when remote
- [x] Service apache
- [x] test service by restart the laptop
- [x] pull
- [x] migrate
- [ ] delete table staff_absents
- [x] delete row add soft delete from table migration