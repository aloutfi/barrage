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

- Git
- Bash



## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/aloutfi/barrage.git
    cd barrage
    ```

2. Make the script executable:
    ```bash
    chmod +x barrage
    ```

3. Move the script to a directory in your PATH, for example:
    ```bash
    sudo mv barrage /usr/local/bin/
    ```

## Alias Management

### Creating an Alias

To create an alias, use the `barrage alias` command followed by the alias name and the command you want to alias. For example:

```bash
barrage alias myalias "echo Hello, World!"
```

This will create an alias named `myalias` that runs the command `echo Hello, World!`.

### Using an Alias

To use an alias, simply call it by its name:

```bash
barrage myalias
```

This will execute the command associated with the alias.

### Listing Aliases

To list all aliases, you can view the contents of the `.barrage_aliases` file in your home directory:

```bash
cat ~/.barrage_aliases
```

### Removing an Alias

To remove an alias, you can manually edit the `.barrage_aliases` file and remove the corresponding line.
