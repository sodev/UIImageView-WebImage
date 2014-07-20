UIWebImageView
====================

An extension of UIView to allow image views to be set from a URL or AWS S3 string

##Usage
UIWebImage is an extension of UIImage that allows users to create an Image view from either a URL or an AWS S3 key string.
UIWebImage utilises AFNetworking and AWSS3 frameworks for the image retrieval as well as allowing the user to set a placeholder image.

##Example
```objective-c
    UIImageView *webImage = [[UIImageView alloc] initWithFrame:webImageFrame];
    [webImage setPlaceholderImage:[UIImage imageNamed:@"placeholderImage"]];
    
    
    [webImage setImageFromS3withAccessKey:@"aws_access_key"
                                    secretKey:@"aws_secret_key"
                                    keyString:@"aws_key_string"
                                 bucketString:@"aws_bucket_name"];
                                 
OR

  [webImage setImageFromUrl:[NSURL URLWithString:@"https://www.google.com.au/images/srpr/logo11w.png"]];
```
