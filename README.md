# capstone-projectDOCUMENTATION  

                   CAPSTONE PROJECT

PREREQUISITES FOR THE PROJECT

* Choose a google cloud provider of your choice, in the case of this project, I used AWS
* Create an EC2 on the AWS, using ubuntu t2 medium because of the nature of the project. So that it won’t be dragging for too long
* Install AWS CLI
* Install JENKINS
* Install HELM
* Install TERRAFORM
* Install KUBECTL
* Install ZIP
* Create IAM User with administration privileges


                    Installer.sh
In the installer.sh file,  all the prerequisite file needed to be installed as hi-lighted above, are written in a bash script in the installer.sh and ran automatically, instead of installing them one after the other manually. Using this method makes it easier and faster.


                       USAGE
Configuration in this directory creates an  AWS EKS cluster using Jenkins for continuous integration and deployment

￼
￼
Note that running this project may create resources which cost money. Destroy resources created immediately using Jenkins destroy.


                              REQUIREMENTS

       Name	     Version
  Terraform	  >=1.3

   AWS	   >=5.40
   Jenkins	    >=2.44



                                 PROVIDERS
      Name	   version
       aws	    >=5.40     



                                  MODULES
    source	     Version
terraform-aws-modules/vpc/aws	   >=5.5.2

             

                                       EKS-OUTPUTS.TF
    output	   Describeiption
cluster_id	
       
                                  
￼
      

￼


￼



￼
     




￼



￼



                                                    USAGE

* Create an ec2  instance  on AWS  on any availability zone of your choice, attache vpc, internet gateway, route table, public $ private subnet and security group to it. 
* Launch the ec2 instance and clone the git repository using git clone then the repo,
* Cd into the capstone- project and input ls. And all the project files will be highlighted, among which are eke folder,kubernetic folder, cluster-jenkinsfile , installer.sh and jenkinsfile .
* Make the installer.sh executable with chmod +x  installer.sh
* Open the batch script and  automatically install all the files in it, as listed above
* Copy the public ip on the ec2 instance and place it  on google with port 8080 . The Jenkins site will pop up and ready to use
* Register on Jenkins platform. And put  the required GitHub parameters for continuous integration and continuous deployment
* Cluster-jenkinsfile is  created  first and later create jenkinsfile. And Jenkins will build ,orchestrate   eke cluster,route53, prometheus grafana and every utility in  the files.
* Open route53 and go to hosts 1, the domain name in the code comes out live. Click on it and name server parameters will come up. Copy the 4 name server and put it on your manage name server 
* Copy the grafana custom name on that page and put on your google. The grafana site pops up, input the default password, and user id. User “admin” and the password is “prom-operator”
* On the grafana site, you will be able to  check  and monitor the infrastructure.
