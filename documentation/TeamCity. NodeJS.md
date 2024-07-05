from:: 
url:: [Node.js | TeamCity On-Premises Documentation](https://www.jetbrains.com/help/teamcity/nodejs.html)
on:: 2024-07-05 10:19

The `nodeJS` build runner allows to run `node`, `npm` and `yarn` steps. It runs in a container, the image used is `node:lts` by default, but can be overridden, or just detected from the project's `.npmrc` file. Some test frameworks used in `package.json` can also be auto-detected (ESLint, Jest, and Mocha are supported), so when creating the configuration from the UI, TeamCity will propose to create respective steps.

The shell script to execute may be anything, actually (but it's assumed you run `npm`, `node` or `yarn`), and this script will be executed inside this container.

If the npm registry is configured and respective build feature is added, then this registry will be available for the npm command inside the shell script. As an alternative, you can add a token to an environment variable, e.g., `NPM_TOKEN`, and specify it in the project's `.npmrc` file as: `//registry.npmjs.org/:_authToken=${NPM_TOKEN}`. In theory, the configured registry should override the `.npmrc` file, but due to a known issue it doesn't always work.