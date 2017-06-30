<img src="cf-loggetter-logo.png" align="middle">

# CF-LogGetter

Download, decompress and consolidate AWS CloudFront CDN logs into a human-readable single file on your Windows machine.

## PURPOSE                             

To download and consolidate all CloudFront Logs from the specified S3 bucket.                          

___                                                            

## PRE-REQUISITES                         
                                                            
The following needs to be completed before using this cmd:  
                                                            
1. All CloudFront logs are stored on an S3 bucket in your AWS account.                                             
2. AWS CLI and gzip were installed.                         
3. The path where aws.exe and gzip.exe are installed were included in the PATH system variable.                    
4. AWS configure has been run and the access keys and region have been set.                                           
5. Copy the files getcflog.bat and settimestamp.bat to the folder where you would like to generate the CloudFront log file.                                                

___                                                            

## SYNTAX                                                             
                                                            
 > getcflog <websitename/s3-bucket-name> [cf-indicator]     
                                                            
 ### websitename:                                               
website for which cloudfront logs need to be downloaded. Use this if the bucket name of it's cloudfront logs are in the format  

> logs.websitename/cdn  

otherwise use **s3-bucket-name** directly.

### s3-bucket-name:                                            
the name of the bucket where the cloudfront logs are stored.                              
                                                            
### cf-indicator:                                              
set this to Y if using s3-bucket-name.

___                                                            

## OUTPUT  
                                                            
The Output File would be generated with the following name format:                                                      
      **cf-logs.D-yyyy-mm-dd-T_hh_mm_ss.txt**                   
