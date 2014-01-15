# git-sync

`git-sync` allows you to easily synchronize a local git repository to a remote location.

## Dependencies

`git-sync` requires [jq](http://stedolan.github.io/jq/download/) (read the installation instructions there).

## Setup

1. Clone this repo: `git clone git@github.com:kflorence/git-sync.git`.
2. Put `git-sync` in your PATH (or: `sudo ln -s /path/to/git-sync /usr/bin/git-sync`)
3. Create a file in the root of your repo called "sftp-config.json" (this is the same file used by [Sublime SFTP](http://wbond.net/sublime_packages/sftp)) and put this in it:

```json
{
   "host": "remote-hostname",
   "user": "your-username",
   "remote_path": "/path/to/remote/repo"
}
```

## Usage

Just run `git-sync` inside of a git repository that contains an "sftp-config.json" file. See `git-sync -h` for more options.

### Filter out files listed in .gitignore

Add the following to your JSON configuration file:

```json
{
   "filter": ":- .gitignore"
}
```

### Set up a git alias

Add the following to your `.gitconfig` file:

```
[alias]
    sync = !git-sync
```

Now you can sync by running `git sync`
