Instruction link: 
https://github.com/tmux-plugins/tpm

1. Clone TPM: 
 `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
2. Create `~/.tmux.conf`
'''
set -g default-terminal "screen-256color"
# Sort session by name
bind S choose-tree -sZ -0 name

# List of plugins
set -g @plugin 'tmux-plugins/tpm'
set -g @ptugin 'tmux-plugins/tmux-sensible'

set -g @plugin 'christoomey/vim-tmux-navigator'
set -g @plugin 'jimeh/tmux-themepack'
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
set -g @plugin 'tmux-plugins/tmux-sessionist'

set -g @themepack 'powerline/default/purple'

set -g @plugin @resurrect-capture-pane-contents 'on'
set -g @continuum-restore 'on'

# Initialize TMUX plugin manager (keep this line at the very bottom of tmux.conf)
run '~/.tmux/plugins/tpm/tpm'
'''
4. Install plugins 

`tmux source ~/.tmux.conf`

Press `prefix + I` (capital `i`, as in Install) to fetch the plugin.
