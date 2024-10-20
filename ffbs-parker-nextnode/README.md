ffbs-parker-nextnode
====================

This is the core package of [gluon-parker](https://github.com/ffbs/gluon-parker),
a Gluon fork that uses routing between the nodes
(aka. Router devices) and the infrastructure.
It is currently in use at Freifunk Braunschweig.
Other communities are interested in adopting it as well.

This package provides `ebtables`-rules that redirect traffic to the
`localnode` IPs to the node itself.

This is needed in networks where the `localnode` addresses are outside
of the client network - for example when using with `parker`.

site.conf
---------

Your `site.conf` probably already contains a `next_node` section, as
requested by the [documentation](https://gluon.readthedocs.io/en/latest/user/site.html).

For Freifunk Braunschweig this section looks like this:

```json
next_node = {
        ip4 = "172.16.127.1",
        ip6 = "2001:bf7:382:0::1",
        name = { "node.ffbs" },
        mac = "72:02:46:6a:1c:27",
},
```
