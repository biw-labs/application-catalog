# Host Metrics

This stack deploys the Telegraf agent to the host machine to collect metrics.
Telegraf will collect host level metrics such as:
* CPU
* Disk
* Memory

Additionally, Telegraf will attach to the Docker socket and provided container level metrics.
