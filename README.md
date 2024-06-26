# GitHub Docs <!-- omit in toc -->
[![Build GitHub Docs On Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new/?repo=github)

This repository contains the documentation website code and Markdown source files for [docs.github.com](https://docs.github.com).

GitHub's Docs team works on pre-production content in a private repo that regularly syncs with this public repo.

Use the table of contents icon <img alt="Table of contents icon" src="./contributing/images/table-of-contents.png" width="25" height="25" /> on the top right corner of this document to navigate to a specific section quickly.

## Contributing

We accept different types of contributions, including some that don't require you to write a single line of code. For detailed instructions on how to get started with our project, see "[About contributing to GitHub Docs](https://docs.github.com/en/contributing/collaborating-on-github-docs/about-contributing-to-github-docs)."

### Ways to contribute

On the GitHub Docs site, you can contribute by clicking the **Make a contribution** button at the bottom of the page to open a pull request for quick fixes like typos, updates, or link fixes.

You can also contribute by creating a local environment or opening a Codespace. For more information, see "[Setting up your environment to work on GitHub Docs](https://docs.github.com/en/contributing/setting-up-your-environment-to-work-on-github-docs)."

<img alt="Contribution call-to-action" src="./contributing/images/contribution_cta.png" width="400">

For more complex contributions, please open an issue using the most appropriate [issue template](https://github.com/github/docs/issues/new/choose) to describe the changes you'd like to see.

If you're looking for a way to contribute, you can scan through our [help wanted board](https://github.com/github/docs/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22) to find open issues already approved for work.

### And that's it!

If you're having trouble with your GitHub account, contact [Support](https://support.github.com).

That's how you can easily become a member of the GitHub Docs community. :sparkles:

## READMEs

In addition to the README you're reading right now, this repo includes other READMEs that describe the purpose of each subdirectory in more detail:

- [content/README.md](content/README.md)
- [content/graphql/README.md](content/graphql/README.md)
- [content/rest/README.md](content/rest/README.md)
- [contributing/README.md](contributing/README.md)
- [data/README.md](data/README.md)
- [data/reusables/README.md](data/reusables/README.md)
- [data/variables/README.md](data/variables/README.md)
- [src/README.md](src/README.md)

## License

The GitHub product documentation in the assets, content, and data folders are licensed under a [CC-BY license](LICENSE).

All other code in this repository is licensed under the [MIT license](LICENSE-CODE).

When using the GitHub logos, be sure to follow the [GitHub logo guidelines](https://github.com/logos).

## Thanks :purple_heart:

Thanks for all your contributions and efforts towards improving the GitHub documentation. We thank you for being part of our :sparkles: community :sparkles:!


Code of Conduct

I have read and agree to the code of conduct for the GitHub Docs project.

Which article on docs.github.com is affected?

For the endpoints and permissions specified in REST API endpoints for teams (https://docs.github.com/en/rest/teams/teams? apiVersion=2022-11-28#add-or-update-team-repository-permissions), they are not recorded on the following pages:

Https://docs.github.com/en/rest/authentication/endpoints-available-for-github-app-installation-access S-tokens? apiVersion=2022-11-28

Https://docs.github.com/en/rest/authentication/endpoints-available-for-github-app-user-access-tokens ? apiVersion=2022-11-28

Https://docs.github.com/en/rest/authentication/endpoints-available-for-fine-grained-personal-access- Tokens? apiVersion=2022-11-28

Https://docs.github.com/en/rest/authentication/permissions-required-for-github-apps? apiVersion=2022-11-28

Https://docs.github.com/en/rest/authentication/permissions-required-for-fine-grained-personal-access -Tokens? apiVersion=2022-11-28

For example, if you search (I guess it's old?) Including {team_slug} and some other endpoints:

/Orgs/{org}/teams/{team_slug}

/Orgs/{org}/teams/{team_slug}/projects

/Orgs/{org}/teams/{team_slug}/projects/{project_id}

/Orgs/{org}/teams/{team_slug}/repos

/Orgs/{org}/teams/{team_slug}/repos/{owner}/{repo}

/Orgs/{org}/teams/{team_slug}/teams

/User/teams

They don't appear on those pages.

What changes do you suggest?

Record them, because some of them use fine-grained personal access tokens, some don't use them, some use them with GitHub application installation access tokens, and some don't use them.

This is really confusing, because it is crucial that the ability to create repo and assign teams with admin permissions seems to be limited to PUT /orgs/{org}/teams/{team_slug}/repos/{owner}/{re Po} is obtained with personal access tokens (classic and fine-grained), but it is not available for GitHub applications installed in the organization, which seems to be a big gap and problem for organizations that restrict PAT access and want to automatically perform operations on GitHub through GitHub applications. .

In addition, using team_id to create a new repo only grants the team read access, which is useless (see: github/rest-api-description#3689).
