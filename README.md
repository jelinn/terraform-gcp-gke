Consumer GKE Module

This repo contains a Module to deploy a [Google Kubernetes Cluster](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/introduction.html) on 
[GCP](https://aws.amazon.com) using [Terraform](https://www.terraform.io/). 

## Who maintains and approves this module?

This module is maintained by the Organization’s Infrastructure Team.  Email infra@organization.com for more info.

```
`| Version | Description | Security Team Approval? | Approver | Approval Date|`

`|———|——————|:——:|:——:|:——:|`

`| v0.0.2| Security Updates | Yes | John Doe | 01/01/2019 |`

`| v0.0.1 | Initial GKE | No | N/A | N/A |`
```


## How do you use this Module?



 
## How do I contribute to this Module?

Contributions are welcome! Check out the Contribution Guidelines instructions.



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
module “gke” {

source = “app.terraform.io/jlinn/gke/gcp”

version = “0.0.1”

cluster_name = “jlinn-demo”

gcp_project = “justin-linn”

gcp_region = “us-east1”

gcp_zone = “us-east1-c”

initial_node_count = 3

}

```


## Inputs



## Outputs


## Configurations Baked into Module


## Further Reading

## Known Issues/Limitations


## Authors

Module managed by [HashiCorp SE Team](https://github.com/hashicorp).


## What’s a Module?

A Module is a reusable, best-practices definition for how to run a single piece of infrastructure, such 
as a database or server cluster. 

Instead of having to figure out the details of how to run a piece of infrastructure from scratch, you can reuse 
existing code that has been proven in production and approved by the security team.
