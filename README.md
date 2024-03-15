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
    output	   Describeiption<img width="1440" alt="Screenshot 2024-03-13 at 22 25 17" src="https://github.com/obamstracon/capstone-project/assets/134118317/da994d6f-8126-40f2-b185-9b6c8b7b955e">

cluster_id	
       
                                  <img width="1440" alt="Screenshot 2024-03-13 at 20 11 43" src="https://github.com/obamstracon/capstone-project/assets/134118317/f2cd914b-8650-46d5-85e6-fc6437613ff6">
<img width="1440" alt="Screenshot 2024-03-13 at 21 34 29" src="https://github.com/obamstracon/capstone-project/assets/134118317/91760103-de95-455f-9bb2-10ba27990642">

￼
      
<img width="1440" alt="Screenshot 2024-03-06 at 21 25 18" src="https://github.com/obamstracon/capstone-project/assets/134118317/ec6f6b57-4f3e-40bc-974e-2e96ba7373e9">

￼

<img width="1440" alt="Screenshot 2024-03-12 at 20 14 38" src="https://github.com/obamstracon/capstone-project/assets/134118317/4380940e-758f-40fe-a00e-6faeb48a13bc">

￼

<img width="1440" alt="Screenshot 2024-03-13 at 20 33 01" src="https://github.com/obamstracon/capstone-project/assets/134118317/37d379da-abd9-4a04-8759-11830a82cdae">

<img width="1440" alt="Screenshot 2024-03-13 at 20 21 16" src="https://github.com/obamstracon/capstone-project/assets/134118317/0e537f4d-8072-46fa-8c4e-c78fc5fedb14">

￼
     <img width="1440" alt="Screenshot 2024-03-14 at 04 07 53" src="https://github.com/obamstracon/capstone-project/assets/134118317/35a214fc-49ef-45c6-b934-3ff8efee5682">





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
