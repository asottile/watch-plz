[![Build Status](https://github.com/asottile/watch-plz/workflows/main/badge.svg)](https://github.com/asottile/watch-plz/actions)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/asottile/watch-plz/master.svg)](https://results.pre-commit.ci/latest/github/asottile/watch-plz/master)

watch-plz
=========

Ensure all of your repositories are watched.

### why

- My current employer also uses github
- They have lots of repositories
- I don't want to watch all of the repositories
- So I uncheck the `Automatically watch repositories` setting
- I then forget to watch my own repositories

### usage

Grab a token [here](https://github.com/settings/tokens/new).
`public_repository` + `notifications` should be sufficient for this token --
though if you want to watch private repositories you'll need the full `repo`
permission.

Modify `DONT_WATCH` in the `watch-plz` script.

```bash
GH_TOKEN=... ./watch-plz --dry-run
```

### how I use it

I use [github actions scheduled builds] to run this periodically.

[github actions scheduled builds]: https://help.github.com/en/actions/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions#onschedule
