# ansible-role-rtpengine [![Build Status](https://secure.travis-ci.org/davehorton/ansible-role-rtpengine.png)](http://travis-ci.org/davehorton/ansible-role-rtpengine)

This is an ansible role for building rtpengine. 

## Role variables

Available variables are listed below, along with default values (see defaults/main.yml):
```
rtp_engine_version: master
```
branch to check out

```
rtp_engine_recording_dir: /tmp
```
directory into which to write files
```
rtp_engine_recording_method: pcap
```
type of files to write
```
rtp_engine_recording_format: eth
```
recording format
```
rtp_engine_udp_port: 12222
```
udp port
```
rtp_engine_NG_port: 22222
```
port to listen on for ng commands
```
rtp_engine_cli_port: 127.0.0.1:9900
```
cli port
```
rtp_engine_log_level: 6
```
log level
```
rtp_engine_min_port: 40000
rtp_engine_max_port: 60000
```
rtp port range
```
homer_protocol: udp
```
protocol to use for homer

```

## Example playbook
```
---
- hosts: all
  become: yes
  roles:
    - ansible-role-rtpengine
```
