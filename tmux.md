# tmux

| action | key bindings |
|-----|-|
| `tmux` | start new |
| `tmux new -s sessionTitle` | start new with session name |
| `tmux a #` | attach |
| `tmux a -t sessionTitle` | attach to named |
| `tmux ls` | List sessions |
| `tmux kill-session -t sessionTitle` | kill session |

### Sessions

| action | key bindings |
|-----|-|
| `:new foo session` | new session |
| `s` | list sessions |
| `$` | name session |

### Windows

| action | key bindings |
|-----|-|
| `c` | create window |
|  | kill current window |
| `&` | kill all windows |
| | rename current window |

### Panes

| action | key bindings |
|-----|-|
| `%` | Vertical split |
| `"` | Horizontal split |
| `x` | kill current pane |
