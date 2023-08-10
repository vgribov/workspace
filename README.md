# Usage

The following command creates a folder under `$HOME/Workspaces` with a given
name and starts a `tmux` session there:

    workspace <Name>

The specified workspace folder can contain a `workspace.yml` file with
environment variables:

    environment:
    - FOO=Foo_value
    - BAR=Bar_value

They will be added to the `tmux new-session` command as:

    -e FOO=Foo_value -e BAR=Bar_value

