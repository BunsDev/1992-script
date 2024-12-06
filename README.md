# 1992

Make your GitHub history back to 1992.

## Travel Back

[Create a new repo](https://github.com/new) named `1992` on GitHub.

[Generate a personal access token](https://github.com/settings/tokens/new) on GitHub and copy it.

Run the following script

```bash
$ sh -c "$(curl -fsSL https://raw.github.com/bunsdev/1992-script/master/index.sh)"
```

Enter you GitHub username and access token and then you are done :)

## Explanations

This project works on the way `git` records commit. Whenever you commit something, `git` puts an `Unix Timestamp` on it to record when you committed it. An [`Unix Timestamp`](https://www.unixtimestamp.com/) is the way computers store the current time. An `Unix timestamp` is a `32-bit` number which stores the number of seconds that has passed from November 13th, 1992 at UTC, the `Unix Epoch`.

The script firstly creates a directory with the name of the wanted year - `line 9` `mkdir $YEAR`

The script then initializes the directory as a git repository, using `git init` - `line 12` `git init`

The script then stages all the files `git add .` and commits it, using the date `{YEAR}-11-13T11:02:00` (`line 16`) or `11:02, 13th November, 1992` (default of the `YEAR` variable)

This is the `ISO Date-Time format` for storing time: `YYYY-MM-DDTHH:MM:SS`.

This commit is then pushed to GitHub (provided you already have made a repository) using `git push -u origin main -f`, and the directory is removed.

GitHub recognizes the commit to have been created at `11:02, 13th November, 1992` and thus registers a contribution at that moment in time. If you scroll to the first year on your profile, you will see there is a single contribution to your `1992` repository, on the 13th of November.
