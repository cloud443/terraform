To deploy the cluster using the configuration file, you will need to run the following commands:

Initialize the Terraform working directory:

terraform init


Review the proposed changes:

terraform plan


Deploy the cluster:

terraform apply


This will create the EKS cluster and all of the necessary resources defined in the configuration file.

Note: The terraform apply command will prompt you to confirm the changes before they are applied. To bypass this confirmation, you can use the -auto-approve flag.

Once the cluster has been deployed, you can verify that it was created successfully by running the following command:
