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
sudo s3fs ml-data-warehouse-uat ~/s3_bucket-phq8 -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-data-warehouse-video-record ~/ml-data-warehouse-video-record -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-kaden-data-interface-test ~/ml-kaden-data-interface-test -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-kaden-data-interface-test ~/ml-kaden-data-analysis-test -o use_cache=/tmp/cache -o allow_other -o uid=1001 

```

###### reference
https://www.youtube.com/watch?v=f_YujEv7tdA




