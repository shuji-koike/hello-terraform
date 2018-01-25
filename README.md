# hello-terraform
Hello, Terraform!

# links

* https://www.terraform.io/
* https://github.com/hashicorp/terraform

# setup

```sh
brew install terraform rbenv
```

```
rbenv install 2.5.0
rbenv local 2.5.0
bundle config --local path ./bundle
rbenv exec bundle
```

## terraform

```sh
terraform init

terraform plan

terraform show

terraform apply

terraform destroy
```

## terraforming

* https://github.com/dtan4/terraforming

```sh
bundle exec terraforming ec2
bundle exec terraforming s3
bundle exec terraforming r53z
bundle exec terraforming r53r
bundle exec terraforming sg --tfstate --merge=./terraform.tfstate

bundle exec terraforming iamg
bundle exec terraforming iamgm
bundle exec terraforming iamgp
bundle exec terraforming iamip
bundle exec terraforming iamp
bundle exec terraforming iampa
bundle exec terraforming iamr
bundle exec terraforming iamrp
bundle exec terraforming iamu
bundle exec terraforming iamup

bundle exec terraforming help | grep terraforming | grep -v help | awk '{print "bundle exec terraforming", $2, "--profile", "default", "--tfstate --merge=./terraform.tfstate", ">>", "current.tf";}' | sh
# find files that only have 1 empty line (likely nothing in AWS)
find . -type f -name '*.tf' | xargs wc -l | grep ' 1 .'
find . -size 1c -exec rm {} \;
```

## snippets

```sh
ln -s ~/.aws
cat .aws/credentials | grep -B1 aws_access_key_id
```
