# Job Scheduler Message >> Slack

## Installation

1. Clone this repository
```sh
git clone https://github.com/enp1s0/jobscheduler2slack.git
cd jobscheduler2slack
```

2. Get Webhook URL (See [Sending messages using Incoming Webhooks - Slack](https://api.slack.com/messaging/webhooks))

3. Set `WEBHOOK_URL` in post_message
```sh
WEBHOOK_URL=https://hooks.slack.com/services/...
```


## Usage

job_script.sh
```sh
#!/bin/sh
#$ ...
#$ ...
export PATH=$PATH:/path/to/jobscheduler2slack

post_message "Hello!"

#./a.out
```

&gt;&gt;
```
Hello! [JobName:j2s-test (JobID:6528295) @r5i0n5]
```

## Supported job scheduler
- UGE (TSUBAME 3.0, ABCI and so on)
- Slurm (TSUBAME KFC and so on)
- TORQUE/OpenPBS
- Fujutsu Job Scheduler (`pjsub`) (Fugaku and so on)
- vico (https://github.com/enp1s0/vico)
