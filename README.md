## demo video for week 8: *CloudFormation Lambda Layers Command Line Tool Major ~~hiccup~~ success*  
	
Please click the video to hear sound or follow along with the transcript that's set just below the video.

<video src="https://user-images.githubusercontent.com/38410965/111996814-c792c180-8af0-11eb-8c29-147ebaae2a01.mp4" autoplay controls loop muted style="max-width: 730px;">
</video>


![demo](https://user-images.githubusercontent.com/38410965/111996814-c792c180-8af0-11eb-8c29-147ebaae2a01.mp4
)

#

> Hello everyone and thank you for watching. This will be a sparse presentation echoing the longer more in-depth one I posted on Monday.  Hiccup turned to success this week and CloudFormation was a breeze.  I’ve made progress therefore on work started Lambda Layers and on new work initializing data on DynamoDB and in and linting the whole mess in a command line tool.  This means that the infra builds on its own and takes itself apart on its own. Nice.

### CloudFormation
### Lambda Layers
### Command Line Tool 
### Major ~~hiccup~~ success

**Steve Depp**
**MSDS 498 section 61**

**Demo Video 8**

- [x] Lambda layers 
via pandas + numpy downloads

- [x] DynamoDB
initializing data

- [x] CLT
Makefile, linting 


#

> For Lamnda Layers ...

### Lambda Layers for ServerlessProducer and ProducerAI

<img width="712" alt="template yml" src="https://user-images.githubusercontent.com/38410965/113763198-67eb0780-96e7-11eb-8f03-1ab8e30d3486.png">

#

> ... one key was sticking to Python 3.6.  

### Python 3.7 and Python 3.8 don’t work

<img width="712" alt="template yml" src="https://user-images.githubusercontent.com/38410965/113763177-60c3f980-96e7-11eb-8843-1bd282d9d2bb.png">

#

> Another ...

### Steps to layering: Install dependencies - locally

<img width="1387" alt="@ 2-build-layer sh" src="https://user-images.githubusercontent.com/38410965/113763152-599ceb80-96e7-11eb-9392-ddd1b805b925.png">

#

> ... was ...

### Remove Pandas and Numpy dependencies

<img width="1387" alt="2-build-layer sh" src="https://user-images.githubusercontent.com/38410965/113763126-50ac1a00-96e7-11eb-9be9-f9d92d75cfe0.png">

#

> ... using fresh copies of linux pandas and numpy, ...

### Fresh copy of linux Pandas and Numpy - locally

<img width="1387" alt="@ 2-build-layer sh ) No Selection" src="https://user-images.githubusercontent.com/38410965/113763097-4ab63900-96e7-11eb-8c68-5dbbb48b76ed.png">

#

> ... and cleaning up any traces of dependencies designed for OS X. [pause]

### Clean up any traces of previous Pandas and Numpy e.g. *.dist-info files

<img width="1387" alt="@ 2-build-layer sh" src="https://user-images.githubusercontent.com/38410965/113763072-438f2b00-96e7-11eb-99d3-2158f8f168c2.png">

#

> Success initializing Dynamo DB, ...

### Initialize DynamoDB

<img width="752" alt="facebook" src="https://user-images.githubusercontent.com/38410965/113763050-3c681d00-96e7-11eb-9ec3-4cc6cd86d1cc.png">

#

> ... programmatically rather than via Dynamo console. 

### Programmatically convert to DDB format

<img width="726" alt="(request t)" src="https://user-images.githubusercontent.com/38410965/113763028-36723c00-96e7-11eb-80b6-43d717f33c5f.png">

#

> So, this functionality transfers to new data and edits of existing via command line tool.

### Do this for new data too —> CLT 

<img width="712" alt="request json" src="https://user-images.githubusercontent.com/38410965/113763006-2f4b2e00-96e7-11eb-894d-10ce0b134bc0.png">

#

> Success with make file that creates a bucket, ... 


### Makefile - make bucket

<img width="752" alt="Makefile" src="https://user-images.githubusercontent.com/38410965/113762987-28bcb680-96e7-11eb-9204-c79fba84987a.png">

#

> ... builds dependency files, ...

### Makefile - build dependencies for layers

<img width="752" alt="Makefile" src="https://user-images.githubusercontent.com/38410965/113762963-22c6d580-96e7-11eb-9b21-a8f496a17806.png">

#

> ... deploys to the AWS stack, ...

### Makefile - deploy

<img width="752" alt="Makefile" src="https://user-images.githubusercontent.com/38410965/113762933-1b073100-96e7-11eb-9f46-d4e445e71717.png">

#

> ... and does that DynamoDb initialization, ...

### Makefile - initialize DynamoDB

<img width="752" alt="Makefile" src="https://user-images.githubusercontent.com/38410965/113762906-1478b980-96e7-11eb-91cb-765857547a3b.png">

#

> ... all at once, if needed. 

### make infra - do it all

<img width="752" alt="Makefile" src="https://user-images.githubusercontent.com/38410965/113762869-0a56bb00-96e7-11eb-95dd-3af2e3349678.png">

