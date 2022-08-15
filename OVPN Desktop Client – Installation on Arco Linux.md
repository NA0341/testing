# OVPN Desktop Client  –  Installation on Arco Linux


**Bela. Kroll (NA0341)**  
`na0341-dev@posteo.org`


date: 2022-08-15 17:54:15  
exec: OVPN-linux-6-2.2.0.4662.run

system:

```
OS: ArcoLinux
Host: HP EliteBook 8540p
Kernel: 5.15.55-2-lts
Uptime: 46 mins
Packages: 1765 (pacman)
Shell: zsh 5.9
CPU: Intel i5 M 540 (2) @ 2.534GHz
GPU: NVIDIA NVS 5100M
Memory: 2335MiB / 5789MiB (40%)
GPU Driver: Hewlett-Packard Company
```


## Installation


### Installer – Shell Output


Running without `sudo` gave an error which says sudo is not installed (this is to be expected because we're runnung on a completely different system and therefore paths may not be the same).

```
na0341@ArcoLinuxHP-EliteBook-8540p  ~/.run  sudo ./OVPN-linux-6-2.2.0.4662.run
[sudo] password for na0341: 
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
[107] Warning: QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
[353481] Warning: QXcbConnection: XCB error: 3 (BadWindow), sequence: 6741, resource id: 8441581, major code: 40 (TranslateCoords), minor code: 0
```


### Installer – Error message


> One or several required packages were not installed.  
> See /tmp/OVPN-missing-packages.log for details or contact support@ovpn.com for more information.

> The following packages were not found:  
> net-tools  
> resolvconf  
> libsecret-common  
> libsecret-1-0  
> libpam-gnome-keyring  
> arptables  
> libcurl4-openssl-dev  
> iproute2  
> iptables  
> libopengl0



### Error message – Information on local packages


```
net-tools
local: net-tools 2.10-1

/usr/bin/arp
/usr/bin/ifconfig
/usr/bin/ipmaddr
/usr/bin/iptunnel
/usr/bin/mii-tool
/usr/bin/nameif
/usr/bin/netstat
/usr/bin/plipconfig
/usr/bin/rarp
/usr/bin/route
/usr/bin/slattach
/usr/share/man/man5/ethers.5.gz
/usr/share/man/man8/arp.8.gz
[...]
/usr/share/man/man8/slattach.8.gz
```
---

```
resolvconf
local: openresolv 3.12.0-1

/etc/resolvconf.conf
/usr/bin/resolvconf
/usr/lib/resolvconf/dnsmasq
/usr/lib/resolvconf/libc
/usr/lib/resolvconf/libc.d/avahi-daemon
/usr/lib/resolvconf/libc.d/mdnsd
/usr/lib/resolvconf/named
/usr/lib/resolvconf/pdns_recursor
/usr/lib/resolvconf/pdnsd
/usr/lib/resolvconf/unbound
/usr/share/licenses/openresolv/LICENSE
/usr/share/man/man5/resolvconf.conf.5.gz
/usr/share/man/man8/resolvconf.8.gz
```
---

```
libsecret-common
local: libsecret 0.20.5-2

/usr/bin/secret-tool
/usr/include/libsecret-1/libsecret/secret-attributes.h
/usr/include/libsecret-1/libsecret/secret-backend.h
/usr/include/libsecret-1/libsecret/secret-collection.h
/usr/include/libsecret-1/libsecret/secret-enum-types.h
/usr/include/libsecret-1/libsecret/secret-item.h
/usr/include/libsecret-1/libsecret/secret-password.h
/usr/include/libsecret-1/libsecret/secret-paths.h
/usr/include/libsecret-1/libsecret/secret-prompt.h
/usr/include/libsecret-1/libsecret/secret-retrievable.h
/usr/include/libsecret-1/libsecret/secret-schema.h
/usr/include/libsecret-1/libsecret/secret-schemas.h
/usr/include/libsecret-1/libsecret/secret-service.h
/usr/include/libsecret-1/libsecret/secret-types.h
/usr/include/libsecret-1/libsecret/secret-value.h
/usr/include/libsecret-1/libsecret/secret-version.h
/usr/include/libsecret-1/libsecret/secret.h
/usr/lib/girepository-1.0/Secret-1.typelib
/usr/lib/libsecret-1.so
/usr/lib/libsecret-1.so.0
/usr/lib/libsecret-1.so.0.0.0
/usr/lib/pkgconfig/libsecret-1.pc
/usr/lib/pkgconfig/libsecret-unstable.pc
/usr/share/gir-1.0/Secret-1.gir
/usr/share/locale/ab/LC_MESSAGES/libsecret.mo
[...]
/usr/share/locale/zh_TW/LC_MESSAGES/libsecret.mo
/usr/share/man/man1/secret-tool.1.gz
/usr/share/vala/vapi/libsecret-1.deps
/usr/share/vala/vapi/libsecret-1.vapi
```

---

```
libsecret-1-0
local: not available

only libsecret available (the one above)
```

---

```
libpam-gnome-keyring
local: not available

only gnome-keyring & libgnome-keyring
pam is installed
```

---

```
arptables
local: not installed

available: arptables (AUR)
```

---

```
libcurl4-openssl-dev
local: not available

available: libcurl-openssl-1.0 (AUR)
```

---

```
iproute2
local: iproute2 5.18.0-1

/etc/iproute2/bpf_pinning
/etc/iproute2/ematch_map
/etc/iproute2/group
/etc/iproute2/nl_protos
/etc/iproute2/rt_dsfield
/etc/iproute2/rt_protos
/etc/iproute2/rt_realms
/etc/iproute2/rt_scopes
/etc/iproute2/rt_tables
/usr/bin/arpd
/usr/bin/bridge
/usr/bin/ctstat
/usr/bin/dcb
/usr/bin/devlink
/usr/bin/genl
/usr/bin/ifstat
/usr/bin/ip
/usr/bin/lnstat
/usr/bin/nstat
/usr/bin/rdma
/usr/bin/routel
/usr/bin/rtacct
/usr/bin/rtmon
/usr/bin/rtstat
/usr/bin/ss
/usr/bin/tc
/usr/bin/tipc
/usr/bin/vdpa
/usr/include/iproute2/bpf_elf.h
/usr/include/libnetlink.h
/usr/lib/libnetlink.a
/usr/lib/tc/m_ipt.so
/usr/lib/tc/m_xt.so
/usr/lib/tc/q_atm.so
/usr/share/bash-completion/completions/devlink
/usr/share/bash-completion/completions/tc
/usr/share/man/man3/libnetlink.3.gz
/usr/share/man/man7/tc-hfsc.7.gz
/usr/share/man/man8/arpd.8.gz
[...]
/usr/share/man/man8/vdpa.8.gz
/usr/share/tc/experimental.dist
/usr/share/tc/normal.dist
/usr/share/tc/pareto.dist
/usr/share/tc/paretonormal.dist
```

---

```
iptables
local: iptables 1:1.8.8-1

/etc/ethertypes
/etc/iptables/empty.rules
/etc/iptables/ip6tables.rules
/etc/iptables/iptables.rules
/etc/iptables/simple_firewall.rules
/usr/bin/arptables-nft
/usr/bin/arptables-nft-restore
/usr/bin/arptables-nft-save
/usr/bin/ebtables-nft
/usr/bin/ebtables-nft-restore
/usr/bin/ebtables-nft-save
/usr/bin/ip6tables
/usr/bin/ip6tables-apply
/usr/bin/ip6tables-legacy
/usr/bin/ip6tables-legacy-restore
/usr/bin/ip6tables-legacy-save
/usr/bin/ip6tables-nft
/usr/bin/ip6tables-nft-restore
/usr/bin/ip6tables-nft-save
/usr/bin/ip6tables-restore
/usr/bin/ip6tables-restore-translate
/usr/bin/ip6tables-save
/usr/bin/ip6tables-translate
/usr/bin/iptables
/usr/bin/iptables-apply
/usr/bin/iptables-legacy
/usr/bin/iptables-legacy-restore
/usr/bin/iptables-legacy-save
/usr/bin/iptables-nft
/usr/bin/iptables-nft-restore
/usr/bin/iptables-nft-save
/usr/bin/iptables-restore
/usr/bin/iptables-restore-translate
/usr/bin/iptables-save
/usr/bin/iptables-translate
/usr/bin/iptables-xml
/usr/bin/nfbpf_compile
/usr/bin/nfnl_osf
/usr/bin/xtables-legacy-multi
/usr/bin/xtables-monitor
/usr/bin/xtables-nft-multi
/usr/include/libipq.h
/usr/include/libiptc/ipt_kernel_headers.h
/usr/include/libiptc/libip6tc.h
/usr/include/libiptc/libiptc.h
/usr/include/libiptc/libxtc.h
/usr/include/libiptc/xtcshared.h
/usr/include/xtables-version.h
/usr/include/xtables.h
/usr/lib/libip4tc.so
/usr/lib/libip4tc.so.2
/usr/lib/libip4tc.so.2.0.0
/usr/lib/libip6tc.so
/usr/lib/libip6tc.so.2
/usr/lib/libip6tc.so.2.0.0
/usr/lib/libipq.so
/usr/lib/libipq.so.0
/usr/lib/libipq.so.0.0.0
/usr/lib/libxtables.so
/usr/lib/libxtables.so.12
/usr/lib/libxtables.so.12.6.0
/usr/lib/pkgconfig/libip4tc.pc
/usr/lib/pkgconfig/libip6tc.pc
/usr/lib/pkgconfig/libipq.pc
/usr/lib/pkgconfig/libiptc.pc
/usr/lib/pkgconfig/xtables.pc
/usr/lib/systemd/scripts/iptables-flush
/usr/lib/systemd/system/ip6tables.service
/usr/lib/systemd/system/iptables.service
/usr/lib/xtables/libarpt_mangle.so
/usr/lib/xtables/libebt_802_3.so
/usr/lib/xtables/libebt_among.so
/usr/lib/xtables/libebt_arp.so
/usr/lib/xtables/libebt_arpreply.so
/usr/lib/xtables/libebt_dnat.so
/usr/lib/xtables/libebt_ip.so
/usr/lib/xtables/libebt_ip6.so
/usr/lib/xtables/libebt_log.so
/usr/lib/xtables/libebt_mark.so
/usr/lib/xtables/libebt_mark_m.so
/usr/lib/xtables/libebt_nflog.so
/usr/lib/xtables/libebt_pkttype.so
/usr/lib/xtables/libebt_redirect.so
/usr/lib/xtables/libebt_snat.so
/usr/lib/xtables/libebt_stp.so
/usr/lib/xtables/libebt_vlan.so
/usr/lib/xtables/libip6t_DNPT.so
/usr/lib/xtables/libip6t_HL.so
/usr/lib/xtables/libip6t_LOG.so
/usr/lib/xtables/libip6t_MASQUERADE.so
/usr/lib/xtables/libip6t_NETMAP.so
/usr/lib/xtables/libip6t_REJECT.so
/usr/lib/xtables/libip6t_SNAT.so
/usr/lib/xtables/libip6t_SNPT.so
/usr/lib/xtables/libip6t_ah.so
/usr/lib/xtables/libip6t_dst.so
/usr/lib/xtables/libip6t_eui64.so
/usr/lib/xtables/libip6t_frag.so
/usr/lib/xtables/libip6t_hbh.so
/usr/lib/xtables/libip6t_hl.so
/usr/lib/xtables/libip6t_icmp6.so
/usr/lib/xtables/libip6t_ipv6header.so
/usr/lib/xtables/libip6t_mh.so
/usr/lib/xtables/libip6t_rt.so
/usr/lib/xtables/libip6t_srh.so
/usr/lib/xtables/libipt_CLUSTERIP.so
/usr/lib/xtables/libipt_ECN.so
/usr/lib/xtables/libipt_LOG.so
/usr/lib/xtables/libipt_MASQUERADE.so
/usr/lib/xtables/libipt_NETMAP.so
/usr/lib/xtables/libipt_REJECT.so
/usr/lib/xtables/libipt_SNAT.so
/usr/lib/xtables/libipt_TTL.so
/usr/lib/xtables/libipt_ULOG.so
/usr/lib/xtables/libipt_ah.so
/usr/lib/xtables/libipt_icmp.so
/usr/lib/xtables/libipt_realm.so
/usr/lib/xtables/libipt_ttl.so
/usr/lib/xtables/libxt_AUDIT.so
/usr/lib/xtables/libxt_CHECKSUM.so
/usr/lib/xtables/libxt_CLASSIFY.so
/usr/lib/xtables/libxt_CONNMARK.so
/usr/lib/xtables/libxt_CONNSECMARK.so
/usr/lib/xtables/libxt_CT.so
/usr/lib/xtables/libxt_DNAT.so
/usr/lib/xtables/libxt_DSCP.so
/usr/lib/xtables/libxt_HMARK.so
/usr/lib/xtables/libxt_IDLETIMER.so
/usr/lib/xtables/libxt_LED.so
/usr/lib/xtables/libxt_MARK.so
/usr/lib/xtables/libxt_NFLOG.so
/usr/lib/xtables/libxt_NFQUEUE.so
/usr/lib/xtables/libxt_NOTRACK.so
/usr/lib/xtables/libxt_RATEEST.so
/usr/lib/xtables/libxt_REDIRECT.so
/usr/lib/xtables/libxt_SECMARK.so
/usr/lib/xtables/libxt_SET.so
/usr/lib/xtables/libxt_SYNPROXY.so
/usr/lib/xtables/libxt_TCPMSS.so
/usr/lib/xtables/libxt_TCPOPTSTRIP.so
/usr/lib/xtables/libxt_TEE.so
/usr/lib/xtables/libxt_TOS.so
/usr/lib/xtables/libxt_TPROXY.so
/usr/lib/xtables/libxt_TRACE.so
/usr/lib/xtables/libxt_addrtype.so
/usr/lib/xtables/libxt_bpf.so
/usr/lib/xtables/libxt_cgroup.so
/usr/lib/xtables/libxt_cluster.so
/usr/lib/xtables/libxt_comment.so
/usr/lib/xtables/libxt_connbytes.so
/usr/lib/xtables/libxt_connlabel.so
/usr/lib/xtables/libxt_connlimit.so
/usr/lib/xtables/libxt_connmark.so
/usr/lib/xtables/libxt_conntrack.so
/usr/lib/xtables/libxt_cpu.so
/usr/lib/xtables/libxt_dccp.so
/usr/lib/xtables/libxt_devgroup.so
/usr/lib/xtables/libxt_dscp.so
/usr/lib/xtables/libxt_ecn.so
/usr/lib/xtables/libxt_esp.so
/usr/lib/xtables/libxt_hashlimit.so
/usr/lib/xtables/libxt_helper.so
/usr/lib/xtables/libxt_ipcomp.so
/usr/lib/xtables/libxt_iprange.so
/usr/lib/xtables/libxt_ipvs.so
/usr/lib/xtables/libxt_length.so
/usr/lib/xtables/libxt_limit.so
/usr/lib/xtables/libxt_mac.so
/usr/lib/xtables/libxt_mark.so
/usr/lib/xtables/libxt_multiport.so
/usr/lib/xtables/libxt_nfacct.so
/usr/lib/xtables/libxt_osf.so
/usr/lib/xtables/libxt_owner.so
/usr/lib/xtables/libxt_physdev.so
/usr/lib/xtables/libxt_pkttype.so
/usr/lib/xtables/libxt_policy.so
/usr/lib/xtables/libxt_quota.so
/usr/lib/xtables/libxt_rateest.so
/usr/lib/xtables/libxt_recent.so
/usr/lib/xtables/libxt_rpfilter.so
/usr/lib/xtables/libxt_sctp.so
/usr/lib/xtables/libxt_set.so
/usr/lib/xtables/libxt_socket.so
/usr/lib/xtables/libxt_standard.so
/usr/lib/xtables/libxt_state.so
/usr/lib/xtables/libxt_statistic.so
/usr/lib/xtables/libxt_string.so
/usr/lib/xtables/libxt_tcp.so
/usr/lib/xtables/libxt_tcpmss.so
/usr/lib/xtables/libxt_time.so
/usr/lib/xtables/libxt_tos.so
/usr/lib/xtables/libxt_u32.so
/usr/lib/xtables/libxt_udp.so
/usr/share/iptables/empty-filter.rules
/usr/share/iptables/empty-mangle.rules
/usr/share/iptables/empty-nat.rules
/usr/share/iptables/empty-raw.rules
/usr/share/iptables/empty-security.rules
/usr/share/iptables/empty.rules
/usr/share/iptables/simple_firewall.rules
/usr/share/man/man1/iptables-xml.1.gz
/usr/share/man/man3/ipq_create_handle.3.gz
[...]
/usr/share/man/man3/libipq.3.gz
/usr/share/man/man8/arptables-nft-restore.8.gz
[...]
/usr/share/man/man8/xtables-translate.8.gz
/usr/share/xtables/pf.os
```

---

```
libopengl0
local: not available
```


## Execution


### OVPN Desktop – Shell Output


The Client gives an inacurate error message:

> OVPN.com is experiencing issues. Limited functionality in client.

According to the missing packages - it's much more likely that the client isn't able to establish a proper connection because of the missing packages/libraries.


```
 na0341@ArcoLinuxHP-EliteBook-8540p  /opt/OVPN  ./OVPN
>>> :  "/home/na0341/.local/share/OVPN_coredumps"
>>> :  "./crashpad_handler"
>>> :  "https://7221b38b412440a6a01b1496b8ca286c@sentry.ovpn.se/37"
System name: Linux
Nodename:ArcoLinuxHP-EliteBook-8540p
Release:5.15.55-2-lts
Version:#1 SMP Fri, 22 Jul 2022 23:29:06 +0000
Machine:x86_64
[sentry] INFO using database path "/home/na0341/.local/share/OVPN_coredumps"
[sentry] DEBUG starting transport
[sentry] DEBUG starting background worker thread
[sentry] DEBUG starting backend
MachineGUID = 29218d27c3bc4ca7913225e9d2a7f47a 
[sentry] DEBUG background worker thread started
static bool LibSecretKeyring::findPassword(const QString&, const QString&, QKeychain::JobPrivate*)
Keychain: Restoring data failed for account "https://www.ovpn.com", error text: Entry not found
[6408:6408:0815/202243.351497:ERROR:gbm_wrapper.cc(292)] Failed to export buffer to dma_buf: No such file or directory (2)
[...]
Opening in existing browser session.
[sentry] DEBUG sending envelope
[sentry] DEBUG submitting task to background worker thread
[sentry] DEBUG shutting down backend
[sentry] DEBUG executing task on worker thread
[sentry] DEBUG shutting down transport
[sentry] DEBUG shutting down background worker thread
[sentry] DEBUG submitting task to background worker thread
* Could not resolve host: sentry.ovpn.se
[sentry] WARN sending via `curl_easy_perform` failed with code `6`
[sentry] DEBUG executing task on worker thread
[sentry] DEBUG background worker thread shut down
```
