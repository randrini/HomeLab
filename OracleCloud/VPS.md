### Setup the VPS

* create a new instance
  * select free tier compute
  * chose ubuntu

* create a new networking
  * set up a virtual cloud network
  * change VCN and VNIC name

* set up a security list
  * add a new ingressrule
      * source: 0.0.0.0/0
      * protocol: TCP
      * destination port range: 22 (ssh)
  * add a new ingressrule
      * source: 0.0.0.0/0
      * protocol: TCP
      * destination port range: 3001 (uptimekuma)
  * click Add Ingress Rules

#### Install Docker

#### Install UptimeKuma via docker compose

#### Use CF Zero Trust Tunnel to host xxxx.owndomain.fr on port 3001

#### Install Tailscale with split DNS..
