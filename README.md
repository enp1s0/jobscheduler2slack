# Job Scheduler Message >> Slack

## Installation

1. Clone this repository
```sh
git clone https://github.com/enp1s0/jobscheduler2slack.git
cd jobscheduler2slack
```

1. Get Webhook URL (See [Sending messages using Incoming Webhooks - Slack](https://api.slack.com/messaging/webhooks))

1. Set `WEBHOOK_URL` in post_message
```sh
WEBHOOK_URL=https://hooks.slack.com/services/...
```

1. Set `PATH` in your .bashrc or .zshrc or ...
```
export PATH=PATH:/path/to/jobscheduler2slack
```

## Usage

job_script.sh
```sh
#!/bin/sh
#$ ...
#$ ...

post_message "Start"

#./a.out
```

## Supported job scheduler
- UGE
- Slurm
- TORQUE
