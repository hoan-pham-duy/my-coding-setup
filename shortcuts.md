*** VScode ***
- Switch between split windows:
+ MacOS: cmd+1,2,...
+ Linux: control+1,2,...
- Switch between explorer and editor:
+ MacOs: cmd+shift+p -> explorer = shortcut: cmd+shift+e
+ Linux:

- Open file in explorer in the sidebar
+ Macos: control + enter
+Linux:

- Open file in explorer in new tab:
+ In setting.json, setup 
{
  "workbench.editor.enablePreview": false
}


*** VIM ***
- Go to definition: gD
- Indentation a file: gg=G
- Move cursor to middle of line: gm
- edit in new tab: tabnew <path_to_file>
- switch between tabs: 1gt, 2gt
- switch windows position: ctrl+w+r, ...?
- Run a command: :! open https://github.com
- open terminal below: below terminal
- change position of window: ctrl+w+r
- rename file in NerdTree: https://stackoverflow.com/questions/1205286/renaming-the-current-file-in-vim
- create new file and open in newtab: !touch newfile.txt    -> :tabnew newfile.txt 
- remove hightlight: :noh


*** Tmux ***
# Open command
Ctrl-b :
# session management
tmux ls (or tmux list-sessions)
tmux new -s session-name
Ctrl-b d Detach from session
tmux attach -t [session name]
tmux kill-session -t session-name

Ctrl-b c Create new window
Ctrl-b d Detach current client
Ctrl-b l Move to previously selected window
Ctrl-b n Move to the next window
Ctrl-b p Move to the previous window
Ctrl-b & Kill the current window
Ctrl-b , Rename the current window
Ctrl-b q Show pane numbers (used to switch between panes)
Ctrl-b o Switch to the next pane
Ctrl-b ? List all keybindings

# moving between windows
Ctrl-b n (Move to the next window)
Ctrl-b p (Move to the previous window)
Ctrl-b l (Move to the previously selected window)
Ctrl-b w (List all windows / window numbers)
Ctrl-b window number (Move to the specified window number, the
default bindings are from 0 -- 9)

# Tiling commands
Ctrl-b % (Split the window vertically)
CTRL-b " (Split window horizontally)
Ctrl-b o (Goto next pane)
Ctrl-b q (Show pane numbers, when the numbers show up type the key to go to that pane)
Ctrl-b { (Move the current pane left)
Ctrl-b } (Move the current pane right)

# Make a pane its own window
Ctrl-b : "break-pane"
# Move the pane
Ctrl-b-o
# Resize pane
:resize-pane -D (Resizes the current pane down)
:resize-pane -U (Resizes the current pane upward)
:resize-pane -L (Resizes the current pane left)
:resize-pane -R (Resizes the current pane right)
:resize-pane -D 10 (Resizes the current pane down by 10 cells)
:resize-pane -U 10 (Resizes the current pane upward by 10 cells)
:resize-pane -L 10 (Resizes the current pane left by 10 cells)
:resize-pane -R 10 (Resizes the current pane right by 10 cells)
# add to ~/.tmux.conf
bind | split-window -h
bind - split-window -v

