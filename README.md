  # Mendable Action
  
  ## How to use it?
  
  - Copy the snippet below into `.github/workflows/mendable.yml`

  
  ```yaml
  # On issue opened
    on:
      issues:
        types:
          - opened
      
    name: Mendable Action
    
    jobs:
      chatgpt_comment:
        runs-on: ubuntu-latest
        name: Suggest solutions to issues - Mendable Action
        steps:
          - uses: actions/checkout@v2
          - name: Suggest solutions to issues - Mendable Action
            uses: SideGuide/mendable-public-action@v0.1
            id: mendable-action
            with:
              number: ${{ github.event.issue.number }}
              mode: 'issues'
            env:
              GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }} 
 ```
 
   - That's it! You should be all set for now.
