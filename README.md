# ECM Containers

The ECM Containers v1.0 offering provides a true hybrid platform:
- Provides ease of deployment not only on-prem, but also in private and public cloud environments like IBM Cloud, AWS, Azure, and IBM Cloud Private (ICp).
- Provides a scalable, manageable, upgradeable, and maintainable platform for both on-premise and cloud environments (public and private)
- Improves return on investmet (ROI) by reducing infrastructure costs and labor costs for maintenance and support
- Reduces the turnaround time of providing customer access to ECM Cloud environments

## Docker images
Review the readme that is provided with each Docker image for details about prerequisites and setup information. 
The ECM Container offering provides the following Docker images with built-in monitoring and logging and security-hardened capabilities:

#### `CPE` [IBM Content Platform Engine](https://github.com/ibm-ecm/container-cpe)
> IBM® Content Platform Engine (CPE) container is a Docker image that enables you to quickly deploy IBM Content Platform Engine without a traditional software installation.
 
#### `CSS` [IBM Content Search Services](https://github.com/ibm-ecm/container-css)
> IBM® Content Search Services container is a Docker image that enables you to quickly deploy IBM Content Search Services cwithout a traditional software installation.

#### `ICN` [IBM Content Navigator](https://github.com/ibm-ecm/container-icn)
> IBM® Content Navigator (ICN) container is a Docker image that enables you to quickly deploy IBM Content Navigator to work with your container implementation of IBM Content Platform Engine.

#### `CMIS` [IBM Content Management Interoperability Services](https://github.com/ibm-ecm/container-cmis)
> IBM® CMIS for Content Manager (IBM CMIS) container is a Docker image that enables you to quickly deploy CMIS without needing to do traditional software install. 

#### `ICM` [IBM Case Manager](https://github.com/ibm-ecm/container-icm)
> IBM® Case Manager (ICM) container is a Docker image that enables you to quickly deploy IBM Case Manager to work with your container implementation of IBM Content Platform Engine.


## Access ECM Container images in Docker Cloud private repositories

### 1. Sign up the Docker ID to access Docker Store
Access Docker Cloud and sign up your Docker ID with one unique Docker ID, Email address and set password.
https://cloud.docker.com/

### 2. Contact IBM and supply us your Docker ID and the Email address, the ECM container image need to be pulled.
For example:

```
Docker ID: mydockerid
Email address: mydockerid@abc.com
ECM container image: Filenet Content Platform Engine
```

### 3. When approved, IBM will assign the Docker ID access permission to ECM Container private repositories, and notice you the image tag information.
For example:

```
ecmcontainers/ecm_earlyadopters_cpe:earlyadopters-gm5.5
```

### 4. Execute docker pull command in your Docker runtime environment.
Need to login Docker Cloud with `docker login` commnd in advance, and then input your Docker ID for user name and password. Please notice that input Docker ID, instead of the email address.
```
# input Docker ID for user name instead of email address
docker login
or
docker login -u [Docker ID] -p [Password]
e.g.
docker login -u mydockerid -p mydockerpw

# pull image from Docker Cloud
docker pull ecmcontainers/ecm_earlyadopters_cpe:earlyadopters-gm5.5
