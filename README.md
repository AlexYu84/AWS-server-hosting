# CS312-final


## Setup
- [Install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli).
- [Install the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

## Configure Credentials

You will have to set-up your AWS credentials for Terraform to work - - [Configure the AWS CLI with an access key ID and secret access key](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html).
1. Start your AWS Academy Learner Lab
2. Click on "AWS" Details" in the top right corner of your Learner Lab page. ![preview](screenshot1.png)
3. Create the file `~/.aws/credentials` and copy the credentials from your "AWS Details" tab. Save the file.

Another option for windows is to use the CLI to setup the auth variables:

```aws configure set <variable> "<value>"```

For example:

```aws configure set aws_access_key_id "ASIAQ3SUJJBSZSG4BANA"```

You will have to run it three times to authenticate: the key, secret, and token.


## Steps
- Run `terraform init`.
- Run `terraform validate`
- Run `terraform apply`.
- Copy the IP outputted by terraform and put it in Minecraft
- Wait it a minute or two for the server to spin up.
- Play.
- Irrecoverably shut everything down with `terraform destroy`.
