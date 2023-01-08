# check-ci-success

Using GitHub's API, check if the CI run on a given branch succeeded

## Inputs

### `repo_owner`

**Required** user or organization under which the repo is

### `repo_name`

**Required** name of the repo

### `branch_name`

**Required** name of the branch to check

### `check_name`

**Required** name of the check run to look for, eg "Travis CI - Branch"

### `github_token`

**Required** GitHub token to authenticate API requests, required because otherwise you risk hitting rate limits

## Outputs

None

## Example usage

```yaml
    - uses: samuelgruetter/check-ci-success@master
      with:
        repo_owner: 'mit-plv'
        repo_name: 'bedrock2'
        branch_name: 'master'
        check_name: 'Travis CI - Branch'
        github_token: ${{ secrets.GITHUB_TOKEN }}
```
