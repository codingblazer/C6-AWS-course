# Launch instance in Public 1A
aws ec2 run-instances --image-id <value> --instance-type <value> --security-group-ids <value> --subnet-id <value> --key-name <value> --user-data <value>

=> Get the image id which AMI ID for linux 2 => from Ui launch instance button => first page will show ami id for linux2
=> instance type will be t2.micro
=> paste id of security group we created 
=> subnet id for public 1A we created 
=> from network and security paste the name of key pair we created earlier
=> file://<go to directory having user-data-subnet-d.txt file and give this name here with .txt> => this file has script which gets the metadata and prints the subnet from the EC2 instance in webapp running on it 

Run aws configure before running these and paste access key and secret for account and region and run the command above. It will run the instances and we can see that in UI => change the name of it to Public1a 

# Launch instance in Public 1B
Run the same command above with just subnet id changed + change the name from UI

# Launch instance in Private 1B
Run the same command above with just subnet id changed + change name 

# Terminate instances

aws ec2 terminate-instances --instance-ids <value> <value>