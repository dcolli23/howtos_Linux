---
title: Scripts To Modify Shell
nav_order: 5
---

# Scripts to Modify Shell

This page details how to create a script that modifies your shell environment. This was particularly handy when I wanted to only activate my conda environment when I chose to, instead of adding the intialization to my bashrc, I could make a script that could do this to my shell on demand.

## Steps

1. Create an executable file in your `/.local/bin/` folder.
    ```
    cd ~/.local/bin/
    vim <name_of_command>
    ```
2. Fill the contents of the command with whatever you want to do with your shell. As an example, this is what my script to activate a conda shell looks like.
    ```bash
    #!/bin/bash
    # Create a temporary file
    TMPFILE=$(mktemp)

    # Add stuff to the temporary file
    # bashrc for normal shell initialization
    echo "source ~/.bashrc" > $TMPFILE
    # bashrc_conda has the command to initialize the conda shell
    cat ~/.bashrc_conda >> $TMPFILE
    echo "rm -f $TMPFILE" >> $TMPFILE
    bash --rcfile $TMPFILE
    ```
    This is the contents of the bashrc_conda file for reference:
    ```bash
    # >>> conda initialize >>>
    # !! Contents within this block are managed by 'conda init' !!
    __conda_setup="$('/home/dylan/anaconda3/bin/conda' 'shell.bash' 'hook' 2> /dev/null)"
    if [ $? -eq 0 ]; then
        eval "$__conda_setup"
    else
        if [ -f "/home/dylan/anaconda3/etc/profile.d/conda.sh" ]; then
            . "/home/dylan/anaconda3/etc/profile.d/conda.sh"
        else
            export PATH="/home/dylan/anaconda3/bin:$PATH"
        fi
    fi
    unset __conda_setup
    # <<< conda initialize <<<
    ```
3. Make the command executable by the following:
    ```
    sudo chmod +x <path to script>
    ```