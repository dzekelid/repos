{
  "info": {
    "name": "Bitbucket Get Repositories Username Repo Slug Patch Spec",
    "_postman_id": "e0f4e576-6495-49ef-b497-ce66c8cc2783",
    "description": "Produces a raw patch for a single commit (diffed against its first\nparent), or a patch-series for a revspec of 2 commits (e.g.\n`3a8b42..9ff173` where the first commit represents the source and the\nsecond commit the destination).\n\nIn case of the latter (diffing a revspec), a patch series is returned\nfor the commits on the source branch (`3a8b42` and its ancestors in\nour example). For Mercurial, a single patch is returned that combines\nthe changes of all commits on the source branch.\n\nWhile similar to diffs, patches:\n\n* Have a commit header (username, commit message, etc)\n* Do not support the `path=foo/bar.py` query parameter\n\nThe raw patch is returned as-is, in whatever encoding the files in the\nrepository use. It is not decoded into unicode. As such, the\ncontent-type is `text/plain`.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "repositories",
      "item": [
        {
          "id": "968bf1a0-2cf5-4a28-8dda-e8e430ac01c1",
          "name": "getRepositoriesUsernameRepoSlugPatchSpec",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "repositories/:username/:repo_slug/patch/:spec"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                },
                {
                  "id": "repo_slug",
                  "value": "repo_slug",
                  "type": "string"
                },
                {
                  "id": "spec",
                  "value": "spec",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Produces a raw patch for a single commit (diffed against its first\nparent), or a patch-series for a revspec of 2 commits (e"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0a941b6f-4cb9-4af7-8cf9-0aa2ed8d9e88"
            }
          ]
        }
      ]
    }
  ]
}