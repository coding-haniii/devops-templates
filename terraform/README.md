# devops-templates/terraform
 - @author. haeun kim
 - @date.   2023-08-01
 - @title.  Terraform Templates to create Cloud Architect & Resources  
 - @keywords.  DevOps / AWS / terraform 

---------------------------------------------------------------------------
# Welcome! Follow these steps.
### Initi Env. in Linux(AWS)
```
* AWS Cli install
$curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
$unzip awscliv2.zip
$sudo ./aws/install
$aws --version
```
-------------------------------------------------------
### Terraform install
```
$sudo yum install -y yum-utils shadow-utils
$sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo
$sudo yum -y install terraform
$sudo mv /usr/bin/terraform /usr/local/bin/  (set terraform on system command)
$terraform -version
```
-------------------------------------------------------
### AWS Configure with AWS access key
```
$aws configure                   (*To do this step, You should create your accesskey on your AWS console)
AWS Access Key ID [None]: 
AWS Secret Access Key [None]: 
Default region name [None]: 
Default output format [None]:    (Option: text|json)

$aws configure list
$aws sts get-caller-identity
```
-------------------------------------------------------
### Terraform command
```
$terraform init      (Confirm current env)
$terraform plan      (Read .tf files && Compare and show summary, err)
$terraform apply     (Exec .tf files && Create resources)
$terraform destroy   (Remove created resources)
```
-------------------------------------------------------
### Ref.
 - https://cloudbim.tistory.com/14
 - https://docs.aws.amazon.com/powershell/latest/userguide/pstools-appendix-sign-up.html (Access key, Eng AWS Manual)
 - https://gain-yoo.github.io/devops/20/ (Access key, Korean)
 - https://notepad96.tistory.com/209  (Setting IDE: VSCODE, Window)  
