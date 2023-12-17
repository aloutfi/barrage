#!/bin/bash

# Function to execute a command in each Git repository within a directory
execute_in_repos() {
    local dir=$1
    shift
    local command=$@

    # Traverse each subdirectory in the specified directory
    for d in "$dir"/*; do
        if [ -d "$d/.git" ]; then
            # Execute the command in the Git repository
            (cd "$d" && eval "$command")
        fi
    done
}

# Function to handle alias creation and usage
handle_alias() {
    echo "TODO"
}

# Main execution loop
if [[ "$1" == "alias" ]]; then
    # Handle alias creation and execution
    handle_alias "${@:2}"
else
    # General command execution
    # Capture the entire command to execute
    command_to_execute="$@"
    # Execute the command in each repository
    # Assuming the current directory is the repo directory
    execute_in_repos "$(pwd)" "$command_to_execute"
fi

