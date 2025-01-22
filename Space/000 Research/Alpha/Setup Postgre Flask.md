- pip install flask-sqlalchemy psycopg2/-binary
- put env = SQLALCHEMY_DATABASE_URI

```json
postgresql://quanta_quire_postgre_user:yqwOfyD75NJ4tLOybAsOc2Z9C2W7k0Uo@dpg-cqk06pij1k6c73a55dlg-a.singapore-postgres.render.com/quanta_quire_postgre

postgresql: \/\/ user : password @ hostname . server-location / database_name

```


- create the model class & db extensions
- flask shell run for creating table or database
	- db.create_all()
	- db.drop_all()

question -> answer -> ask feedback -> rating
chat q -> response a-f
	number then rating
save rating

question -> answer -> question
chat q -> response a-f
	answer then -1

