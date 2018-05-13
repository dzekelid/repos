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
- name: Bitbucket Get Repositories Username Repo Slug Patch Spec
  description: |-
    Produces a raw patch for a single commit (diffed against its first
    parent), or a patch-series for a revspec of 2 commits (e.g.
    `3a8b42..9ff173` where the first commit represents the source and the
    second commit the destination).

    In case of the latter (diffing a revspec), a patch series is returned
    for the commits on the source branch (`3a8b42` and its ancestors in
    our example). For Mercurial, a single patch is returned that combines
    the changes of all commits on the source branch.

    While similar to diffs, patches:

    * Have a commit header (username, commit message, etc)
    * Do not support the `path=foo/bar.py` query parameter

    The raw patch is returned as-is, in whatever encoding the files in the
    repository use. It is not decoded into unicode. As such, the
    content-type is `text/plain`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/bitbucket-logo.png
  humanURL: https://bitbucket.org/
  baseURL: https://api.bitbucket.org//2.0
  tags: Repos
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-patch-spec-get.md
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/repos/master/_listings/bitbucket/repositories-username-repo-slug-patch-spec-get-postman.md
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