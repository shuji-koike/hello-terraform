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

## terraforming

* https://github.com/dtan4/terraforming

```
bundle exec terraforming ec2
bundle exec terraforming s3
bundle exec terraforming r53z
bundle exec terraforming r53r
```

## snippets

```
ln -s ~/.aws
cat .aws/credentials | grep -B1 aws_access_key_id
```
