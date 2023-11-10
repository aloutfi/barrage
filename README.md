# barrage
A filepath-oriented command line utility for streamlining development and administration over multiple git repositories. 



## Examples

```bash
cd ~/Workspace/folder_of_repos/
barrage git checkout -b AOL/something-i-need-to-do-in-a-few-repos
```

```bash
barrage cp ~/Desktop/pull_request_template.md .github/ && git commit -m "chore: added  pull request template." .github/
```

```bash
barrage poetry lock && git commit -m "chore: ran lock" && git push
```



### Alias creation

```bash
barrage alias pr gh pr create --fill && gh pr merge --auto --merge && gh pr view --json url | jq -r ".url" 
barrage pr
```

```bash
barrage alias whereami basename -s .git `git config --get remote.origin.url`
barrage alias status whereami && git status
barrage status
```



## Requirements





## Installation

