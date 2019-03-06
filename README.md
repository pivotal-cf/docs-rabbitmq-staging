# RabbitMQ for Pivotal CF docs

### Branch Management

The master branch is the tree-trunk, so ALWAYS make changes you want carried forward in this branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Then, if necessary, immediately cherry-pick/copy any changes that you want to push immediately to production into the appropriate branches listed below:

| Branch Name| Use for… |
|------------| ---------|
| master     | 1.16 (staged here: http://docs-pcf-staging.cfapps.io/rabbitmq-cf/1-n/index.html) |
| 1.15-live  | 1.15 (http://docs.pivotal.io/rabbitmq-cf/1-15/) |
| 1.14-live  | v1.14 (http://docs.pivotal.io/rabbitmq-cf/1-14/)|
| 1.13-live  | v1.13 (http://docs.pivotal.io/rabbitmq-cf/1-13/)|
| 1.12-live  | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.12.pdf)|
| 1.11-live  | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.11.pdf)|
| 1.10-live  | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.10.pdf)|
| 1.9-live   | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf)|
| 1.8-live   | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.8.pdf)|
| 1.7-live   | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.7.pdf)|
| 1.6-live   | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.6.pdf)|
| 1.5-live   | NOT IN USE (PDF is here: https://docs.pivotal.io/archives/rabbitmq-pcf-1.5.pdf)|


[docs-book-rabbitmq]: https://github.com/pivotal-cf/docs-book-rabbitmq/blob/master/config.yml

### Staging Environment

When a commit is made into any of the above branches, the documentation is deployed by [this concourse build][docs-staging-deploy]. All the supported
versions will be accessible on the [staging website][docs-staging].

[docs-staging-deploy]: https://wings.concourse.ci/teams/cf-docs/pipelines/cf-services?groups=rabbitmq
[docs-staging]:        http://docs-pcf-staging.cfapps.io/rabbitmq-cf/

### Style Sheet

Use this section to specify spelling of special words for RabbitMQ for PCF:

+ on-demand plan
+ shared-VM plan
+ dedicated-VM plan

### Making Your Documentation Changes Live

Click the deploy button in the pipeline! Living the dream :-D

### Tag Management

We do not need to maintain older versions of the documentation so we're electing to not use tags to snapshot the state of the documentation for each previous patch version.

### Contributing Documentation

If there's some documentation to add for an unreleased patch version of RabbitMQ then create a branch off of the **live** branch you intend to modify and create a Pull Request against that branch. Once the version that change is targeting is released, the Pull Request can be merged and will be live the next time a documentation deployment occurs.

If the documentation is meant to be target several released versions, then you'll need to create a Pull Request for each individual minor version.

### Partials

Cross-product partials for **RabbitMQ for Pivotal CF ** are single sourced from the [Services Partials](https://github.com/pivotal-cf/docs-services-partials) repo to allow for versioning.

Previously, these partials were sourced from the v018.x branch of the On Demand Service Broker SDK and did not support versions.

### Releasing a New Minor Version

Since **master** is the latest and greatest documentation, the process would be to cut a **x.x-live** branch for the version that **master** was targeting during that time. A corresponding section in **config.yml** in the [docs-book-pcfservices][docs-book-pcfservices] repository would also need to be made.

After this point, **master** will then be the target for the next version of the RabbitMQ product tile.
