# gh-noti

Github CLI extension to check unread notifications in this [page](https://github.com/notifications).

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

```sh
gh noti
```

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

## Todo
- [ ] mark all as read
- [ ] mark one as read by id
