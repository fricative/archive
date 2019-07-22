replace the hardcoded initialization of `db_config` dictionary variable located at the top of 
gmap_pipeline/gmap/src/app.py with the following:

```
db_config = {
    "host": os.environ['db_host'],
    "user": os.environ['db_user'],
    "password": os.environ['db_password'],
    "db": os.environ['db_name'],
}
```

just like how it is done in preprocess_pipeline/preprocess/src/app.py. 
