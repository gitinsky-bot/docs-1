---
title: Exporters and integrations
sort_rank: 4
---

# Exporters and integrations

There are a number of libraries and servers which help in exporting existing
metrics from third-party systems as Prometheus metrics. This is useful for
cases where it is not feasible to instrument a given system with Prometheus
metrics directly (for example, HAProxy or Linux system stats).

## Official third-party exporters

These exporters are maintained as part of the official
[Prometheus GitHub organization](https://github.com/prometheus):

   * [Node/system metrics exporter](https://github.com/prometheus/node_exporter)
   * [AWS CloudWatch exporter](https://github.com/prometheus/cloudwatch_exporter)
   * [Blackbox exporter](https://github.com/prometheus/blackbox_exporter)
   * [Collectd exporter](https://github.com/prometheus/collectd_exporter)
   * [Consul exporter](https://github.com/prometheus/consul_exporter)
   * [Graphite exporter](https://github.com/prometheus/graphite_exporter)
   * [HAProxy exporter](https://github.com/prometheus/haproxy_exporter)
   * [InfluxDB exporter](https://github.com/prometheus/influxdb_exporter)
   * [JMX exporter](https://github.com/prometheus/jmx_exporter)
   * [Memcached exporter](https://github.com/prometheus/memcached_exporter)
   * [Mesos task exporter](https://github.com/prometheus/mesos_exporter)
   * [MySQL server exporter](https://github.com/prometheus/mysqld_exporter)
   * [SNMP exporter](https://github.com/prometheus/snmp_exporter)
   * [StatsD exporter](https://github.com/prometheus/statsd_exporter)

The [JMX exporter](https://github.com/prometheus/jmx_exporter) can export from a
wide variety of JVM-based applications, for example [Kafka](http://kafka.apache.org/) and
[Cassandra](http://cassandra.apache.org/).

## Independently maintained third-party exporters

There are also a number of exporters which are externally contributed
and maintained. We encourage the creation of more exporters but cannot
vet all of them for best practices. Commonly, those exporters are
hosted outside of the Prometheus GitHub organization.

   * [Aerospike exporter](https://github.com/alicebob/asprom)
   * [Apache exporter](https://github.com/neezgee/apache_exporter)
   * [BIG-IP exporter](https://github.com/ExpressenAB/bigip_exporter)
   * [BIND exporter](https://github.com/digitalocean/bind_exporter)
   * [Ceph exporter](https://github.com/digitalocean/ceph_exporter)
   * [CouchDB exporter](https://github.com/gesellix/couchdb-exporter)
   * [Django exporter](https://github.com/korfuri/django-prometheus)
   * [Google's mtail log data extractor](https://github.com/google/mtail)
   * [Grok exporter](https://github.com/fstab/grok_exporter)
   * [Heka dashboard exporter](https://github.com/docker-infra/heka_exporter)
   * [Heka exporter](https://github.com/imgix/heka_exporter)
   * [IoT Edison exporter](https://github.com/roman-vynar/edison_exporter)
   * [IPMI exporter](https://github.com/lovoo/ipmi_exporter)
   * [Jenkins exporter](https://github.com/lovoo/jenkins_exporter)
   * [knxd exporter](https://github.com/RichiH/knxd_exporter)
   * [Meteor JS web framework exporter](https://atmospherejs.com/sevki/prometheus-exporter)
   * [Minecraft exporter module](https://github.com/Baughn/PrometheusIntegration)
   * [Mirth Connect exporter](https://github.com/vynca/mirth_exporter)
   * [MongoDB exporter](https://github.com/dcu/mongodb_exporter)
   * [Munin exporter](https://github.com/pvdh/munin_exporter)
   * [NATS exporter](https://github.com/lovoo/nats_exporter)
   * [New Relic exporter](https://github.com/jfindley/newrelic_exporter)
   * [Nginx metric library](https://github.com/knyar/nginx-lua-prometheus)
   * [NSQ exporter](https://github.com/lovoo/nsq_exporter)
   * [OpenWeatherMap exporter](https://github.com/RichiH/openweathermap_exporter)
   * [Passenger exporter](https://github.com/stuartnelson3/passenger_exporter)
   * [PgBouncer exporter](http://git.cbaines.net/prometheus-pgbouncer-exporter/about)
   * [PostgreSQL exporter](https://github.com/wrouesnel/postgres_exporter)
   * [PowerDNS exporter](https://github.com/janeczku/powerdns_exporter)
   * [RabbitMQ exporter](https://github.com/kbudde/rabbitmq_exporter)
   * [RabbitMQ Management Plugin exporter](https://github.com/deadtrickster/prometheus_rabbitmq_exporter)
   * [Rancher exporter](https://github.com/infinityworksltd/prometheus-rancher-exporter)
   * [Redis exporter](https://github.com/oliver006/redis_exporter)
   * [RethinkDB exporter](https://github.com/oliver006/rethinkdb_exporter)
   * [rTorrent exporter](https://github.com/mdlayher/rtorrent_exporter)
   * [scollector exporter](https://github.com/tgulacsi/prometheus_scollector)
   * [SMTP/Maildir MDA blackbox prober](https://github.com/cherti/mailexporter)
   * [Speedtest.net exporter](https://github.com/RichiH/speedtest_exporter)
   * [SQL query result set metrics exporter](https://github.com/chop-dbhi/prometheus-sql)
   * [Ubiquiti UniFi exporter](https://github.com/mdlayher/unifi_exporter)
   * [Varnish exporter](https://github.com/jonnenauha/prometheus_varnish_exporter)
   * [WebDriver exporter](https://github.com/mattbostock/webdriver_exporter)
   * [Xen exporter](https://github.com/lovoo/xenstats_exporter)
   * [Zookeeper exporter](https://github.com/carlpett/zookeeper_exporter)

When implementing a new Prometheus exporter, please follow the
[guidelines on writing exporters](/docs/instrumenting/writing_exporters)
Please also consider consulting the [development mailing
list](https://groups.google.com/forum/#!forum/prometheus-developers).  We are
happy to give advice on how to make your exporter as useful and consistent as
possible.

## Directly instrumented software

Some third-party software already exposes Prometheus metrics natively, so no
separate exporters are needed:

   * [cAdvisor](https://github.com/google/cadvisor)
   * [Doorman](https://github.com/youtube/doorman)
   * [Etcd](https://github.com/coreos/etcd)
   * [Kubernetes-Mesos](https://github.com/mesosphere/kubernetes-mesos)
   * [Kubernetes](https://github.com/kubernetes/kubernetes)
   * [RobustIRC](http://robustirc.net/)
   * [SkyDNS](https://github.com/skynetservices/skydns)
   * [Weave Flux](http://weaveworks.github.io/flux/)

## Other third-party utilities

This section lists libraries and other utilities that help you instrument code
in a certain language. They are not Prometheus client libraries themselves but
make use of one of the normal Prometheus client libraries under the hood. As
for all independently maintained software, we cannot vet all of them for best
practices.

   * Clojure: [prometheus-clj](https://github.com/soundcloud/prometheus-clj)
   * Go: [go-metrics instrumentation library](https://github.com/armon/go-metrics)
   * Go: [gokit](https://github.com/peterbourgon/gokit)
   * Java/JVM: [Hystrix metrics publisher](https://github.com/soundcloud/prometheus-hystrix)
