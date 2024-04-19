# terraform-aws-vpcbatch5
## Create main.tf file and input following


```hcl
module "vpc" {
    source = "1askat9/vpcbatch5/aws"
    region = "us-east-2"
    vpc_cidr = "10.0.0.0/16"
    subnet1_cidr = "10.0.1.0/24"
    subnet2_cidr = "10.0.2.0/24"
    subnet3_cidr = "10.0.3.0/24"
    ip_on_launch = true
    instance_type = "t2.micro"
    subnet1_nmae = "hello1"
    subnet1_nmae = "hello2"
    subnet1_nmae = "hello3"
    ports= [22, 80, 81]
   

} 

```

## Create appache.sh file and input script. Eg.
```hlc
#!/bin/bash


sudo apt update
sudo apt install apache2 -y
sudo sysytemctl start apache2
sudo sysytemctl enable apache2
```