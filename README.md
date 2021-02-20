###### blog
```
https://creodias.eu/-/how-to-mount-object-storage-container-as-a-file-system-in-linux-using-s3fs-
```

###### save password
```
vi /etc/passwd-s3fs
esc : x!
```

s3_key:s3_passwd


###### Allow non-root users to specify the allow_other or allow_root mount options
```
sudo nano /etc/fuse.conf
uncomment user_allow_other
```

###### mount
```
sudo s3fs bucket_name local_folder -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-data-warehouse-uat ~/s3_bucket-phq8 -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-data-warehouse-video-record ~/ml-data-warehouse-video-record -o use_cache=/tmp/cache -o allow_other -o uid=1001 
sudo s3fs ml-kaden-data-interface-test ~/ml-kaden-data-interface-test -o use_cache=/tmp/cache -o allow_other -o uid=1001  -o umask=0277
sudo s3fs ml-kaden-data-analysis-test2 ~/ml-kaden-data-analysis-test2 -o use_cache=/tmp/cache -o allow_other -o uid=1001  -o umask=0277

```

###### reference
```
https://www.youtube.com/watch?v=f_YujEv7tdA. 
https://wintelguy.com/umask-calc.pl
```



