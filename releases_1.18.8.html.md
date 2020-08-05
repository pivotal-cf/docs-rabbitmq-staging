## <a id="1-18-8"></a> v1.18.8

**Release Date**: July 17, 2020

### Resolved Issues

This release fixes the following issues:

Previously, the smoke test would pick up the default cf domain. This might 
cause smoke tests to fail when the smoke tests domain is not accessible from
the RabbitMQ Service Instance domain for on-demand services. 
Operators can now configure the smoke tests domain to ensure that the service instance is accessible during smoke tests.


### Known Issues

This release has the following known issues:


### Compatibility

The following components are compatible with this release:

<table class="nice"> <th>Component</th> <th>Version</th> 	<tr>
		<td>Erlang</td>
		<td>22.3.4.3</td>
	</tr>
	<tr>
		<td>HAProxy</td>
		<td>1.8.25</td>
	</tr>
	<tr>
		<td>OSS RabbitMQ*</td>
		<td>3.8.5</td>
	</tr>
	<tr>
		<td>Stemcell</td>
		<td>621.x</td>
	</tr>
	<tr>
		<td>Tanzu Application Service</td>
		<td>2.7.*, 2.8.*, 2.9.*</td>
	</tr>
	<tr>
		<td>bpm</td>
		<td>1.1.8</td>
	</tr>
	<tr>
		<td>cf-cli</td>
		<td>1.27.0</td>
	</tr>
	<tr>
		<td>cf-rabbitmq</td>
		<td>312.0.0</td>
	</tr>
	<tr>
		<td>cf-rabbitmq-multitenant-broker</td>
		<td>73.0.0</td>
	</tr>
	<tr>
		<td>cf-rabbitmq-service-gateway</td>
		<td>18.0.0</td>
	</tr>
	<tr>
		<td>cf-rabbitmq-smoke-tests</td>
		<td>55.0.0</td>
	</tr>
	<tr>
		<td>loggregator-agent</td>
		<td>3.21.5</td>
	</tr>
	<tr>
		<td>on-demand-service-broker</td>
		<td>0.40.0</td>
	</tr>
	<tr>
		<td>rabbitmq-metrics</td>
		<td>34.0.0</td>
	</tr>
	<tr>
		<td>rabbitmq-on-demand-adapter</td>
		<td>139.0.0</td>
	</tr>
	<tr>
		<td>routing</td>
		<td>0.203.0</td>
	</tr>
	<tr>
		<td>service-metrics</td>
		<td>1.12.5</td>
	</tr>
	<tr>
		<td>syslog</td>
		<td>11.6.1</td>
	</tr></table>

* For more information, see the <a href="https://github.com/rabbitmq/rabbitmq-server/releases/tag/v3.8.5">v3.8.5</a> GitHub documentation.
