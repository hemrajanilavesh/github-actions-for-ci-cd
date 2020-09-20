# Using Github Actions for CI-CD Workflow

[![Node.js CI](https://github.com/hemrajanilavesh/github-actions-for-ci-cd/workflows/Node.js%20CI/badge.svg?branch=master&event=push)](https://github.com/hemrajanilavesh/github-actions-for-ci-cd/actions?query=branch%3Amaster+is%3Acompleted)
[![codecov](https://codecov.io/gh/hemrajanilavesh/github-actions-for-ci-cd/branch/master/graph/badge.svg)](https://codecov.io/gh/hemrajanilavesh/github-actions-for-ci-cd)
[![Known Vulnerabilities](https://snyk.io/test/github/hemrajanilavesh/github-actions-for-ci-cd/badge.svg?targetFile=package.json)](https://snyk.io/test/github/hemrajanilavesh/github-actions-for-ci-cd?targetFile=package.json)

The repository contains a working example of Continuous Integration & Continuous Delivery of a Tic Tac Toe Web App.
 
## Workflow Contents

##### Workflow file can be found [here](https://github.com/hemrajanilavesh/github-actions-for-ci-cd/blob/master/.github/workflows/node.js.yml)

It will do the following:
1. Checkout repository 
2. Install Node dependencies 
3. Build the Source Code and Generate Artifact 
4. Run tests against different platforms using below matrix strategy:
    <table>
    <thead>
    <tr>
    <th>OS</th>
    <th>Node version 1</th>
    <th>Node version 2</th>
    </tr>
    </thead>
    <tbody>
    <tr><td>ubuntu-latest</td><td>12.x</td><td>14.x</td></tr>
    <tr><td>windows-2016</td><td>12.x</td><td>14.x</td></tr>
    </tbody>
    </table>
5. Generate Code Coverage Report and publish to https://codecov.io/    
6. Build Docker Image and publish to Github Registry 

##### Published Image can be found [here](https://github.com/hemrajanilavesh/github-actions-for-ci-cd/packages/404800)

## Actions Used in the Workflow

- [Checkout](https://github.com/actions/checkout)
- [Upload Artifact](https://github.com/actions/upload-artifact)
- [Download Artifact](https://github.com/actions/download-artifact)
- [Setup Node](https://github.com/actions/setup-node)
- [Docker Build Push](https://github.com/docker/build-push-action)
- [Codecov](https://github.com/marketplace/actions/codecov)

## References

[Building and Testing Node.js](https://docs.github.com/en/actions/guides/building-and-testing-nodejs)

[Github Learning Lab: Continuous Integration](https://lab.github.com/githubtraining/github-actions:-continuous-integration)

[Github Learning Lab: Publish to GitHub Packages](https://lab.github.com/githubtraining/github-actions:-publish-to-github-packages)
