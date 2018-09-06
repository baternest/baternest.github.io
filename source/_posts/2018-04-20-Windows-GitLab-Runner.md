---
title: Windows GitLab Runner
date: 2018-04-20 14:00:34
categories:
tags:
---
[GitLab.org / gitlab-runner · GitLab](https://gitlab.com/gitlab-org/gitlab-runner)

[Install GitLab Runner on Windows](https://docs.gitlab.com/runner/install/windows.html)
[GitLab CI/CD Variables](https://docs.gitlab.com/ee/ci/variables/)

```
gitlab-runner install --user ".\ENTER-YOUR-USERNAME" --password "ENTER-YOUR-PASSWORD"
gitlab-runner start

gitlab-runner register --name zh-runner --url https://ubuntu:8081/gitlab/ --registration-token _8N7_mVwE25etMCvPLGX
gitlab-runner unregister --all-runners

gitlab-runner stop
gitlab-runner uninstall
```

[gitlab-runner register](https://docs.gitlab.com/runner/commands/README.html#gitlab-runner-register)

[GitLab Runner FAQ | GitLab ](https://docs.gitlab.com/runner/faq/#the-service-did-not-start-due-to-a-logon-failure-error-when-starting-service-on-windows)

* Manually using Administrative Tools:

    Go to Control Panel > System and Security > Administrative Tools,
    open the Local Security Policy tool,
    chose the Security Settings > Local Policies > User Rights Assignment on the list on the left,
    open the Log on as a service on the list on the right,
    click on the Add User or Group... button,
    add the user ("by hand" or using Advanced... button) and apply the settings.