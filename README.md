# Usage

This simple shell script wraps `tmux` to add the `here` command, which starts
`tmux` in the current working directory which becomes a *workspace folder*.

You can either use it as a separate tool:

    workspace here

Or symlink it to wrap `tmux`:

    sudo ln -s $PWD/workspace /usr/local/bin/tmux
    cd path/to/your/workspace
    tmux here

The workspace folder can contain a `workspace.yml` file with environment
variables:

    environment:
    - FOO=Foo_value
    - BAR=Bar_value

They will be added to the `tmux new-session` command as:

    -e FOO=Foo_value -e BAR=Bar_value
