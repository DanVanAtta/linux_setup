#!/bin/bash

LINE_COUNT=$(cat /etc/hosts | wc -l)
if [ "$LINE_COUNT" -gt 100 ]; then
  echo "Skipping, /etc/host file looks to already be updated with $LINE_COUNT lines"
  exit
fi

wget https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts
sudo cp /etc/hosts /etc/hosts.backup
cat hosts | sudo tee -a /etc/hosts > /dev/null
rm hosts
