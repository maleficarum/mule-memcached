mule-memcached
=============

This connector is a very basic way to writer/read from/to memcached.

Introduction
============

To include this connector in your project, you have to include mule-memcached jar.

After that, you must modify mule-config.xml to add the connector schema as follows :

#### Add the namespaces
	xmlns:memcached="http://www.mulesoft.org/schema/mule/memcached"

#### Include de XSD location
	http://www.mulesoft.org/schema/mule/memcached http://www.mulesoft.org/schema/mule/memcached/1.0-SNAPSHOT/mule-memcached.xsd

#### Configuration
=============

To connecto to Memcached service , you have to configure the follow params :

	<memcached:config host="localhost" />

Finally, to send messages to cache :

	<memcached:send key="TRANSID" message="#[payload['c']]" />

... to send messages to queue :

	<memcached:receive key="TRANSID" />
