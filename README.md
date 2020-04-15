# tmux-rotate-pane

Install the scripts `tmux-merge-panes` and `tmux-split-pane` somewhere
in your `PATH`.

Then put something like the following into your `~/.tmux.conf`

    bind-key m run-shell tmux-merge-panes
    bind-key C-t run-shell tmux-split-pane
    bind-key C-n swap-pane -s :+.top \; rotate-window -Ut :+

Have tmux server reload its configuration and hit `prefix-C-t` to create
a split new pane, and another, and another...

Then use `prefix-C-n` to swap in a pane from the list of previously
created split panes.

Somewhere along the way `prefix-m` might be used to regroup all the
existing and unseen panes in the pool of panes swapped in by `prefix-C-n`.
