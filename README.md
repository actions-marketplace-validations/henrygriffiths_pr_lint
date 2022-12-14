# PR Lint
This action makes sure PR titles are linted with commitlint and project management issue keys

Examples:

One issue key: `fix(deps): issue-123: fixing deps`

Multiple issue keys: `fix(deps): issue-123, key-1234: fixing deps`

# Usage
```yaml
- uses: henrygriffiths/pr_lint@v3
  with:
    # Required
    # Issue Key used in project management system
    # If multiple keys are used, separate via comma (eg: keya,keyb)
    issuekey: ''
    
    # Optional
    # Manually provide PR title via actions
    # Default: ${{ github.event.pull_request.title }}
    prtitle: ''
    
    # Optional
    # Manually provide types (comma separated)
    # Default: 'build,ci,chore,docs,feat,fix,perf,refactor,revert,style,task,test'
    types: ''
    
    # Optional
    # Allow linting to pass when no issue key is provided
    # Default: true
    allownokey: true
    
    # Optional
    # Word used when no issue key is provided
    # Default: none
    nokeyword: ''
```


# License

This project is released under the [MIT License](LICENSE)
