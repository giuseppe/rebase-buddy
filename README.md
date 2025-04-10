# RebaseBuddy

RebaseBuddy is a tool that uses Claude AI to automatically write or
check your Git commit messages.

It is nothing more than an experiment to play with the Claude AI API.

### Setup

An Anthropic API key is required.  The Anthropic API key is expected
   at the `~/anthropic/key` path.
   ```
   mkdir -p ~/.anthropic
   echo "your-anthropic-api-key" > ~/.anthropic/key
   ```

## Usage

### Check a commit message

To analyze the most recent commit and receive suggestions:

```
rebase-buddy
```

### Automatically improve a commit message

To replace the most recent commit message with an AI-improved version:
\
```
rebase-buddy --inline
```

### git rebase -i

It is meant to be used interactively with `git rebase -i`.  To
rewrite/improve the git commit message for the current branch, you can
run:

```
git rebase -i $base_branch -x 'rebase-buddy [--inline]'
```

If `--inline` is specified to `rebase-buddy`, then the git commit
message is replaced inline and amended to the git patch.

## License

rebase-buddy is licensed under the GNU General Public License v2.0 or later.
