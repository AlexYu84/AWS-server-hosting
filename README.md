

## Background
we will being hosting a minecraft server through AWS. However, we will do this ONLY through terraform and scripts. We will not need to connect to AWS in any way besides starting up the lab/AWS session.


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


## Steps - https://media.oregonstate.edu/media/t/1_wsmzsls8
- Run `terraform init`.
- Run `terraform validate`.
- Run `terraform apply`.
- Copy the IP outputted by terraform and put it in Minecraft
- Wait a minute or two for the server to spin up. (this might take a while)
- Play.
- Irrecoverably shut everything down with `terraform destroy`.

## Sources

https://github.com/HarryNash/terraform-minecraft
https://canvas.oregonstate.edu/courses/1914651/assignments/9243895?module_item_id=23242128

## Bonus
If you want to keep up with the newest minecraft version you will need to go into the main.tf file and edit one line.
On line 62 of main.tf:

`wget -O server.jar https://piston-data.mojang.com/v1/objects/84194a2f286ef7c14ed7ce0090dba59902951553/server.jar`

Replace the link: "https://piston-data.mojang.com/v1/objects/84194a2f286ef7c14ed7ce0090dba59902951553/server.jar" with whatever jar link that is provided the [Official Minecraft Website Download](https://www.minecraft.net/en-us/download/server).
