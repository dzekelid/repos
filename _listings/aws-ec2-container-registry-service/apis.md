---
name: AWS EC2 Container Registry Service
description: Amazon EC2 Container Registry (ECR) is a fully-managednbsp;Dockernbsp;container
  registry that makes it easy for developers to store, manage, and deploy Docker container
  images. Amazon ECR is integrated withnbsp;Amazon EC2 Container Service (ECS), simplifying
  your development to production workflow. Amazon ECR eliminates the need to operate
  your own container repositories or worry about scaling the underlying infrastructure.
  Amazon ECR hosts your images in a highly available and scalable architecture, allowing
  you to reliably deploy containers for your applications. Integration with AWS Identity
  and Access Management (IAM) provides resource-level control of each repository.
  With Amazon ECR, there are no upfront fees or commitments. You pay only for the
  amount of data you store in your repositories and data transferred to the Internet.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
x-kinRank: "10"
x-alexaRank: ""
tags:
- Stack Network
- Discovery
- Containers
- Amazon Web Services
created: "2018-03-23"
modified: "2018-03-23"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/apis.yaml
specificationVersion: "0.14"
apis:
- name: AWS EC2 Container Registry API
  description: Amazon EC2 Container Registry (ECR) is a fully-managednbsp;Dockernbsp;container
    registry that makes it easy for developers to store, manage, and deploy Docker
    container images
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: ""
  baseURL: :///
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/action-setrepositorypolicy-get.md
- name: AWS EC2 Container Registry API Describe Repositories
  description: Describes image repositories in a registry.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: http:://{host}//
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/action-describerepositories-get.md
x-common:
- type: x-documentation
  url: http://docs.aws.amazon.com/AmazonECR/latest/APIReference/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/ecr/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/ecr/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/ecr/pricing/
- type: x-website
  url: https://aws.amazon.com/ecr/
- type: x-documentation
  url: http://docs.aws.amazon.com/AmazonECR/latest/APIReference/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/ecr/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/ecr/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/ecr/pricing/
- type: x-website
  url: https://aws.amazon.com/ecr/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---