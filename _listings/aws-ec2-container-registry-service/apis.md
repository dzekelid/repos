---
name: AWS EC2 Container Registry Service
x-slug: aws-ec2-container-registry-service
description: Amazon EC2 Container Registry (ECR) is a fully-managedDockercontainer
  registry that makes it easy for developers to store, manage, and deploy Docker container
  images. Amazon ECR is integrated withAmazon EC2 Container Service (ECS), simplifying
  your development to production workflow. Amazon ECR eliminates the need to operate
  your own container repositories or worry about scaling the underlying infrastructure.
  Amazon ECR hosts your images in a highly available and scalable architecture, allowing
  you to reliably deploy containers for your applications. Integration with AWS Identity
  and Access Management (IAM) provides resource-level control of each repository.
  With Amazon ECR, there are no upfront fees or commitments. You pay only for the
  amount of data you store in your repositories and data transferred to the Internet.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Repos
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/apis.md
specificationVersion: "0.14"
apis:
- name: AWS EC2 Container Registry API - Create Repository
  x-api-slug: actioncreaterepository-get
  description: Creates an image repository.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actioncreaterepository-get-openapi.md
- name: AWS EC2 Container Registry API - Delete Repository
  x-api-slug: actiondeleterepository-get
  description: Deletes an existing image repository.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actiondeleterepository-get-openapi.md
- name: AWS EC2 Container Registry API - Delete Repository Policy
  x-api-slug: actiondeleterepositorypolicy-get
  description: Deletes the repository policy from a specified repository.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actiondeleterepositorypolicy-get-openapi.md
- name: AWS EC2 Container Registry API - Describe Repositories
  x-api-slug: actiondescriberepositories-get
  description: Describes image repositories in a registry.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actiondescriberepositories-get-openapi.md
- name: AWS EC2 Container Registry API - Get Repository Policy
  x-api-slug: actiongetrepositorypolicy-get
  description: Retrieves the repository policy for a specified repository.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actiongetrepositorypolicy-get-openapi.md
- name: AWS EC2 Container Registry API - Set Repository Policy
  x-api-slug: actionsetrepositorypolicy-get
  description: Applies a repository policy on a specified repository to control access
    permissions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Compute_AmazonECR.png
  humanURL: https://aws.amazon.com/ecr/
  baseURL: :///
  tags: Amazon Web Services, Containers, Discovery, Stack Network, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/aws-ec2-container-registry-service/actionsetrepositorypolicy-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.ec2.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.ec2.container.registry.service.stack.network
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