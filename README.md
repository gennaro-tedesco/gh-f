<h1 align="center">
  <br>
  <img width="150" height="150" src="gh-f-logo.png">
  <br>
</h1>

<h2 align="center">
  <a href="#" onclick="return false;">
    <img alt="PR" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat"/>
  </a>
  <a href="https://github.com/gennaro-tedesco/gh-f/releases">
    <img alt="releases" src="https://img.shields.io/github/release/gennaro-tedesco/gh-f"/>
  </a>
</h2>

<h4 align="center">the ultimate compact fzf gh extension</h4>
<h3 align="center">
  <a href="#Installation">Installation</a> •
  <a href="#Usage">Usage</a> •
  <a href="#Customisation">Customisation</a> •
  <a href="#Feedback">Feedback</a>
</h3>

`gh-f` is the ultimate, compact and snappy `fzf` extension for `gh` cli. It addresses most of your daily GitHub workflow, if not all of it: `f` stands for filter, fzf or fomething felse.

## Installation
```
gh extension install gennaro-tedesco/gh-f
```
### Requirements
- fzf
- [gnu core utils](https://www.gnu.org/software/coreutils/)
- [bat](https://github.com/sharkdp/bat) (optional, if not detected it uses `less` as a pager, instead)

## Usage
Get started!
```
gh f
```
shows the help page. Or watch it in action:

[![asciicast](https://asciinema.org/a/EmYMmhOAn0dWAyBYrNqKk5AlR.svg)](https://asciinema.org/a/EmYMmhOAn0dWAyBYrNqKk5AlR)

```
gh f [cmd]
```
takes one of the following arguments or flags

| command      | description                               | binds
|:------------ |:----------------------------------------- |:------
| -a,adds      | add files to staging area                 | enter: add files to staging area<br>ctrl-d: diff selected file
| -r,runs      | show github workflow runs and filter logs | enter: search run logs
| -g,greps     | grep in files in revision history         | interactive prompt: insert regex, select files, show pattern in revision history
| -p,prs       | view, diff and checkout PR                | enter: checkout selected PR<br>ctrl-d: diff selected PR<br>ctrl-v: view selected PR
| -b,branches  | checkout and diff branches                | enter: checkout selected branch<br>ctrl-d: diff selected branch<br>ctrl-x: delete selected branch
| -l,logs      | select commits and show diff              | enter: show selected commit diff
| -t,tags      | checkout and diff version tags            | enter: checkout tag in detached HEAD<br>ctrl-d diff against current branch
| -s,search    | search issues in any repository           | interactive prompt: follow instructions
| -m,myissue   | search issues you opened somewhere        | interactive prompt: follow instructions
| -k,pick      | cherrypick files between branches         | enter: checkout cherrypicked files from branch
| -h,help      | show help page                            |
| -V,version   | print the current version                 |

Most commands follow the semantics of `git` standard instructions (so that you can remember them easily), only we append an `s` to avoid conflicts, should you have those commands lying around in the shell as aliases or for scripting.

## Customisation
If you want to skip typing `gh f` before each command you may alias it directly, for instance
```
gh set alias prs `f -p` # show PRs
gh set alias l `f -l` # show git logs
```
and likewise for the rest.

The prompt colours are defined via their ANSI sequences [here](https://github.com/gennaro-tedesco/gh-f/blob/37157bb30c2bceb99a5c9d6d199c543ce347690f/gh-f#L6-L9): change yourself accordingly, if you like different ones.

## Feedback
If you find this application useful consider awarding it a ⭐, it is a great way to give feedback! Otherwise, any additional suggestions or merge request is warmly welcome!

See also the complete family of extensions
- [gh-s](https://github.com/gennaro-tedesco/gh-s) to search for repositories with interactive prompt
- [gh-i](https://github.com/gennaro-tedesco/gh-i) to search for github issues with interactive prompt
