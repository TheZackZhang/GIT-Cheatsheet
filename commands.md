
# Git Commands

## Snapshotting
### status
### add
### commit
### reset
### mv
### rm

## Branching & Merging
### branch
### checkout 
```
git checkout <branch>
git checkout <commit>
```
Options
- -b
- --detach

### sparse-checkout
```
git sparse-checkout set <directory>
git sparse-checkout add <directory>
git sparse-checkout disable
git sparse-checkout reapply
```
Options (for set)
- --cone (default yes)
- --sparse-index (default no)
- --stdin

### merge
### tag
### stash

## Sharing & Updating
### fetch
```
git fetch [<options>] [<repository> [<refspec>...]]
```
```
git fetch --all [<options>]
```
- Fetch all remotes

### pull
### push
### remote
```
git remote add [-t <branch>] [-m <master>] [-f] [--[no-]tags] [--mirror=(fetch|push)] <name> <url>
```
- Add a remote named \<name> for the repository at \<url>

Options:
- -v --verbose
  - show remote url after name. For promisor remotes, also show the filter configured (eg: blob:none)

### submodule

## Inspection & Comparison
### show
```
git show <object>
```
### log
```
git log [<options>] [<revision-range>] [[--] <path>...]
```
- Show commit logs

```
git log foo bar ^baz
```
- Show log of the commits reacheable from foo or bar, and not from baz

Options:
- -- \<path>...
  - Limit commits to the given path
- --first-parent
  - Follow only the first parent commit upon seeing a merge commit
- --before=\<date>, --after=\<date>
- --author=\<pattern>
- --grep=\<pattern>

### diff
```
git diff [<options>] --no-index [--] <path> <path>
```
- Compare the given two paths on the filesystem

```
git diff [<options>] [--merge-base] <commit> [--] [<path>...]
```
- View the changes in my working tree relative to the given commit

```
git diff [<options>] [--merge-base] <commit> <commit> [--] [<path>...]
```
- View the changes between two arbitrary commits

```
git diff
```
- Changes in the working tree not yet staged for the next commit

```
git diff --cached
```
- Changes between the index and last commit. This is what would be commited if run `git commit`

Options:
- --name-only
  - Show only names of changed files
- --summary
  - asd 
- --output=\<file>
  - Output to a particular file instead of stdout
- -- \<path>
  - Limit comparison to the given path

### difftool
### describe

## Patching
### cherry-pick
### rebase
### revert

## Debugging
### bisect
### blame