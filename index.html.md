---
breadcrumb: RabbitMQ for Pivotal Cloud Foundry&reg; Documentation
title: RabbitMQ for Pivotal Cloud Foundry&reg; Documentation
owner: London Services
---

RabbitMQ is a fast and dependable open-source message server that supports a wide range of use cases including reliable integration, content based routing and global data delivery, and high volume monitoring and data ingestion.

Emerging as the de facto standard for cloud messaging, RabbitMQ is used for efficient communication between servers, applications and devices, and creates lasting value by enabling rapid development of modern decentralized application and data architectures that can scale with your business needs.
The [Pivotal Cloud Foundry&reg;](https://network.pivotal.io/products/pivotal-cf) (PCF) installer enables cloud operators to deploy a [RabbitMQ service](https://network.pivotal.io/products/pivotal-rabbitmq-service) in PCF. You can deploy the service as a single node or a cluster.

## Product snapshot

<dl>
<dt>Current RabbitMQ for PCF Details</dt>
<dd><strong>Version</strong>: 1.6.0 </dd>
<dd><strong>Release Date</strong>: 18th May 2016</dd>
<dd><strong>Software component version</strong>: RabbitMQ OSS 3.6.2</dd>
<dd><strong>Compatible Ops Manager Version(s)</strong>: 1.7.x, 1.6.x, 1.5.x, 1.4.x</dd>
<dd><strong>Compatible Elastic Runtime Version(s)</strong>: 1.7.x, 1.6.x, 1.5.x, 1.4.x</dd>
<dd><strong>vSphere support?</strong> Yes</dd>
<dd><strong>AWS support?</strong> Yes</dd>
<dd><strong>OpenStack support?</strong> Yes</dd>
</dl>

## Upgrading to the Latest Version

Consider the following compatibility information before upgrading RabbitMQ for Pivotal Cloud Foundry&reg;.

<p class="note"><strong>Note</strong>: Upgrading from any 1.5x tile to 1.6.x will involve taking the RabbitMQ cluster offline while the version of RabbitMQ is upgraded from 3.5.7 to 3.6.2  </p>

<p class="note"><strong>Note</strong>: Before you upgrade to Ops Manager 1.4.x, you must first upgrade RabbitMQ for PCF to at least 1.3.4. This allows RabbitMQ for PCF upgrades after you install OpsManager 1.4.x. </p>

<p class="note"><strong>Note</strong>: Only version 1.5.9 and above are certified to work in new installations of Ops Manager 1.7.x. </p>

For more information, refer to the full [Product Version Matrix](http://docs.pivotal.io/compatibility-matrix.pdf).

<table border="1" class="nice">
<tr>
  <th>Ops Manager Version</th>
  <th>Supported Upgrades from Imported RabbitMQ Installation</th>
</tr>
<tr>
  <th>1.3.x</th>
  <td><ul>
      <li>From 1.3.2.1 to 1.3.2.2, 1.3.3.0, 1.3.3.1, 1.3.3.2, 1.3.4.0</li>
      <li>From 1.3.2.2 to 1.3.3.0, 1.3.3.1, 1.3.3.2, 1.3.4.0</li>
      <li>From 1.3.3 to 1.3.3.1, 1.3.3.2, 1.3.4, 1.3.5, 1.3.6</li>
      <li>From 1.3.3.1 to 1.3.3.2, 1.3.4, 1.3.5, 1.3.6</li>
      <li>From 1.3.3.2 to 1.3.4, 1.3.5, 1.3.6</li>
      <li>From 1.3.4 to 1.3.5, 1.3.6</li>
      <li>From 1.3.5 to 1.3.6</li>
    </ul>
  </td>
</tr>
<tr>
  <th>1.6.x, 1.5.x and 1.4.x</th>
  <td><ul>
      <li>From 1.3.3.2 to 1.4.1, 1.4.2</li>
      <li>From 1.3.4 to 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.3.5 to 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.3.6 to 1.4.0, 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10</li>
      <li>From 1.4.0 to 1.4.1, 1.4.2, 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.1 to 1.4.2, 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.2 to 1.4.3, 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.3 to 1.4.4, 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.4 to 1.4.5, 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.5 to 1.4.6, 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.6 to 1.4.7, 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.7 to 1.4.8, 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.8 to 1.4.9, 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.9 to 1.4.10, 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.4.10 to 1.5.0, 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.0 to 1.5.1, 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.1 to 1.5.2, 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.2 to 1.5.3, 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.3 to 1.5.4, 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.4 to 1.5.5, 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.5 to 1.5.6, 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.6 to 1.5.7, 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.7 to 1.5.8, 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.8 to 1.5.9, 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.9 to 1.5.10, 1.5.11, 1.6.0</li>
      <li>From 1.5.10 to 1.5.11, 1.6.0</li>
      <li>From 1.5.11 to 1.6.0</li>
    </ul>
  </td>
</tr>
<tr>
  <th>1.7.x</th>
  <td><ul>
    <li>From 1.5.9 to 1.5.10, 1.5.11, 1.6.0</li>
    <li>From 1.5.10 to 1.5.11, 1.6.0</li>
    <li>From 1.5.11 to 1.6.0</li>
    </ul>
  </td>
</tr>
</table>


## Features

* Provision an instance of the RabbitMQ service, which corresponds to a unique RabbitMQ vhost (virtual host)
* Bind applications to an instance of the plan, providing unique credentials for each binding
* Management dashboard access to PCF Operators and application developers
* Deployment across multiple availability zones, with nodes striped across the AZs automatically
* Enable SSL (Secure Sockets Layer) for the AMQP, MQTT, STOMP protocols
* 2 node RabbitMQ cluster in a default deployment
* HAProxy load balancer across all nodes to balance connections
* Plugin configuration can be easily changed at any time and the cluster redeployed and updated
* The cluster topology can be changed and easily scaled out
* Default configurable policy applied to all new instances to mirror queues on two nodes
* Automated upgrades of RabbitMQ for major, minor and patch releases
* Configire the end point for the RabbitMQ Syslog
* RabbitMQ and HAproxy metrics are exposed on the firehose

### Install via Pivotal Ops Manager

To install RabbitMQ for PCF, follow the procedure for installing Pivotal Ops Manager tiles:

1. Download the product file from [Pivotal Network](https://network.pivotal.io/).
1. Upload the product file to your Ops Manager installation.
1. Click **Add** next to the uploaded product description in the Ops Manager `Available Products` view to add this product to your staging area.
1. Click the newly added tile to review any configurable options.
1. Click **Apply Changes** to install the service.

This product requires Ops Manager version 1.4.0 or greater.

### Using RabbitMQ in your application

RabbitMQ is shown in the services marketplace, either in the Apps Manager or
through `cf marketplace` on the CLI.

Application developers can create an instance of the application with `cf create-service p-rabbitmq standard <your name>`.
For this service an instance equals a **Vhost** on the RabbitMQ cluster.

Creating a binding gives the user permissions to access this Vhost and associated management dashboard.

### Current Limitations
Limitations with the current RabbitMQ for PCF product include:

* Availability Zone configuration **cannot** be changed once deployed.

We hope to address all of these limitations in future releases.

### Known Issues

* In versions `1.4.1` and `1.4.2`, the `manage` button for your RabbitMQ instance in Apps Manager will not automatically log you into the RabbitMQ Dashboard. You need to press `logout` and then login with your `username` and `password` which can be obtained from inspecting the environment variables for your instance.
* In versions `1.5.0` and `1.5.1`, when performing a fresh installation or upgrade, if the Elastic Runtime system and application domains are different then the `Broker Registrar` errand will fail. To resolve this disable the errand and redeploy, then register the broker manually using the system domain route `pivotal-rabbitmq-broker.system.domain`. For more information on registering brokers see the [CloudFoundry documentation](http://docs.cloudfoundry.org/services/managing-service-brokers.html).
* In the `1.5.0, 1.5.1, 1.5.2, 1.5.3` releases, when performing a fresh installation or upgrade, if you have the rabbitmq\_jsonrpc\_channel or rabbitmq\_jsonrpc\_channel_examples plugins selected then the RabbitMQ nodes will fail to start. The plugins are no longer distributed with RabbitMQ and plugin validation was introduced in RabbitMQ `3.5.7`, causing the nodes to fail to start. To resolve this issue you should install/upgrade to version `1.5.4` or above of the tile.
* In the '1.4.x` and `1.5.x` tiles it not possible to install the RabbitMQ tile in multiAZ with multi-subnet networks.

### Feedback
Please provide any bugs, feature requests, or questions to [the Pivotal Cloud Foundry&reg; Feedback list](mailto:pivotal-cf-feedback@pivotal.io).
