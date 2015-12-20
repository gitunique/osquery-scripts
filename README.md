# osquery-scripts
Configuration and parsing of osquery related data

## Background

osquery is a host-based monitoring tool developed and used by facebook. More details 
are available from:
 - https://code.facebook.com/posts/844436395567983/introducing-osquery/

## Configuration details

Employing osquery in a scalable way can be done by using filebeat 
(https://www.elastic.co/products/beats/filebeat) to transport log entries
directly to elastic search or via logstash for additional filtering and processing.

### Filebeat
Filebeat is a lightweight forwarder and needs to be installed on each host running osquery.
A sample configuration file is contained within the filebeat directory.

### Logstash
Logstash is highly configurable, a basic configuration specifying 
 - a beats input
 - a simple filter
 - an output to elastic search

is contained in the log stash directory.

### osqueryd.comf
An example osquery configuration that will work with Ubuntu based linux systems is
contained in the osquery directory.


