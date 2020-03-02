# Branch naming rules

Github action to enforce Pull Request title conventions

## Usage

See [action.yml](./action.yml)

```yaml
steps:
- uses: deepakputhraya/action-pr-title@master
  env:
    GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
    regex: '([a-z])+\/([a-z])+' # Regex the title should match.
    allowed_prefixes: 'feature,stable,fix' # title should start with the given prefix
    prefix_case_sensitive: false # title prefix are case insensitive
    min_length: 5 # Min length of the title
    max_length: 20 # Max length of the title
```

## License
The scripts and documentation in this project are released under the [MIT License](./LICENSE)
