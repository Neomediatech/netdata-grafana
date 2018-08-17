# netdata-grafana
Automatically generate grafana dashboard from Netdata metrics and config. (Graphite and Devel for opentsdb)

## requirements:
* netdata configured to send metric on a backend, like this:
(/etc/netdata/netdata.conf)
<pre>[backend]
    enabled = yes 
    data source = average 
    type = graphite 
    destination = tcp:fw...ne....it:2003 
    # type your backend server:port 
    prefix = netdata 
    # hostname = netdata 
    update every = 10 
    send hosts matching = localhost *</pre>

## usage:  
* clone this repo on host that run netdata
* modify netdata-grafana-hosts.conf according to your needs
* run 'python parser.py'
you'll get a file named [hostname].json
* import this json on Grafana
maybe all is ok :-)
