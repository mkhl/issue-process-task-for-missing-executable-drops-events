## This issue is now fixed

## Running a task with type `process` should emit the right events

Steps to reproduce:

1. Run the task `process`
1. Run the task `process` again.
1. Note that each failed in its own terminal, despite what the message in the terminal said.
1. Focus the terminal and press a key to close it.
1. Run the task `shell`.
1. Run the task `shell` again.
1. Note that both failed in the same terminal, again not shared with the `process` task.
1. Without closing the terminal, run the task `process` again.
1. Note that the task reuses the terminal now, but doesn't fail. Instead it just produces no output at all, and doesn't seem to signal that it's finished.
