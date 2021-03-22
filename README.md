# Bash Shell Wrapper For Github Search

Allows you to retrieve all the search results for a search query
using Github API v4, their GraphQL API.

# How to use it

You have to put in the organization as a separate argument. Otherwise
any valid GitHub search query should work.

For instance:

    bin/repo_search '10 days ago' 'now' 'my-organization' 'archived:false is:internal is:private'

Would build a `result.json` file in the `./opt/data/facts` directory,
which lists all of the repos merged since 10 days ago using the raw
JSON returned by the [GitHub GraphQL API](https://docs.github.com/en/graphql/overview/about-the-graphql-api).

## Limitations

1. Only has been tested on private repos.
