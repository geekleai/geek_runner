# geek_runner
Self-hosted GitHub Actions like runner in the cloud.


## GCP
Terraform provisioning for:

- Ephemeral VMs in Managed Instance Group (MIG)
- Each VM instance processes maximum of one workflow job
- Each runner provisioned with its own GiHub token
- Configurable worker pool (size, machine type, CPU, memory, accelerators)
- VPC and VPC Service Controls with User-defined IAM service account, roles
- Customizable runner image with startup/shutdown script hooks