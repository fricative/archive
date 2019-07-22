replace the hardcoded initialization of `db_config` dictionary variable located at the top of 
gmap_pipeline/gmap/src/app.py with the following:

```
db_config = {
    "host": os.environ['db_host'],
    "user": os.environ['db_user'],
    "password": os.environ['db_password'],
    "db": os.environ['db_name'],
    'cursorclass': pymysql.cursors.DictCursor
}
```

Also, one needs to create S3 buckets with globally unique name and replace with your own bucket names in 
`setup.sh`, `app.py` of the preprocess lambda and the two template.yaml files
