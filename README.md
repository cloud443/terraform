To deploy the cluster using the configuration file, you will need to run the following commands:

Initialize the Terraform working directory:

terraform init


Review the proposed changes:

terraform plan


Deploy the cluster:

terraform apply


This will create the EKS cluster and all of the necessary resources defined in the configuration file.

Note: The terraform apply command will prompt you to confirm the changes before they are applied. To bypass this confirmation, you can use the -auto-approve flag.

Once the cluster has been deployed,


Run the following command to retrieve the access credentials for your cluster and configure kubectl.

 aws eks --region $(terraform output -raw region) update-kubeconfig \
    --name $(terraform output -raw cluster_name)
    
    
    Verify the Cluster
Use kubectl commands to verify your cluster configuration.

First, get information about the cluster.

 kubectl cluster-info
 
 
 
 Clean up your workspace
 Destroy any resources you create when you are done with this tutorial. Run terraform destroy and confirm with yes in your terminal.
