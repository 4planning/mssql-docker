# SQL Server in Docker

This is 4Planning updated fork of Micorsof's [mssql-docker](https://github.com/microsoft/mssql-docker) repo, aims to provide a centralized location for community engagement. In here you will find documentation, Dockerfiles and additional developer resources.

> [:warn:] Sql server Windows containers are no longer supported by Microsoft, and their use are discouraged.

**SQL Server in Docker** could come in different flavors, but in this repo we currently maintain only SQL Server 2022 Express Edition. This image is based on Windows Container technology and can only be run using [Docker Engine for Windows Containers](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/docker/configure_docker_daemon).

Before choosing to run a SQL Server container for production use cases, please review our [support policy](https://support.microsoft.com/en-us/help/4047326/support-policy-for-microsoft-sql-server) for SQL Server Containers to ensure that you are running on a supported configuration.

**SQL Server Command Line Tools(sqlcmd,bcp)** are also available as a Docker Image. You can now deliver SQL Server management payload using this as a base image for your CI/CD scenarios. Check out the [mssql-tools Docker Image](https://hub.docker.com/r/microsoft/mssql-tools/) to get started.

Visit the [Microsoft Docker Hub page](https://hub.docker.com/u/microsoft) for more information and additional images.

## Documentation
- [Getting started guide for the SQL Server on Linux container](https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker)
- [Best practices guide](https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-configure-docker)

## Troubleshooting & Frequently Asked Questions

- "Unknown blob" error code: You are probably trying to run the Windows Containers-based Docker image on a Linux-based Docker Engine. If you want to continue running the Windows Container-based image, we recommend reading the following community article: [Run Linux and Windows Containers on Windows 10](https://stefanscherer.github.io/run-linux-and-windows-containers-on-windows-10/).

- When using the Windows Docker CLI you must use double quotes instead of single ticks for the environment variables, else the mssql-server-linux image won't find the `ACCEPT_EULA` or `SA_PASSWORD` variables which are required to start the container.

- The 'sa' password has a minimum complexity requirement (8 characters, uppercase, lowercase, alphanumerical and/or non-alphanumerical)

- Licensing for SQL Server in Docker: Regardless of where you run it - VM, Docker, physical, cloud, on prem - the licensing model is the same and it depends on which edition of SQL Server you are using. The Express and Developer Editions are free. Standard and Enterprise have a cost. More information here: [https://www.microsoft.com/en-us/sql-server/sql-server-2016-editions](https://www.microsoft.com/en-us/sql-server/sql-server-2016-editions)

## License

The Docker resource files for SQL Server are licensed under the MIT license.  See the [LICENSE file](LICENSE) for more details.

