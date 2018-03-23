# RDS
This repository contain RDS commands

exec msdb.dbo.rds_backup_database 
        @source_db_name='db_name', 
        @s3_arn_to_backup_to='arn:aws:s3:::bucket-name/db_name.bak',
        @overwrite_S3_backup_file=1;


exec msdb.dbo.rds_task_status @task_id=14;

exec msdb.dbo.rds_task_status @db_name='db_name';

exec msdb.dbo.rds_restore_database 
        @restore_db_name='db_name', 
        @s3_arn_to_restore_from='arn:aws:s3:::bucket-name/db_name.bak';
