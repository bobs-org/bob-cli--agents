#gh:gh_bobs-org__bob-cli I've got the `bob task-status-hooks` command set up to run as a cronjob on
my mac machine, but it seems to be aborting early often because it detects other
modifications being made to my Obsidian vault.

- It would be better if we used some retry strategy with a backoff policy of some sort
  to ensure this command almost always succeeds.
- If we need to retry we should log the output and that output should be stored to a log
  file not output by the cron job, which would cause me to get a local email (see the
  command output below for context).
- Also can you help me change the cronjob schedule / job configurations a bit if
  necessary/desirable to get these conflicts to stop occurring as much?

```
❯ mail
Mail version 8.1 6/6/93.  Type ? for help.
"/var/mail/bbugyi": 3 messages 3 new
>N  1 bbugyi@Kellys-MBP.lo  Mon Sep 14 07:45  18/797   "Cron <bbugyi@Kellys-MBP> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log"
 N  2 bbugyi@Kellys-MBP.lo  Mon Sep 14 08:45  18/797   "Cron <bbugyi@Kellys-MBP> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log"
 N  3 bbugyi@Kellys-MBP.lo  Mon Sep 14 09:15  18/797   "Cron <bbugyi@Kellys-MBP> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log"
? 1
Message 1:
From bbugyi@Kellys-MBP.localdomain  Mon Sep 14 07:45:03 2026
X-Original-To: bbugyi
Delivered-To: bbugyi@Kellys-MBP.localdomain
From: bbugyi@Kellys-MBP.localdomain (Cron Daemon)
To: bbugyi@Kellys-MBP.localdomain
Subject: Cron <bbugyi@Kellys-MBP> ~/.cargo/bin/bob task-status-hooks >> /var/tmp/bob_task_status_hooks.log
X-Cron-Env: <SHELL=/bin/sh>
X-Cron-Env: <PATH=/usr/bin:/bin>
X-Cron-Env: <LOGNAME=bbugyi>
X-Cron-Env: <USER=bbugyi>
Date: Mon, 14 Sep 2026 07:45:01 -0400 (EDT)

bob task-status-hooks: another Bob vault maintenance run is already active; rerun later

?
```

Can you help me fix these issues / make these improvements? #plan %m:gpt-6-astra