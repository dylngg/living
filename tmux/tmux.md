## Opening tmux

You open a new tmux session by running `tmux`. You can also attach to a existing session using `tmux attach`. You can detach a window by typing `^b d` or `^b :detach` (See below).

## Creating and modifying windows and panes

The keybindings to create various panes are as follows: (`^b` must be type immediately before)

| Keybinding | What does it do? |
| --- | --- |
| `%` | Opens a pane on the right side (taking up half the space) of the active window |
| `"` | Opens a pane on the bottom side (taking up half the space) of the active window |
| `c` | Opens a new window to the right (and switches to it). You can also use `:new-window` |

## Switching windows and panes

The easiest way to switch between panes is to use the following keybindings: `^b <arrowkey>`, where `<arrowkey>`. The easiest way to switch between windows is by using `^b n` and `^b p` (which switches to the next and previous windows).

| Keybinding | What does it do? |
| --- | --- |
| `^o` | Rotates the panes in the current window forwards |
| `0-9` | Switches to the indexed window (check the bottom for a number) |
| `'` | Prompts for the indexed window to switch to (check the bottom for a number) |
| `;` | Move to the previously active pane |
| `l` | Move to the previously active window |
| `!` | Moves the current pane into a new window |
| `{` | Swaps the current pane with the previous pane |
| `}` | Swaps the current pane with the next pane |

### Killing windows and panes

You can kill a pane with `^b x` and a window with `^b &`.

## Scrolling and Copying

You can enter copy mode (which allows you to scroll) by running `^b [`. There you can scroll up and down (vim keybindings even work!).

## Sources

You can contribute to this document [here](https://github.com/dylngg/living/tree/master/tmux) by opening a merge request or an issue. Any and all contributions, as well as feedback, is welcome.

<http://man.openbsd.org/OpenBSD-current/man1/tmux.1> (`man 1 tmux`)
<https://leanpub.com/the-tao-of-tmux/read>