#

> To save money and time and nervous energy worrying that you left the AWS oven on, the infra tears itself apart too.

### Makefile - tear it down

<img width="752" alt="bucket" src="https://user-images.githubusercontent.com/38410965/113762826-ff9c2600-96e6-11eb-9c42-445fc5ff0933.png">

#

> Rather than demo live, here’s a timed version from make infra at zero seconds, ...


### make infra @ zero seconds

<img width="682" alt="Last login Fri" src="https://user-images.githubusercontent.com/38410965/113762773-f27f3700-96e6-11eb-8163-488fa28b6e1d.png">

<img width="239" alt="0000 00" src="https://user-images.githubusercontent.com/38410965/113762783-f4e19100-96e6-11eb-8a9c-13050ae0b596.png">

#

> ... getting the OS X copy of dependencies including pandas, ...

### get OS X version of pandas

<img width="682" alt="Collecting pandas" src="https://user-images.githubusercontent.com/38410965/113762742-eabf9280-96e6-11eb-9ebb-5f77b721433b.png">

#

> ... and numpy, ...

### ditto numpy

<img width="682" alt="ython-dateutil-2 8 1 python-json-lopper-2 0 1 pytz-2828 4 requests-2 24 0 satran" src="https://user-images.githubusercontent.com/38410965/113762722-e3988480-96e6-11eb-83f6-0b12e9ee36e4.png">

#

> ... getting linux version of pandas, ...

### Get linux version of pandas

<img width="682" alt="100 16 5M 100 16 5M" src="https://user-images.githubusercontent.com/38410965/113762694-dc717680-96e6-11eb-87ba-d2b254fdd50b.png">

#

> ... and again numpy, ...

### ditto numpy

<img width="682" alt="_distributor_init py" src="https://user-images.githubusercontent.com/38410965/113762671-d4b1d200-96e6-11eb-9728-841cdf67c740.png">

#

> ... starting the deployment, ...

### begin deployment to AWS stack @ 52 seconds

<img width="682" alt="inflating packageProducerAlpythoneumpytestingprint_coercion_tables py" src="https://user-images.githubusercontent.com/38410965/113762627-c82d7980-96e6-11eb-8e31-ef0521125f39.png">

<img width="239" alt="0052 66" src="https://user-images.githubusercontent.com/38410965/113762642-cc599700-96e6-11eb-9ae8-713e0bb42a57.png">

#

> ... finishing most of the deployment instructions, ...

### Initialize DynamoDB @ 3 minutes 55 seconds

<img width="682" alt="decorators py" src="https://user-images.githubusercontent.com/38410965/113762570-bb108a80-96e6-11eb-9f61-5d12a3bc371c.png">

<img width="241" alt="0355 71" src="https://user-images.githubusercontent.com/38410965/113762582-bd72e480-96e6-11eb-9463-ff811ac15981.png">

#

> ... watch it build on the Cloud Formation console, ...

### Infra just begins to show up on cloud formation at this point ~ 4 minutes

<img width="1194" alt="CloudFormation - Sta X" src="https://user-images.githubusercontent.com/38410965/113762513-a7652400-96e6-11eb-89a2-99e7d38b7711.png">

#

> ... see it finish. 

### Infra continues to build well after the terminal prompt is returned 

<img width="1194" alt="CloudFormation - Sta X" src="https://user-images.githubusercontent.com/38410965/113762480-a03e1600-96e6-11eb-9db6-90900bd31ffa.png">

# 

> So, at 4 minutes 45 seconds, we begin to tear it down.

### Tear it down - infra finished building at 4 minutes 45 seconds

<img width="682" alt="pytestingnosetester py" src="https://user-images.githubusercontent.com/38410965/113762443-94525400-96e6-11eb-96c2-f6c984b4bb74.png">

<img width="237" alt="0445 80" src="https://user-images.githubusercontent.com/38410965/113762463-99170800-96e6-11eb-955e-7faa904943ec.png">

#

### Delete the stack, and stack artifacts on S3

<img width="682" alt="waiting for stack createupdate to complete" src="https://user-images.githubusercontent.com/38410965/113762418-8c92af80-96e6-11eb-86d5-392e9ee1af3e.png">

#

### As with deploying, prompt is returned but deletion continues for a bit longer.

<img width="1194" alt="CloudFormation - Sta X" src="https://user-images.githubusercontent.com/38410965/113762371-83a1de00-96e6-11eb-8970-769c7cd8e11c.png">

#

### Round trip in ...

<img width="1194" alt="fp-cloud-formation-c X" src="https://user-images.githubusercontent.com/38410965/113762323-77b61c00-96e6-11eb-8e86-e931369a1082.png">

#

> Thanks very much. 

### 6 minutes 50 seconds ~ similar to S.A.M.

<img width="245" alt="0650 72" src="https://user-images.githubusercontent.com/38410965/113762261-68cf6980-96e6-11eb-82ab-d768eb018a54.png">

**Thank you.**










