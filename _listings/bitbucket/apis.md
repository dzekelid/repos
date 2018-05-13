---
name: Bitbucket
description: Code against the Bitbucket API to automate simple tasks, embed Bitbucket
  data into your own site, build mobile or desktop apps, or even add custom UI add-ons
  into Bitbucket itself using the Connect framework.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
x-kinRank: "8"
x-alexaRank: ""
tags:
- Stack Network
- Imports
- Developers
created: "2018-03-23"
modified: "2018-03-23"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/apis.yaml
specificationVersion: "0.14"
apis:
- name: Bitbucket
  description: Code against the Bitbucket API to automate simple tasks, embed Bitbucket
    data into your own site, build mobile or desktop apps, or even add custom UI add-ons
    into Bitbucket itself using the Connect framework
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
  humanURL: ""
  baseURL: https://api.bitbucket.org//2.0
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/users-username-repositories-parameters.md
- name: Bitbucket Add Repositories Username Repo Slug Commits
  description: |-
    Identical to `GET /repositories/{username}/{repo_slug}/commits`,
    except that POST allows clients to place the include and exclude
    parameters in the request body to avoid URL length issues.

    **Note that this resource does NOT support new commit creation.**
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
  humanURL: https://bitbucket.org/
  baseURL: https://api.bitbucket.org//2.0
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-commits-post.md
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-commits-post-postman.md
- name: Bitbucket Add Repositories Username Repo Slug Issues
  description: |-
    Creates a new issue.

    This call requires authentication. Private repositories or private
    issue trackers require the caller to authenticate with an account that
    has appropriate authorisation.

    The authenticated user is used for the issue's `reporter` field.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
  humanURL: https://bitbucket.org/
  baseURL: https://api.bitbucket.org//2.0
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-issues-post.md
- name: Bitbucket Add Repositories Username Repo Slug Pipelines
  description: "Endpoint to create and initiate a pipeline. \nThere are a couple of
    different options to initiate a pipeline, where the payload of the request will
    determine which type of pipeline will be instantiated.\n# Trigger a Pipeline for
    a branch or tag\nOne way to trigger pipelines is by specifying the reference for
    which you want to trigger a pipeline (e.g. a branch or tag). \nThe specified reference
    will be used to determine which pipeline definition from the `bitbucket-pipelines.yml`
    file will be applied to initiate the pipeline. The pipeline will then do a clone
    of the repository and checkout the latest revision of the specified reference.\n\n###
    Example\n\n```\n$ curl -X POST -is -u username:password \\\n  -H 'Content-Type:
    application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n  -d '\n  {\n    \"target\": {\n      \"ref_type\": \"branch\", \n      \"type\":
    \"pipeline_ref_target\", \n      \"ref_name\": \"master\"\n    }\n  }'\n```\n#
    Trigger a Pipeline for a commit on a branch or tag\nYou can initiate a pipeline
    for a specific commit and in the context of a specified reference (e.g. a branch,
    tag or bookmark).\nThe specified reference will be used to determine which pipeline
    definition from the bitbucket-pipelines.yml file will be applied to initiate the
    pipeline. The pipeline will clone the repository and then do a checkout the specified
    reference. \n\nThe following reference types are supported:\n\n* `branch` \n*
    `named_branch`\n* `bookmark` \n * `tag`\n\n### Example\n\n```\n$ curl -X POST
    -is -u username:password \\\n  -H 'Content-Type: application/json' \\\n  https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n  -d '\n  {\n    \"target\": {\n      \"commit\": {\n        \"type\": \"commit\",
    \n        \"hash\": \"ce5b7431602f7cbba007062eeb55225c6e18e956\"\n      }, \n
    \     \"ref_type\": \"branch\", \n      \"type\": \"pipeline_ref_target\", \n
    \     \"ref_name\": \"master\"\n    }\n  }'\n```\n# Trigger a specific pipeline
    definition for a commit\nYou can trigger a specific pipeline that is defined in
    your `bitbucket-pipelines.yml` file for a specific commit. \nIn addition to the
    commit revision, you specify the type and pattern of the selector that identifies
    the pipeline definition. The resulting pipeline will then clone the repository
    and checkout the specified revision.\n\n### Example\n\n```\n$ curl -X POST -is
    -u username:password \\\n  -H 'Content-Type: application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
    \        \"type\":\"commit\"\n       },\n        \"selector\": {\n           \"type\":\"custom\",\n
    \             \"pattern\":\"Deploy to production\"\n          },\n        \"type\":\"pipeline_commit_target\"\n
    \  }\n  }'\n```\n# Trigger a specific pipeline definition for a commit on a branch
    or tag\nYou can trigger a specific pipeline that is defined in your `bitbucket-pipelines.yml`
    file for a specific commit in the context of a specified reference. \nIn addition
    to the commit revision, you specify the type and pattern of the selector that
    identifies the pipeline definition, as well as the reference information. The
    resulting pipeline will then clone the repository a checkout the specified reference.\n\n###
    Example\n\n```\n$ curl -X POST -is -u username:password \\\n  -H 'Content-Type:
    application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
    \        \"type\":\"commit\"\n       },\n       \"selector\": {\n          \"type\":
    \"custom\",\n          \"pattern\": \"Deploy to production\"\n       },\n       \"type\":
    \"pipeline_ref_target\",\n       \"ref_name\": \"master\",\n       \"ref_type\":
    \"branch\"\n     }\n  }'\n```"
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
  humanURL: https://bitbucket.org/
  baseURL: https://api.bitbucket.org//2.0
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-pipelines-post.md
x-common:
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: https://bitbucket.org/
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: https://bitbucket.org/
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: https://bitbucket.org/
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: https://bitbucket.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---