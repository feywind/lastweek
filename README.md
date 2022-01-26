# lastweek

Given a username and/or GitHub access token, this tool will provide a report
of the work done by the user last week. This can be useful for sharing with
your coworkers, or just for your own notes.

## Installing / Quick Start

```
go install github.com/crwilcox/lastweek@latest

export GITHUB_TOKEN=your-token
lastweek
```

## Usage

Token and User can be provided via environment variables. Note, User can be
inferred from your GITHUB_TOKEN. Setting a token is recommended as it avoids
rate limiting issue as well as gives information about private repository
activity.

```
export GITHUB_USERNAME=your-username
export GITHUB_TOKEN=your-token
```

They can also be provided by flag, along with other settings.

```
Usage of lastweek:
  -end_date string
        The end date in ISO layout. E.g. YYYY-MM-DD
  -start_date string
        The start date in ISO layout. E.g. YYYY-MM-DD
  -start_of_week string
        The first day of your snippet week (default "Saturday")
  -token string
        Your GitHub access token.
  -user string
        Your GitHub username.
  -weeks_back int
        The number of weeks ago to see snippets for (default 1)
```


## Acknowledgments

I have written various versions of this tool. This most recent rewrite though was
influenced by a version I stumbled on by [RJPercival](https://github.com/rjpercival)
that had went out of date (though had some ideas I liked) as well as another
by [SethVargo](https://github.com/sethvargo) which had a way of formatting the
output I preferred to my previous ways. In combining these various elements of
each along with elements of previous iterations of my own, I created `lastweek`.
