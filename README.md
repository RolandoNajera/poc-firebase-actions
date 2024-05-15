Local configuration

To configure github actions in Firebase only requires to run commands as described in [official documentation](https://firebase.google.com/docs/hosting/github-integration):

For the new Firebase setup run the following and select the github actions option:

```
firebase init hosting
```

If already firebase created, we can add github actions with the following command:

```bash
firebase init hosting:github
```

For more details about the Firebase github actions, see the [official github repo](https://github.com/marketplace/actions/deploy-to-firebase-hosting).

## Github configuration

Could be important to shadow the project ID as a secret, to do that we can add this property as a secret in Repository -\> settings -\> secrets and variables -\> Actions -\> Repository secrets

## Configuring deployment in two different environments

To configure two projects in the same workspace is used the command:

```bash
firebase use --add
```

This command is important to achieve the deployment in two different environments at the same time.

# References

This article was part of the spike task HUTADE-2 to understand how the projects, environments and github actions work, all code and POC are located at the github repository [hutade/poc-firebase-actions](https://github.com/hutade/poc-firebase-actions)

[GitHub actions for Firebase deploy](https://github.com/marketplace/actions/deploy-to-firebase-hosting)

[Handle Firebase environments blog](https://firebase.blog/posts/2016/07/deploy-to-multiple-environments-with)

Git flows

[Trunk based development](https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development)
