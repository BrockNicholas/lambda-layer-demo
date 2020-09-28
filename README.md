# lambda-layer-demo

Add desired library folders to a folder named `python`


Zip the contents
`zip -r custom_lambda_funcs.zip ./python`

Upload as AWS Lambda Layer

Add layer to your function

Import from your included directories in your function:
e.g., 

>import simplejson
>
>def lambda_handler(event, context):
>    
>    
>    return {
>        'statusCode': 200,
>        'body': simplejson.dumps('Hello from Lambda!')
>    }


## Notes
You can also create the `python` directory in the format `python/lib/python3.8/site-packages`

Update the 3.8 to whichever python you're using. But the plain ol' `/python` directory works in most cases
