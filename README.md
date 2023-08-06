# Submodule Network
Action focused on updating child submodules of a corporate network. Useful for linked applications among different subsidiaries which shares the same core and wants to enable customizations of the source code. It supports both homogeneous and hybrid git environments in GitHub and Azure repositories.

## Usage

```yaml
- uses: bancolombia/submodule-network@v1
  with:
    # Personal access token (PAT) used to fetch the repository. 
    
    # We recommend using a service account with the least permissions necessary. Also
    # when generating a new PAT, select the least scopes necessary.
    subsidiary_token: xXyYzZ01?!

    #The repository url from GitHub or Azure domain. GitHub: owner/repo  -  Azure: <azure_domain>/repo
    subsidiary_repo_url: owner/repo

    #(ONLY REQUIRED FOR AZURE REPOS) Username of the Azure account with the neccesary permissions to clone the repository
    subsidiary_repo_username: john_doe

    #Either 'GitHub' or 'Azure'. Default value is 'GitHub'
    platform: GitHub

    #Either 'push' or 'pull-request' operations. Default value is 'push'
    operation: push

    #Branch of the submodule. Default value: 'main'
    subsidiary_branch: main   


```
