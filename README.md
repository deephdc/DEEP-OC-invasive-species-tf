<div align="center">
<img src="https://marketplace.deep-hybrid-datacloud.eu/images/logo-deep.png" alt="logo" width="300"/>
</div>

# DEEP as a Service container for invasive species identification

[![Build Status](https://jenkins.indigo-datacloud.eu:8080/buildStatus/icon?job=Pipeline-as-code/DEEP-OC-org/DEEP-OC-invasive-species-tf/master)](https://jenkins.indigo-datacloud.eu:8080/job/Pipeline-as-code/job/DEEP-OC-org/job/DEEP-OC-invasive-species-tf/job/master)

This is a container that will run the DEEP as a Service API component. From the DEEPaas API the user can choose the model
 to train or to predict, together with the basic input parameters.


## Run the container

### Directly from Docker Hub

To run the Docker container directly from Docker Hub and start using the API
simply run the following command:

```bash
$ docker run -ti -p 5000:5000 deephdc/deep-oc-invasive-species-tf
```

This command will pull the Docker container from the Docker Hub
[`deephdc`](https://hub.docker.com/u/deephdc/) organization.

### Building the container

If you want to build the container directly in your machine (because you want
to modify the `Dockerfile` for instance) follow the following instructions:

Building the container:

1. Get the `DEEP-OC-invasive-species-tf` repository (this repo):

    ```bash
    $ git clone https://github.com/deephdc/DEEP-OC-invasive-species-tf
    ```

2. Build the container:

    ```bash
    $ cd DEEP-OC-invasive-species-tf
    $ docker build -t deephdc/deep-oc-invasive-species-tf .
    ```

3. Run the container:

    ```bash
    $ docker run -ti -p 5000:5000 deephdc/deep-oc-invasive-species-tf
    ```

These three steps will download the repository from GitHub and will build the
Docker container locally on your machine. You can inspect and modify the
`Dockerfile` in order to check what is going on. For instance, you can pass the
`--debug=True` flag to the `deepaas-run` command, in order to enable the debug
mode.


## Connect to the API

Once the container is up and running, browse to `http://localhost:5000` to get
the [OpenAPI (Swagger)](https://www.openapis.org/) documentation page.
