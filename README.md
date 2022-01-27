## Query Data Sources (VPC)
In this tutorial, you will use Terraform to deploy a workspace containing a VPC and security groups on AWS in the us-east-1 region. Next, you will use the aws_availability_zones data source to configure your VPC's Availability Zones (AZs), allowing you to deploy this configuration in any AWS region. Then, you will use the terraform_remote_state data source to deploy another workspace containing your application infrastructure to your VPC. Finally, you will use the aws_ami data source to configure the correct AMI for the current region.

### Update VPC region
- Change to the VPC repository directory.
- `cd learn-terraform-data-sources-vpc`
- Add the `aws_availability_zones.available` to `main.tf`.
- Update the VPC configuration to use this data source to set the list of availability zones.
- `terrform init`
- `terraform apply -var aws_region=us-west-1`
- Add a data source to `main.tf` to access region information.
- Add an output for the region to `outputs.tf`.
- `terraform apply -var aws_region=us-west-1`

### Reference
https://learn.hashicorp.com/tutorials/terraform/data-sources