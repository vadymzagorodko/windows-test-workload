# Running a Windows Docker Container

This folder includes a [Marathon](https://mesosphere.github.io/marathon/) app
definition which can be used to run a Windows Docker Container on a DC/OS mixed cluster.

### Steps to run the example workload

- Install Marathon-LB from DC/OS service catalogue and you will have the ability to access the app using http://<linuxpublicagentipaddress>
- Specify in the `windows-docker-app.json` file the `HAPROXY_0_VHOST` which is the public dns name of the public agent
- Update in the `windows-docker-app.json` file the `constraints` which is the region like `windows-us-west-2`.
- Install the `windows-docker-app.json` filetemplate to run the Windows Docker container
