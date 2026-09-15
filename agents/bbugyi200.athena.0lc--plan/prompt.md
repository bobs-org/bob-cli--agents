#gh:gh_bobs-org__bob-cli Can you help me start outputing these log messages from the `bob task-status-hooks` command to STDOUT instead of STDERR so I stop receiving these local emails (see the command output below for context)? My macbook has a cronjob configured that runs this command and redirects STDOUT to a log file. #plan
```
❯ mail
Mail version 8.1 6/6/93.  Type ? for help.
"/var/mail/bbugyi": 1 message 1 new
>N  1 bbugyi@Kellys-MacBoo  Tue Sep 15 12:00  19/1055  "Cron <bbugyi@Kellys-MacBook-Pro> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log"
? 1
Message 1:
From bbugyi@Kellys-MacBook-Pro.local  Tue Sep 15 12:00:09 2026
X-Original-To: bbugyi
Delivered-To: bbugyi@Kellys-MacBook-Pro.local
From: bbugyi@Kellys-MacBook-Pro.local (Cron Daemon)
To: bbugyi@Kellys-MacBook-Pro.local
Subject: Cron <bbugyi@Kellys-MacBook-Pro> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log
X-Cron-Env: <SHELL=/bin/sh>
X-Cron-Env: <PATH=/usr/bin:/bin>
X-Cron-Env: <LOGNAME=bbugyi>
X-Cron-Env: <USER=bbugyi>
Date: Tue, 15 Sep 2026 12:00:00 -0400 (EDT)

2026-09-15T12:00:00 bob task-status-hooks: retry run=18d589db02612038-b1b8-0 attempt=1 elapsed=0.001s reason=lock_contention delay=1.269s error="another Bob vault maintenance run is already active; rerun later"
2026-09-15T12:00:09 bob task-status-hooks: retry run=18d589db02612038-b1b8-0 succeeded attempts=2 elapsed=8.913s

? Saved 1 message in mbox
```