
forked [tinoji/delete-older-releases](https://github.com/tinoji/delete-older-release-assets).

Add following step to your workflow:

```yaml
- uses: bien-omosura/delete-older-release-assets@v1.0.1
  with:
    repo: <owner>/<repoName> # defaults to current repo
    keep_latest: 3
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

