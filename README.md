# CS312-final


## Setup
- [Install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli) (tested on 1.1.3).
- [Install the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html).

## Configure Credentials

You will have to set-up your AWS credentials for Terraform to work - - [Configure the AWS CLI with an access key ID and secret access key](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html).
1. Start your AWS Academy Learner Lab
2. Click on "AWS" Details" in the top right corner of your Learner Lab page.



## Steps
- Run `terraform init`.
- Run `terraform apply`.
- Copy the IP output by the previous command into Minecraft.
- Wait a minute for the server to spin up.
- Play.
- Irrecoverably shut everything down with `terraform destroy`.
