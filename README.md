###### blog
```
https://fullstacknotes.com/mount-aws-s3-bucket-to-ubuntu-file-system/
```

###### save password
```
vi /etc/passwd-s3fs
esc : x!
```

s3_key:s3_passwd


###### mount
```
sudo s3fs bucket_name local_folder -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-data-warehouse-uat /phq8 -o use_cache=/tmp/cache -o allow_other -o uid=1001 
```




