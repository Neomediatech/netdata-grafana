# netdata-grafana
Automatically generate grafana dashboard from Netdata metrics and config. (Graphite and Devel for opentsdb)

usage:  
  - clone this repo on host that run netdata
  - modify netdata-grafana-hosts.conf according to your needs
  - run 'python parser.py'
  you'll get a file named [hostname].json
  - import this json on Grafana
  maybe all is ok :-)
