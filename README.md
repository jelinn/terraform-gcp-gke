Consumer GKE Module

This repo contains a Module to deploy a [Google Kubernetes Cluster](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/introduction.html) on 
[GCP](https://aws.amazon.com) using [Terraform](https://www.terraform.io/). 

## Who maintains and approves this module?

This module is maintained by the Organization’s Infrastructure Team.  Email infra@organization.com for more info.


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


