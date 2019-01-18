# bbr-ac
BBR with Actual Congestion

## Introduction

BBR with Actual Congestion (BBR-AC) is a implementation of *a*STEAM Project <https://asteam.korea.ac.kr>. 
Bottleneck Bandwidth and Round-trip time (BBR), a congestion control algorithm proposed by Google that converges to Kleinrock’s optimal operating point for the first time. It claims to provide higher throughput with less end-to-end delay. However, many researches and Google itself has observed twice increase in retransmissions by BBR as compared to CUBIC. In this work, we focus on this retransmission problem in BBR and propose a solution.

## Requirements and Dependencies

* Please access `include/net/inet_connection_socket.h` and set `ICSK_CA_PRIV_SIZE` to `12 * sizeof(u64)`.
* Above development was based on the Linux version of 4.14.64+.

## Instructions

* How to Run
  1. Just replace the existing `tcp_bbr.c` in `/usr/src/.../net/ipv4/`.
  2. `make` and `make install` for the directory.
  3. `reboot` the system.
  4. Change the default Congestion Algorithm to *bbr*

