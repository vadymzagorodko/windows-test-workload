# Running a Windows Docker Container

This folder includes a [Marathon](https://mesosphere.github.io/marathon/) app
definition which can be used to run a Windows Docker Container on a DC/OS mixed cluster.

### Steps to run the example workload

- Install Marathon-LB from DC/OS service catalogue and you will have the ability to access the app using `http://<linuxpublicagentipaddress>`
- Modify in the `windows-docker-app.json` file:
   - the label `HAPROXY_0_VHOST` which must be the public dns name of the public agent
   - the `constraints` which must be set to the region of the windows node (like `windows-us-west-2`).
- Deploy the Jenkins app defined in `windows-docker-app.json`
   ```
   dcos marathon app add windows-docker-app.json
   ```

