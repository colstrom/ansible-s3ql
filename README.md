# ansible-s3ql

[S3QL](https://bitbucket.org/nikratio/s3ql/) is a file system that stores all its data online using storage services like Google Storage, Amazon S3, or OpenStack.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

Tunables
--------
* `s3ql_log_root` (string) - Directory for logs
* `s3ql_log_path` (string) - Path for log file
* `s3ql_mountpoint` (string) - Mountpoint for S3QL
* `s3ql_authinfo_path` (string) - Location of auth file
* `s3ql_cache_path` (string) - Path for cache data
* `s3ql_user` (string) - User to run S3QL as
* `s3ql_group` (string) - Group to run S3QL as
* `s3ql_bucket_name` (string) - Bucket Name
* `s3ql_access_key_id` (string) - Access Key ID for S3
* `s3ql_secret_access_key` (string) - Secret Access Key for S3
* `s3ql_encryption_enabled` (boolean) - Encrypt data before storing?
* `s3ql_encryption_password` (string) - Password for encryption?

Dependencies
------------
* [colstrom.apt-repository](https://github.com/colstrom/ansible-apt-repository/)

Example Playbook
----------------
    - hosts: servers
      roles:
         - role: colstrom.s3ql
           s3ql_bucket_name: mybucketname
           s3ql_mountpoint: /mnt/s3

License
-------
[MIT](https://tldrlegal.com/license/mit-license)

Contributors
------------
* [Chris Olstrom](https://colstrom.github.io/) | [e-mail](mailto:chris@olstrom.com) | [Twitter](https://twitter.com/ChrisOlstrom)
* Aaron Pederson
