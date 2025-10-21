# Private Makefile

This makefile that executes various tasks in a Salesforce project.

## Branch Structure

We are assuming a project that will proceed with the branch separation method shown below.

| Branch Name | Variable           | Default Structure              |
| :---------- | :----------------- | :----------------------------- |
| main        | GIT_DEFAULT_BRANCH | main                           |
| release     | GIT_RELEASE_BRANCH | release/[Release Version Name] |

You can change the configuration by modifying the corresponding variables.

## Available Commands

| Command  | Usage                                                                                                                                               |
| :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| help     | Explain how to use it.                                                                                                                              |
| update   | Update the Salesforce CLI and related plugins.                                                                                                      |
| delta    | Specify the VERSION and create a package based on the differences between "origin/main" and "origin/release/[VERSION]".                             |
| deploy   | Specify the VERSION and ALIAS, and deploy the package based on the delta command to the environment specified by ALIAS.                             |
| validate | Specify the VERSION and ALIAS, and perform a deployment validation of the package based on the delta command to the environment specified by ALIAS. |

### help Commands

It will be written in the format shown below.

```sh
make help
```

### update Commands

It will be written in the format shown below.

```sh
make update
```

### delta Commands

It will be written in the format shown below.

```sh
make delta VERSION=[VERSION NAME]
```

### deploy Commands

It will be written in the format shown below.

```sh
make deploy AILIAS=[AILIAS NAME] VERSION=[VERSION NAME]
```

### validate Commands

It will be written in the format shown below.

```sh
make validate AILIAS=[AILIAS NAME] VERSION=[VERSION NAME]
```
