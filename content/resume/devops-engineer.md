# As a DevOps Engineer

I am a strong proponent of [Infrastructure as Code](https://www.thoughtworks.com/insights/blog/infrastructure-code-reason-smile). I automate my infrastructure provisioning with [CloudFormation](https://aws.amazon.com/cloudformation/) and [Terraform](https://www.terraform.io) templates. My CloudFormation templates are written in YAML.

I used to write *everything* in CloudFormation but now write everything I can in Terraform. The original reason was to have templates which allow provisioning resources other than just AWS, i.e. [Azure](https://azure.microsoft.com), [Google Cloud](https://cloud.google.com), [Akamai](https://www.akamai.com). However, I have never really needed anything outside of what AWS provides but continue to use Terraform because I like the [template syntax](https://www.terraform.io/docs/configuration/syntax.html) better and I find its variables and [modularization](https://www.terraform.io/docs/configuration/modules.html) easier to work with (as opposed to CloudFormation's [nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-nested-stacks.html)).

I write both CloudFormation and Terraform templates in WebStorm because WebStorm has [built-in support for YAML](https://www.jetbrains.com/help/webstorm/code-style-yaml.html) and a [Terraform plugin](https://plugins.jetbrains.com/plugin/7808-hashicorp-terraform--hcl-language-support) which provides syntax highlighting and other goodies. I can also set up a WebStorm configuration which runs `terraform apply` on the current template with a keybinding.

I am also a proponent of [Immutable Servers](https://martinfowler.com/bliki/ImmutableServer.html) where compute instances / servers / containers are deployed once and, essentially, never patched or updated, avoiding [Configuration Drift](http://www.continuitysoftware.com/blog/what-is-configuration-drift/). Rather than apply a patch, new instances are deployed, traffic gradually moved to the new instances, and the old instances terminated. I have done [Green/Blue deployments](https://www.thoughtworks.com/insights/blog/implementing-blue-green-deployments-aws) using either load balancers or a [Weighted Round-Robin](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy.html#routing-policy-weighted) routing policy with [Route 53 DNS](https://aws.amazon.com/route53/) to gradually move traffic. [CodeDeploy](https://aws.amazon.com/codedeploy/) has also recently gotten [built-in support for Green/Blue deployments](https://aws.amazon.com/about-aws/whats-new/2017/01/aws-codedeploy-introduces-blue-green-deployments/) and I am actively exploring that option.

With Immutable Servers, I don't make a lot of use of [Chef](https://www.chef.io), [Puppet](https://puppet.com), or [Ansible](https://www.ansible.com). I don't care for Chef and Ansible because they are procedural vs. declarative and I don't like Puppet because advanced tasks require writing Ruby code. And, for the most part, I don't like any of them because they default to a client/server architecture which actually just adds more infrastructure that needs to be managed.  

Instead, I've become a huge fan of containerization with [Docker](https://www.docker.com) being my primary solution. I combine Docker with Hashicorp's [Packer](https://www.packer.io) to create Amazon Machine Images (AMIs) which are, currently, the final artifact deployed to production.

I'm looking into using [AWS Elastic Container Service](https://aws.amazon.com/ecs/) or [AWS Elastic Kubernetes Service](https://aws.amazon.com/eks/) to manage elasticity of container clusters in production. Containers are the future and managed elasticity is the way to go. The new [AWS Fargate](https://aws.amazon.com/fargate/) also provides some interesting new capabilities.

Sandbox, development, and QA environments use very small MySQL instances in [RDS](https://aws.amazon.com/rds/) or local instances of MySQL. Production uses a highly-available [Aurora](https://aws.amazon.com/rds/aurora/) cluster spread across multiple Availability Zones (AZs). I used to use [DynamoDB](https://aws.amazon.com/dynamodb/) for writing events and [triggering Lambda functions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.Lambda.html) but found Aurora to be more cost-effective in production and Aurora now also has the ability to [trigger Lambda functions](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/AuroraMySQL.Integrating.Lambda.html). I'm not the only one to [notice how cost-effective Aurora is](https://abhishek-tiwari.com/dynamodb-or-aurora/).

I'm also comfortable setting up a [Continuous Integration / Continuous Deployment](https://www.atlassian.com/continuous-delivery/ci-vs-ci-vs-cd) (CI/CD) workflow with [Jenkins][1], [CircleCI][2], or CodeBuild using GitHub or CodeCommit triggers. [AWS CodePipeline](https://aws.amazon.com/codepipeline/) pulls the code from CodeCommit and invokes [AWS CodeBuild](https://aws.amazon.com/codebuild/) to build the app, run tests, and integrate with Packer to create an AMI. [CodeDeploy](https://aws.amazon.com/codedeploy/) can then apply a CloudFormation or Terraform template to spin up an EC2 instance with the AMI.

[1]: https://jenkins.io
[2]: https://circleci.com

I make liberal use of [CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) along with [SNS notifications](https://aws.amazon.com/sns/) to monitor for problems in production. I've recently been introduced to [New Relic][3] and am finding it very helpful analyzing metrics and identifying problematic areas.

Logging is always a challenge in production environments. CloudWatch logs do the job for the most part but I've started working with 3rd party tools like [PaperTrail][4] for real-time offsite logging and [Logstash][5] and [Elasticsearch][6] for log analysis.

[5]: https://www.elastic.co/products/logstash
[6]: https://www.elastic.co/products/elasticsearch
[4]: https://papertrailapp.com
[3]: https://newrelic.com

I've worked with [VictorOps][7] to manage on-call schedules and integrate with other services like Slack. I've tinkered a bit with it's *transmogrification* feature to make AWS alarms more readable and actionable.

I use [CloudTrail](https://aws.amazon.com/cloudtrail/) to track user activity and API calls within the environment. It also comes in handy when you need to roll something back to a previous value that no one wrote down before changing it.

I proactively monitor and analyze costs with [Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) to find opportunities to reduce AWS expenses. I use [spot instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-spot-instances.html) whenever possible for batch jobs, CI/CD, and other intermittent activities.

[7]: https://victorops.com

I use [Lucidchart](https://www.lucidchart.com/pages/aws-architecture-import) to create network diagrams of my AWS infrastructure and [Cloudcraft](https://cloudcraft.co) to create cool 3D diagrams of the entire infrastructure.