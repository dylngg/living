## Opening tmux

You open a new tmux session by running `tmux`. You can also attach to a existing session using `tmux attach`. You can detach a window by typing `^b d` or `^b :detach` (See below).

## Vi vs Emacs Key Bindings

There are two different options for keybindings in tmux: vi and emacs. The default when you start up is emacs unless `EDITOR` or `VISUAL` contains "vi", in which case vi keybindings are set. You can override this in `~/.tmux.conf` via `set-window-option -g mode-keys vi` or `set-window-option -g mode-keys emacs`.

## Creating and modifying windows and panes

The keybindings to create various panes are as follows: (`^b` must be type immediately before)

| Keybinding | What does it do? |
| --- | --- |
| `%` | Opens a pane on the right side (taking up half the space) of the active window |
| `"` | Opens a pane on the bottom side (taking up half the space) of the active window |
| `c` | Opens a new window to the right (and switches to it). You can also use `:new-window` |
| `,` | Renames the current window. You can also use `:rename-window` |

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

You can enter copy mode (which allows you to scroll) by running `^b [`. In this mode you can scroll up and down and see lines past your viewport (vim's hjll movement works in when in vi mode!). To copy text in vi mode you'd hit the `<space>` bar to start a selection and in emacs mode you'd do a `^<space>` (ctl-spacebar) combo. At this point you can use the arrow keys to select the text you want to copy. Once satistifed with your selection, hit `<enter/return>` if in vi mode or `<alt>-w` in emacs mode and the selection will be copied into tmux's buffer. To paste what's in the current buffer do `^b ]`.

In summary:

| Mode | Keybinding | What does it do? |
| --- | --- | --- |
| vi/emacs | `^b [` | Enters copy mode. |
| vi | `<space>` | Allows you to start a selection (in copy mode). |
| emacs | `^<space>` | Allows you to start a selection (in copy mode). |
| vi | `<enter/return>` | Copies the selection into tmux's buffer (after selecting in in copy mode). |
| emacs | `<alt>-w` | Copies the selection into tmux's buffer (after selecting in in copy mode). |
| vi/emacs | `^b ]` | Pastes tmux's buffer. |

## Sources

You can contribute to this document [here](https://github.com/dylngg/living/tree/master/tmux) by opening a merge request or an issue. Any and all contributions, as well as feedback, is welcome.

<http://man.openbsd.org/OpenBSD-current/man1/tmux.1> (`man 1 tmux`)

<https://leanpub.com/the-tao-of-tmux/read>

<https://awhan.wordpress.com/2010/06/20/copy-paste-in-tmux/>
