# Obsidian Git

> [!NOTE]+ Notes on this note
> Just copy and paste to `.obsidian/plugins/obsidian-git/data.json`
> Then change the hostname



**data.json**


```json
{
  "commitMessage": "{{hostname}}: {{date}}",
  "commitDateFormat": "YYYY.MMM.DD hh:mm A",
  "autoSaveInterval": 90,
  "autoPushInterval": 0,
  "autoPullInterval": 0,
  "autoPullOnBoot": false,
  "disablePush": false,
  "pullBeforePush": true,
  "disablePopups": false,
  "listChangedFilesInMessageBody": true,
  "showStatusBar": true,
  "updateSubmodules": false,
  "syncMethod": "merge",
  "customMessageOnAutoBackup": false,
  "autoBackupAfterFileChange": false,
  "treeStructure": false,
  "refreshSourceControl": true,
  "basePath": "",
  "differentIntervalCommitAndPush": false,
  "changedFilesInStatusBar": false,
  "showedMobileNotice": true,
  "refreshSourceControlTimer": 7000,
  "showBranchStatusBar": true,
  "setLastSaveToLastCommit": false,
  "submoduleRecurseCheckout": false,
  "gitDir": "",
  "showFileMenu": true,
  "lineAuthor": {
    "show": false,
    "followMovement": "inactive",
    "authorDisplay": "initials",
    "showCommitHash": false,
    "dateTimeFormatOptions": "date",
    "dateTimeFormatCustomString": "YYYY-MM-DD HH:mm",
    "dateTimeTimezone": "viewer-local",
    "coloringMaxAge": "1y",
    "colorNew": {
      "r": 255,
      "g": 150,
      "b": 150
    },
    "colorOld": {
      "r": 120,
      "g": 160,
      "b": 255
    },
    "textColorCss": "var(--text-muted)",
    "ignoreWhitespace": false,
    "gutterSpacingFallbackLength": 5,
    "lastShownAuthorDisplay": "initials",
    "lastShownDateTimeFormatOptions": "date"
  },
  "autoCommitMessage": "{{hostname}}: {{date}}"
}
```