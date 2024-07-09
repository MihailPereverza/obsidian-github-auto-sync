# GitHub Sync

Simple plugin that allows you to sync your vault to a personal GitHub repo for **syncing across devices**.

![](screenshots/ribbon-button.png)

## How to Use

1. When changes are made to md files and text input is stopped, the entire repository is automatically synchronized.
2. Click the **Sync with Remote** ribbon icon to pull changes from your GitHub repo and push local changes. 
If there are any conflicts, the unmerged files will be opened for you to resolve (or just push again with the unresolved conflicts - that's fine too).

## Setup
What you need:
- GitHub account
- GitHub [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens) from https://github.com/settings/tokens
- GitHub repo for your vault
- Git installed device

After installing the plugin, open the **GitHub Sync** section in Settings. Put in your GitHub username, personal access token, and the URL for your GitHub repo in the noted format. Make sure your PAT has control of private repos if your repo is private. That's it.

### Optional

If your git binary is not accessible from your system PATH (i.e. if you open up Command Prompt or Terminal and can't use git), you need to provide its location. I initialize git only when launching Cmder, so I need to input a custom path like so: `C:/Users/Kevin/scoop/apps/cmder-full/current/vendor/git-for-windows/cmd/git`.

I'm assuming your vault directory is already a Git repository, but if it's not you need to `git init` it first (make sure the default branch name matches what's on the GitHub repo e.g. main).

## Tasks for Features:

- ✅ Automatic synchronization when stopping file editing 
- ✅ Synchronization of installed plugins
- ⬜ Synchronization of Excalidraw files (Obsidian event "editor-change" does not work on them, a different synchronization mechanism is needed)
