##### Basic usage
```python
# wsgi.py
from flask import Flask 
app = Flask(__name__)
```
run it with
```sh
python run wsgi.py
gunicorn -w 4 wsgi:app
# w = how much worker for handling request

# auto refresh, with debug on
flask --app example.py --debug run
```