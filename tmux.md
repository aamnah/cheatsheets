# tmux
---
title: tmux cheatsheet
date: 2019-08-21
---


| action | key bindings |
|-|-|
| `tmux` | start new |
| `tmux new -s foo` | start new with session name |
| `tmux a #` | attach |
| `tmux a -t foo` | attach to named |
| `tmux ls` | List sessions |
| `tmux kill-session -t foo` | kill session |

### Sessions

| action | key bindings |
|-|-|
| `:new foo session` | new session |
| `s` | list sessions |
| `$` | name session |

### Windows

| action | key bindings |
|-|-|
| `<pre> c` | create window |
|  | kill current window |
| `<pre> &` | kill all windows |
| | rename current window |

### Panes

| action | key bindings |
|-|-|
| `%` | Vertical split |
| `"` | Horizontal split |
