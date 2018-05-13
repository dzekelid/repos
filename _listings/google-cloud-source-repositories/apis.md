---
name: Google Cloud Source Repositories
description: Google Cloud Source Repositories provides Git version control to support
  collaborative development of any application or service, including those that run
  on Google App Engine and Google Compute Engine. If you are using the Stackdriver
  Debugger, you can use Cloud Source Repositories and related tools to view debugging
  information alongside your code during application runtime. Cloud Source Repositories
  also provides a source browser that you can use to view your repository files from
  within the Cloud Console.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-repositories.png
x-kinRank: "9"
x-alexaRank: ""
tags:
- Stack Network
- SDKs
- SDK
- Orchestration
- Google APIs
- GitHub
- Code
created: "2018-03-23"
modified: "2018-03-23"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/google-cloud-source-repositories/apis.yaml
specificationVersion: "0.14"
apis:
- name: Cloud Source Repositories API
  description: Google Cloud Source Repositories provides Git version control to support
    collaborative development of any application or service, including those that
    run on Google App Engine and Google Compute Engine
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-repositories.png
  humanURL: ""
  baseURL: ://sourcerepo.googleapis.com//
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/google-cloud-source-repositories/v1-resource-testiampermissions-post.md
- name: Cloud Source Repositories API Create Repo
  description: |-
    Creates a repo in the given project with the given name..

    If the named repository already exists, `CreateRepo` returns
    `ALREADY_EXISTS`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-cloud-repositories.png
  humanURL: https://cloud.google.com/source-repositories/
  baseURL: http:://sourcerepo.googleapis.com//
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/google-cloud-source-repositories/v1-parent-repos-post.md
x-common:
- type: x-concepts
  url: https://cloud.google.com/source-repositories/docs/concepts
- type: x-documentation
  url: https://cloud.google.com/source-repositories/docs/
- type: x-getting-started
  url: https://cloud.google.com/source-repositories/docs/quickstart
- type: x-guides
  url: https://cloud.google.com/source-repositories/docs/how-to
- type: x-pricing
  url: https://cloud.google.com/source-repositories/pricing
- type: x-website
  url: https://cloud.google.com/source-repositories/
- type: x-concepts
  url: https://cloud.google.com/source-repositories/docs/concepts
- type: x-documentation
  url: https://cloud.google.com/source-repositories/docs/
- type: x-getting-started
  url: https://cloud.google.com/source-repositories/docs/quickstart
- type: x-guides
  url: https://cloud.google.com/source-repositories/docs/how-to
- type: x-pricing
  url: https://cloud.google.com/source-repositories/pricing
- type: x-website
  url: https://cloud.google.com/source-repositories/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---