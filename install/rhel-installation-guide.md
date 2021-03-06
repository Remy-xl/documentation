# Install Kata Containers on RHEL

> **Warning:**
>
> - The RHEL packages are provided as a convenience to users until native
>   packages are available in RHEL. However, they are **NOT** currently tested
>   (although CentOS is) so caution should be exercised.
>
>   See https://github.com/kata-containers/ci/issues/3 for further details.

1. Install the Kata Containers components with the following commands:

   ```bash
   $ source /etc/os-release
   $ ARCH=$(arch)
   $ BRANCH="${BRANCH:-master}"
   $ sudo -E yum-config-manager --add-repo "http://download.opensuse.org/repositories/home:/katacontainers:/releases:/${ARCH}:/${BRANCH}/RHEL_${VERSION_ID}/home:katacontainers:releases:${ARCH}:${BRANCH}.repo"
   $ sudo -E yum -y install kata-runtime kata-proxy kata-shim
   ```

2. Decide which container manager to use and select the corresponding link that follows:

   - [Docker](docker/rhel-docker-install.md)
   - [Kubernetes](https://github.com/kata-containers/documentation/blob/master/Developer-Guide.md#run-kata-containers-with-kubernetes)
