# Renovate

## Automerge

Renovates automerge is broken when using stability days, see https://github.com/renovatebot/renovate/issues/7800. The renovate PRs is instead merged automatically by the merge-renovate-prs.yml workflow. Note that _rebaseWhen_ must be set to _behind-base-branch_ in order to avoid broken lockfiles.

## Update GitHub Token

The token that Renovate uses for private packages are stored encrypted in the renovate.json file. 

To update the token you must: 
1. Generate a GitHub token with repo and read packes rights
1. go to https://app.renovatebot.com/encrypt
1. Insert the token as raw value, enter LKP-RnD as organization and vms-web-client as repo and encrypt
1. Replace the _npm.encrypted.npmToken_ value with the encrypted value