# git-sync

`git-sync` allows you to easily synchronize a git repository to a remote location.

## Dependencies

`git-sync` requires [jsawk](https://github.com/micha/jsawk) (read the installation instructions there).

## Setup

1. Clone this repo: `git clone git@github.com:kflorence/git-sync.git`.
2. Put `git-sync` in your PATH (or: `sudo ln -s /path/to/bin/git-sync /usr/bin/git-sync`)
4. Create a file in the root of your repo called "sftp-config.json" (this is the same file used by [Sublime SFTP](http://wbond.net/sublime_packages/sftp)) and put this in it:

```json
{
   "host": "remote-hostname",
   "user": "your-username",
   "remote_path": "/path/to/remote/repo"
}
```

## Usage

Just run `git-sync` inside of a git repository that contains an "sftp-config.json" file. Optionally, you can also provide the path to a repo as an argument like: `git-sync /path/to/your/repo`.
