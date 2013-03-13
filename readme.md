# git-sync

`git-sync` allows you to easily synchronize a git repository to a remote location using `rsync` and `jsawk`.

## How to use

1. Clone this repo: `git clone git@github.com:kflorence/git-sync.git`.
2. Put `git-sync` in your PATH (or: `sudo ln -s /path/to/bin/git-sync /usr/bin/git-sync`)
3. [Install jsawk](https://github.com/micha/jsawk) (follow the instructions there).
4. Create a file in the root of your repo called "sftp-config.json" and put this in it:
   ```json
   {
       "host": "remote-hostname",
       "user": "your-username",
       "remote_path": "/path/to/remote/repo"
   }
   ```
5. Run git-sync inside of a repository, or pass the path to a repository as the first argument: `git-sync /path/to/repo`
