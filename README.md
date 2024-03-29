# Job Scheduler Message >> Slack

## Installation

1. Clone this repository
```sh
git clone https://github.com/enp1s0/jobscheduler2slack.git
cd jobscheduler2slack
```

2. Get Webhook URL (See [Sending messages using Incoming Webhooks - Slack](https://api.slack.com/messaging/webhooks))

3. Set `WEBHOOK_URL` in `$HOME/.js2slack.conf`
```sh
echo 'WEBHOOK_URL=https://hooks.slack.com/services/...' > $HOME/.js2slack.conf
chmod 600 $HOME/.js2slack.conf
```

> **Note**
> If you want to put the config file somewhere other than the home directory, put it anywhere and set the environment variable `$JS2SLACK_CONFIG`.


## Usage

job_script.sh
```sh
#!/bin/sh
#$ ...
#$ ...
export PATH=$PATH:/path/to/jobscheduler2slack/bin

js2slack_post "Hello!"

#./a.out
```

&gt;&gt;
```
Hello! [JobName:j2s-test (JobID:6528295) @r5i0n5]
```

## Supported job scheduler
- UGE (TSUBAME 3.0, ABCI, etc)
- Slurm (TSUBAME KFC, etc)
- TORQUE/OpenPBS
- Fujutsu Job Scheduler (`pjsub`) (Fugaku, etc)
- vico (https://github.com/enp1s0/vico)
