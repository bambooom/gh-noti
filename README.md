# gh-noti

Github CLI extension to check unread notifications in this [page](https://github.com/notifications).

As the feature is available in `gh`, see [this issue](https://github.com/cli/cli/issues/659).

Still WIP.

## Installation

```sh
gh extension install bambooom/gh-noti
```

Needs `jq` installed

```sh
brew install jq
```

## Usage

1. `gh noti` : list all unread notifications

```
ID          Repo                         Type         Title                                                                                                 Reason            Updated
-------     ------                       -------      ---------------                                                                                       ------            -------------------
2371625702  zzzzc/openresty-doc          PullRequest  fix markdown toc sidebar                                                                              author            2021-09-03T05:56:14Z
1209817679  mengxiong10/vue2-datepicker  Issue        Vue3 compatibility                                                                                    manual            2021-08-27T20:05:51Z
535892525   axios/axios                  Issue        Handling onUploadProgress on network failure                                                          manual            2021-07-27T07:15:54Z
```

Or no unread:

```
✨ No unread notifications.
```

2. `gh noti read`: mark all notifications as read

3. `gh noti read <id>`: use the id in the list to mark one thread as read

## Todo
- [x] mark all as read, https://docs.github.com/en/rest/reference/activity#mark-notifications-as-read
- [x] mark one as read by id, https://docs.github.com/en/rest/reference/activity#mark-a-thread-as-read
- [ ] open a unread notification thread url

## Ref
* [GitHub CLI 2.0 includes extensions! | The GitHub Blog](https://github.blog/2021-08-24-github-cli-2-0-includes-extensions/)
* [Creating GitHub CLI extensions - GitHub Docs](https://docs.github.com/en/github-cli/github-cli/creating-github-cli-extensions)
* no API for marking a notification as 'Done' status as it seems relatively new and maybe changed later, see https://github.community/t/no-api-command-for-new-done-state-of-notifications/122508
