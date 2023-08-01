# python-actions
Action to check for pending translations in projects which use Qt Linguist.
<br><br>
## License
Please see [LICENSE](LICENSE)
<br><br>
## Usage
Create a workflow file inside your repo in .github/workflow and add the following.
Change the name and the triggering event to fit your needs.
```yml
name: pending-translations

on: [workflow_dispatch]

jobs:
    translation_job:
      runs-on: ubuntu-latest
      name: Pending translations check
      steps:
        - uses: trippedBit/qtlinguist-check-pending-translations@v1.0.0
          with:
            pro-file: translation.pro
  
```
### Inputs
The following inputs are available:
* pro-file: pro file which lists the files to check. This is a required input.