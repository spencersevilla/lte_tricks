# lte_tricks
Repo full of common scripts and systemd services I end up needing

start.sh/stop.sh:
These scripts start or stop open5gs control plane components.

cycling_tcpdump.crontab:
Install this script in crontab (as root) and it captures all control traffic (not data plane) into a nice set of organized tcpdump files. Important variables are as follows:
-G 14400 restarts the script every 14400 seconds (4 hours)
-w /root/tcpdump/ is the directory these files are saved into. Make sure it already exists and that you can write to it
-24 means that this script only keeps the most recent 24 files. This is four days worth of traffic, assuming 4hour chunks as above.


