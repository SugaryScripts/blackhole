url:: [NVM Commands Cheatsheet – Duncan Leung](https://duncanleung.com/nvm-commands-cheatsheet)

## Install a Version of NodeJS

```text
$ nvm install <node_version>      // Install a specific version
$ nvm install --lts               // Install the latest LTS release
$ nvm install-latest-npm          // Install latest NPM release only
```

## List Available Releases

```text
$ nvm ls-remote
$ nvm ls-remote | grep -i "latest"
$ nvm ls-remote | grep -i "<node_version>"
```

## List Installed Versions

```text
$ nvm ls
```

## [](https://duncanleung.com/nvm-commands-cheatsheet/#switch-to-a-version)Switch to a Version

```text
$ nvm use <node_version_or_alias>  // Switch to a specific version
$ nvm use --lts                    // Switch to the latest LTS version
```

## [](https://duncanleung.com/nvm-commands-cheatsheet/#verifying-nodejs-version)Verifying NodeJS Version

```text
$ node -v
$ npm -v
$ nvm -v
```

## [](https://duncanleung.com/nvm-commands-cheatsheet/#default-to-a-nodejs-version-aliasing)Default to a NodeJS Version (Aliasing)

```text
$ nvm alias default <node_version>        // Sets the default version on a shell
$ nvm alias <alias_name> <node_version>   // Sets a user-defined alias to a versions 

$ nvm unalias <alias_name>                // Deletes the alias named <alias_name>
```

## [](https://duncanleung.com/nvm-commands-cheatsheet/#check-the-path-to-the-nodejs-executable)Check the Path to the NodeJS Executable

```text
$ nvm which <installed_node_version>      // Path to a specific executable
```

## Uninstall a Version of NodeJS

```text
$ nvm uninstall <node_version>    // Uninstall a specific version
$ nvm uninstall --lts             // Uninstall the latest LTS release
```