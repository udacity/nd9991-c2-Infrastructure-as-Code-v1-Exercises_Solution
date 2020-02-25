-------------------------
This is how you store a value in the Parameter Store:

aws ssm put-parameter --name "DBURL" --value "testdb.com" --type String --overwrite

In this case, storing the parameter DBURL with the value testdb.com
and overwriting if the parameter already exists.
-------------------------

This is how you get a parameter from the Parameter Store:

aws ssm get-parameter --name "DBURL"

The output will be in JSON format,so, 
you'll need to parse the "Value" from it.
-------------------------

In order to do this from your EC2 Instances, you'll need a role
assigned that provides access to Systems Manager (SSM)