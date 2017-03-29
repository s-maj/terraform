---
layout: "aws"
page_title: "AWS: aws_api_gateway_client_certificate"
sidebar_current: "docs-aws-resource-api-gateway-client-certificate"
description: |-
  Provides an API Gateway Client Certificate.
---

# aws\_api\_gateway\_client\_certificate

Provides an API Gateway Client Certificate.

~> **Note:** All arguments including the PEM encoded certificate will be stored in the raw state as plain-text.
[Read more about sensitive data in state](/docs/state/sensitive-data.html).

## Example Usage

```
resource "aws_api_gateway_client_certificate" "demo" {
  description = "My client certificate"
}
```

## Argument Reference

The following arguments are supported:

* `description` - (Optional) The description of the client certificate.


## Attribute Reference

The following attributes are exported:

* `id` - The identifier of the client certificate.
* `created_date` - The date when the client certificate was created.
* `expiration_date` - The date when the client certificate will expire.
* `pem_encoded_certificate` - The PEM-encoded public key of the client certificate.

## Import

API Gateway Client Certificates can be imported using the id, e.g.

```
$ terraform import aws_api_gateway_client_certificate.demo ab1cqe
```
