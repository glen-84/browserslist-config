# Browserslist config

The GosuGamers [Browserslist](https://github.com/browserslist/browserslist) config.

## Installation

You will need to set an environment variable named `GG_GITLAB_NPM_TOKEN` with the value of a [personal access token](https://gitlab.com/-/profile/personal_access_tokens) (name: `npm`, scopes: `api`), in order to install private packages with the `@gosugamers` scope (if you haven't yet done so).

1. In the same directory as your `package.json` file, create or edit a `.npmrc` file to include the following lines:
    ```npmrc
    @gosugamers:registry=https://gitlab.com/api/v4/packages/npm/
    //gitlab.com/api/v4/packages/npm/:_authToken=${GG_GITLAB_NPM_TOKEN}
    ```
2. Run `npm install @gosugamers/browserslist-config --save-dev`.
3. Add `"browserslist": ["extends @gosugamers/browserslist-config"]` to your `package.json` file.

## Development

This project is effectively a clone of [@glen-84/browserslist-config](https://github.com/glen-84/browserslist-config) with a few changes for GosuGamers.

### Pulling updates from the source

1. Run `git remote add upstream https://github.com/glen-84/browserslist-config.git` (if you haven't yet done so).
2. Run `git pull upstream master`.

### Publishing the current version

1. Ensure that the `GG_GITLAB_NPM_TOKEN` environment variable is set (see above).
2. Run `npm publish` to publish the current version.
