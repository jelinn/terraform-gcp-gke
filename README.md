# # Consumer GKE Module

This repo contains a Module to deploy a [Google Kubernetes Cluster](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/introduction.html) on 
[GCP](https://aws.amazon.com) using [Terraform](https://www.terraform.io/). 

## Who maintains and approves this module?

This module is maintained by the Organization’s Infrastructure Team.  Email infra@organization.com for more info.

| Version | Description | Security Team Approval? | Approver | Approval Date|
|———|——————|:——:|:——:|:——:|
| v0.0.2| Security Updates | Yes | John Doe | 01/01/2019 |
| v0.0.1 | Initial GKE | No | N/A | N/A |

<!——
## How do you use this Module?



 
## How do I contribute to this Module?

Contributions are very welcome! Check out the [Contribution Guidelines](https://github.com/hashicorp/terraform-azurerm-vault/tree/master/CONTRIBUTING.md) for instructions.



## How is this Module versioned?

This Module follows the principles of [Semantic Versioning](http://semver.org/). You can find each new release, 
along with the changelog, in the [Releases Page](../../releases). 

During initial development, the major version will be 0 (e.g., `0.x.y`), which indicates the code does not yet have a 
stable API. Once we hit `1.0.0`, we will make every effort to maintain a backwards compatible API and use the MAJOR, 
MINOR, and PATCH versions on each release to indicate any incompatibilities. 



# Google Cloud GKE Terraform module

Terraform module which creates a GKE cluster on GCP.


—>
## Usage

```hcl
module “elb” {
  source  = “app.terraform.io/<YOURTFEORGNAME>/consumer-elb/aws”
  version = “1.13”
  name = “${var.name}-elb”
  environment = “${var.environment}”
  
  # ELB attachments
  number_of_instances = “${var.number_of_instances}”
  instances           = [“${module.ec2_instances.id}”]
}
  
module “ec2_instances” {
  source = “app.terraform.io/<YOURTFEORGNAME>/consumer-ec2-instance/aws”
  version = “1.4”
  name                        = “${var.name}-ec2”
  instance_count = “${var.number_of_instances}”
}

```
<!— BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK —>

## Inputs

| Name | Description | Type | Default | Required |
|———|——————|:——:|:——:|:——:|
| environment | Choose: dev,stage,prod | string | - | yes |
| instances | List of instances ID to place in the ELB pool | list | `<list>` | yes |
| name | The name of the ELB | string | - | yes |
| number_of_instances | Number of instances to attach to ELB | string | `2` | no |

<!——
| access_logs | An access logs block | list | `<list>` | no |
| connection_draining | Boolean to enable connection draining | string | `false` | no |
| connection_draining_timeout | The time in seconds to allow for connections to drain | string | `300` | no |
| cross_zone_load_balancing | Enable cross-zone load balancing | string | `true` | no |
| health_check | A health check block | list | - | yes |
| idle_timeout | The time in seconds that the connection is allowed to be idle | string | `60` | no |
| internal | If true, ELB will be an internal ELB | string | - | yes |
| listener | A list of listener blocks | list | - | yes |
| security_groups | A list of security group IDs to assign to the ELB | list | - | yes |
| subnets | A list of subnet IDs to attach to the ELB | list | - | yes |
| tags | A mapping of tags to assign to the resource | string | `<map>` | no |
——>

## Outputs

This module contains no outputs.

| Name | Description |
|———|——————|


<!——————
| Name | Description |
|———|——————|
| this_elb_arn | The ARN of the ELB |
| this_elb_dns_name | The DNS name of the ELB |
| this_elb_id | The name of the ELB |
| this_elb_instances | The list of instances in the ELB |
| this_elb_name | The name of the ELB |
| this_elb_source_security_group_id | The ID of the security group that you can use as part of your inbound rules for your load balancer’s back-end application instances |
| this_elb_zone_id | The canonical hosted zone ID of the ELB (to be used in a Route 53 Alias record) |
—>
<!— END OF PRE-COMMIT-TERRAFORM DOCS HOOK —>

## Configurations Baked into Module


## Further Reading



<!——————
## Known Issues/Limitations


## Authors

Module managed by [HashiCorp SE Team](https://github.com/hashicorp).


## What’s a Module?

A Module is a reusable, best-practices definition for how to run a single piece of infrastructure, such 
as a database or server cluster. 

Instead of having to figure out the details of how to run a piece of infrastructure from scratch, you can reuse 
existing code that has been proven in production and approved by the security team.
——————>

