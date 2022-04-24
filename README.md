# learning-ci-cd-pipeline

### Basic Syntax

```yaml
# This is a basic workflow to help you get started with Actions

name: My CI/CD Pipeline

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the main branch
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

#   # Allows you to run this workflow manually from the Actions tab
#   workflow_dispatch:

# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      - name : Print Greetings
        run : echo "Hello ! Ahmed Ayaz"
        
      - name : Checking Node Version
        run : node -v
      
      - name : Checking NPM Version
        run : npm -v
      
      - name : Printing Event Name
        run : echo " ${{ github.event_name }} "
        
      - name : Printing Runner OS 
        run : echo " ${{ runner.os }} "
        
      - name : Printing Github Repository 
        run : echo " ${{ github.repository }} "
        
      - name : Farewell Command
        run : echo "Scene Done"
```

- `${{ env var }}` This is how we save environmental variables.