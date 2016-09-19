# docs-rabbitmq-staging

A repo for the RabbitMQ for Pivotal CF docs

About branch management:
+ Master contains the latest version of the docs
+ Other versions of the docs are contained in the branches named with the version number
+ At any one time, expect two versions of the latest doc; master and a staler branch named with the version number.

For example, to publish the v1.6.6 docs:
1. I merged the master branch into the v1.6.5 branch. 
2. Then, I merged the v1.6.6 branch (used to develop the new doc) into the master branch.

