<h1 align="center">
  <br>
  <img width="150" height="150" src="gh-f-logo.png">
  <br>
</h1>

<h2 align="center">
  <a href="#" onclick="return false;">
    <img alt="PR" src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat"/>
  </a>
  <a href="https://github.com/gennaro-tedesco/stargazer/releases">
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

`gh-f` is the ultimate, compact and snappy `fzf` extension for `gh` cli. It addresses most of your daily GitHub workflow, if not all of it: `f` stands for fuzzy, fzf or fomething felse.

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
shows the help page.
```
gh f [cmd]
```
takes one of the following arguments or flags

| command      | description                               | binds
|:------------ |:----------------------------------------- |:------
| -r,runs      | show github workflow runs and filter logs | enter: search run logs
| -p,prs       | view, diff and checkout PR                | enter: checkout the selected PR<br>ctrl-d: diff the selected PR<br>ctrl-v: view the selected PR
| -b,branches  | checkout and diff branches                | enter: checkout the selected branch<br>ctrl-d: diff the selected PR
| -l,logs      | select commits and show diff              | enter: show selected commit diff
| -s,search    | search issues in any repository           | interactive prompt: follow instructions
| -m,myissue   | search issues you opened somewhere        | interactive prompt: follow instructions
| -h,help      | show help page                            |
| -V,version   | print the current version                 |

## Customisation
If you want to skip typing `gh f` before each command you may alias it directly, for instance
```
gh set alias prs --shell `gh f -p`
```
and likewise for the rest.

The prompt colours are defined via their ANSI sequences [here](https://github.com/gennaro-tedesco/gh-f/blob/37157bb30c2bceb99a5c9d6d199c543ce347690f/gh-f#L6-L9): change yourself accordingly, if you like different ones.

## Feedback
If you find this application useful consider awarding it a ⭐, it is a great way to give feedback! Otherwise, any additional suggestions or merge request is warmly welcome!
