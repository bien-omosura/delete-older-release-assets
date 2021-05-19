# GitHub Action: Delete older release assets

This action deletes older release assets (not releases) of given repo

Inspired by and forked [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases).

Add following step to your workflow:

```yaml
- uses: tinoji/delete-older-release-assets@v0.1.0
  with:
    repo: <owner>/<repoName> # defaults to current repo
    keep_latest: 3
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Available Options

#### `keep_latest`

| required |
| -------- |
| true     |

Specifies number of latest releases (sorted by `created_at`) to keep. Pass `0` if you want to delete all release assets.

#### `repo`

| required | default               |
| -------- | --------------------- |
| false    | repo executing action |

Repo name in the format of `<owner>/<repoName>`. Defaults to the repo that executing this action.
