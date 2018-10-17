# RabbitMQ for Pivotal CF docs

## Branches in this Content Repo

**MASTER** branch - Use for the next unreleased version: **1.15**, staged here: http://docs-pcf-staging.cfapps.io/rabbitmq-cf/1-n/index.html

The master branch is the tree-trunk, so ALWAYS make changes you want carried forward in this branch. This includes:

* Unreleased features
* Doc bug fixes
* Doc reorganization or enhancement

Then, if necessary, immediately cherry-pick/copy any changes that you want to push immediately to production into the appropriate "-live" branch below:

**1.14-live** - current branch for documentation that is assumed/expected to be live on [docs.pivotal.io/rabbitmq-cf/1-14](http://docs.pivotal.io/rabbitmq-cf/1-14/).

**1.13-live** - current branch for documentation that is assumed/expected to be live on [docs.pivotal.io/rabbitmq-cf/1-13](http://docs.pivotal.io/rabbitmq-cf/1-13/).

**1.12-live** - current branch for documentation that is assumed/expected to be live on [docs.pivotal.io/rabbitmq-cf/1-12](http://docs.pivotal.io/rabbitmq-cf/1-12/).

**1.11-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.11.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.11.pdf).

**1.10-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.10.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.10.pdf).

**1.9-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf).

**1.8-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf).

**1.7-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf).

**1.6-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf).

**1.5-live** - not in use because the docs are no longer live. PDF available at [https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf](https://docs.pivotal.io/archives/rabbitmq-pcf-1.9.pdf).

[docs-book-rabbitmq]: https://github.com/pivotal-cf/docs-book-rabbitmq/blob/master/config.yml


## Book Repo

**docs-book-rabbitmq** is the book repo:

* **Edge** branch is for the next unreleased version, available on staging at this link:<br>
http://docs-pcf-staging.cfapps.io/rabbitmq-cf/1-n/index.html

* **Master** branch is for the published/live releases listed above.


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

### Releasing a New Minor Version

Since **master** is the latest and greatest documentation, the process would be to cut a **x.x-live** branch for the version that **master** was targeting during that time. A corresponding section in **config.yml** in the [docs-book-pcfservices][docs-book-pcfservices] repository would also need to be made.

After this point, **master** will then be the target for the next version of the RabbitMQ product tile.

