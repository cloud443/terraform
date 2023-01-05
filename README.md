Deploying the Cluster using the Configuration File
Initialize the Terraform working directory:
```bash
terraform init
Review the proposed changes:
```bash
terraform plan
Deploy the cluster:
```bash
terraform apply
Note: The terraform apply command will prompt you to confirm the changes before they are applied. To bypass this confirmation, you can use the -auto-approve flag.

Retrieve the access credentials for your cluster and configure kubectl:
```bash
aws eks --region $(terraform output -raw region) update-kubeconfig \
    --name $(terraform output -raw cluster_name)
Verify the cluster:
Use kubectl commands to verify your cluster configuration. First, get information about the cluster:

```bash
kubectl cluster-info
Clean up your workspace:
Destroy any resources you create when you are done with this tutorial. Run:

```bash
terraform destroy
and confirm with yes in your terminal.



