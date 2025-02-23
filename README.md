# harvard-coachin


AWS:

- create a bucket by the name : www.harvardinstitute.org
- go to properties and enable static website hosting : give index and error file names
- upload files to the bucket 
- select region : Bombay
- once done you can open this page: http://www.harvardinstitute.org.in.s3-website.ap-south-1.amazonaws.com/
- if it gives public access permission go to permission and 
- make this bucket public 
- add this permmission 
```json
{
	"Version": "2012-10-17",
	"Statement": [
		{
			"Sid": "PublicReadGetObject",
			"Principal": "*",
			"Effect": "Allow",
			"Action": [
			    "s3:GetObject"
			    ],
			    "Resource":[
			        "arn:aws:s3:::www.harvardinstitute.org.in/*"
			        ]
		}
	]
}
```
- now you can see the site : http://www.harvardinstitute.org.in.s3-website.ap-south-1.amazonaws.com/

