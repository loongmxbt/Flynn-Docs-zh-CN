# 欢迎使用 Flynn

[Flynn](https://flynn.io) is a next generation open source Platform as a Service
(PaaS).

[Flynn](https://flynn.io) 是下一代的开源 PaaS 平台。

Unlike most PaaS's, Flynn can run stateful services as well as [twelve-factor
](http://12factor.net/) apps. This includes built-in database appliances (just
Postgres to start). Flynn is modular so users can easily modify, upgrade, and
replace components.

不同于大多数PaaS， Flynn 既可以运行 twelve－factor 应用，又可以运行状态服务。
Flynn 包括内置数据库应用（目前仅有 Postgres 一种）。Flynn 是一种模块，用户可以方便的定制、升级以及替换组件。

Flynn components are divided into two _layers_.

Flynn 组件被分为两层。

**Layer 0** is a low-level resource framework inspired by the [Google
Omega](http://eurosys2013.tudos.org/wp-content/uploads/2013/paper/Schwarzkopf.pdf)
paper. Layer 0 also includes [service discovery](/discoverd).

**Layer 1** is a set of higher level components that makes it easy to deploy and
maintain applications and databases.

You can learn more about the project at the [Flynn website](https://flynn.io).

**Layer 0** 是由 [Google
Omega](http://eurosys2013.tudos.org/wp-content/uploads/2013/paper/Schwarzkopf.pdf) 论文启发的一个底层资源框架。
Layer 0 也包括了 [service discovery](/discoverd).

**Layer 1** 是一套高层的组建，他使其能轻松的部署和维护应用程序和数据库。

你可以访问 [Flynn website](https://flynn.io) 了解更多项目相关信息。

### Status

Flynn 处于极速开发中。

Users are encouraged to experiment with Flynn but should assume there are
stability, security, and performance weaknesses throughout the project. This
warning will be removed when Flynn is ready for production use.

Please **report bugs** as issues on [this
repository](https://github.com/flynn/flynn/issues) after searching to see if
anyone has already reported the issue.

## Getting Started

### Run your own cluster

如果你想要配置并运行你自己的 Flynn 集群 （无论是本地还是使用专门硬件或是云服务商），你可以参考[Installation Guide](https://flynn.io/docs/installation)。

### Deploying applications

参见 [Using Flynn](https://flynn.io/docs) 教程如何部署和扩展应用。

## Components

### Layer 0

**[discoverd](/discoverd)** The Flynn service discovery system.

**[host](/host)** The Flynn host service, manages containers on each host
and provides the scheduling framework.

### Layer 1

**[blobstore](/blobstore)** A simple, fast HTTP file service.

**[bootstrap](/bootstrap)** Bootstraps Flynn Layer 1 from a JSON manifest using
the Layer 0 API.

**[cli](/cli)** Command-line Flynn HTTP API client.

**[controller](/controller)** Provides management and scheduling of applications
running on Flynn via an HTTP API.

**[gitreceived](/gitreceived)** An SSH server made specifically for accepting git pushes.

**[postgresql](/appliance/postgresql)** Flynn [PostgreSQL](http://www.postgresql.org/) database appliance.

**[receiver](/receiver)** Flynn's git deployer.

**[router](/router)** Flynn's TCP/HTTP router/load balancer.

**[slugbuilder](/slugbuilder)** Turns a tarball into a Heroku-style "slug" using
[buildpacks](https://devcenter.heroku.com/articles/buildpacks).

**[slugrunner](/slugrunner)** Runs Heroku-like
[slugs](https://devcenter.heroku.com/articles/slug-compiler).

**[taffy](/taffy)** Taffy pulls git repos and deploys them to Flynn.

## Contributing

We welcome and encourage community contributions to Flynn.

Since the project is still unstable, there are specific priorities for
development. Pull requests that do not address these priorities will not be
accepted until Flynn is production ready.

Please familiarize yourself with the [Contribution
Guidelines](https://flynn.io/docs/contributing) and [Project
Roadmap](https://flynn.io/docs/roadmap) before contributing.

There are many ways to help Flynn besides contributing code:

 - Find bugs and file issues.
 - Improve the [documentation](/website) and website.

Learn more at [flynn.io](https://flynn.io).

Flynn is a [trademark](https://flynn.io/docs/trademark-guidelines) of Prime Directive, Inc.
