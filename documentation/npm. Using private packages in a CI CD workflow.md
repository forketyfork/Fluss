from:: [[TeamCity. NodeJS]]
url:: [Using private packages in a CI/CD workflow | npm Docs](https://docs.npmjs.com/using-private-packages-in-a-ci-cd-workflow)
on:: 2024-07-05 11:27

You need to create an access token. A granular token is recommended, but the documentation describes the process for the legacy token:
```sh
npm token create # both read and publish permissions
npm token create --read-only # only read permissions
npm token create --cidr=192.0.2.0/24 # with CIDR whitelisting as to who can use this token
```

You can also create an automation token on the website that will allow to publish the artifact even if 2FA is enabled, but it's still considered legacy.

To use the token in CI, add it as a secret and put it into an environment variable, e.g., here's how to do it in in GitHub Actions:
```yaml
steps:
  - run: |
      npm install
  - env:
      NPM_TOKEN: ${{ secrets.NPM_TOKEN }}
```

Check in an `.npmrc` file to the root of your project that references this variable:
```
//registry.npmjs.org/:_authToken=${NPM_TOKEN}
```