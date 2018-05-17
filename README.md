# Riello Netman

[Riello](http://www.riello-powersystems.de) UPS use a module called Netman to provive SNMP performance data.
OpenNMS doesn't has Riellos OIDs included per default.
So an additional config is required.

Copy the datacollection file into $ONMS_HOME/etc/datacollection/ and don't forget to add an entry in datacollection-config.xml:

`<include-collection dataCollectionGroup="Netman-Plus"/>`

OpenNMS needs a restart to load this config!

The default UPS graphes will be used for these metrics too.
So no need to create new ones.
