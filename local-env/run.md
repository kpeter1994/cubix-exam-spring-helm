# How to run the background application locally
You will not get exact running commands, rather just help how to run it locally.

## Image name
The name of the image to run (including tag) is:
```
quay.io/drsylent/cubix/exam/background:springboot3
```

## Configuration
The application will not start up without configuring the 
__BACKGROUND_TOKEN__ environment variable. The value of this variable will be used 
for validating the call, so the callers must set this up appropriately too.

The application uses the 8080 port for serving both business requests and 
management functionalities.
