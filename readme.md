# dockercompose_configure_machine

## Description:

Configures a RHEL machine to run Docker Compose.

## Behaviour:

**Feature:** Ensures Docker Compose is installed
As a System Admin
I want to ensure that a RHEL machine is configure as a standalone Docker host
So that Docker containers can be managed on the host.

**Scenario**: Configures a RHEL 7 machine to run Docker Compose
- **Given** a base RHEL 7 machine is available
- **When** the configuration of the machine is initiated
- **Then** valid YUM repositories are installed
- **Then** the Python Package Manager is installed
- **Then** the Docker python library is installed
- **Then** Docker is installed
- **Then** Docker storage is configured
- **Then** Docker Compose is installed

## Configuration:

### Default variables

The following is a list of default variables used by this role.

| Variable  | Description  | Value  |
|---|---|---|
| **docker_device** | Device name for docker storage | /dev/sdb |
| **docker_compose_version** | The version of Docker Compose to be installed to manage the lifecycle of the Nexus Docker container. | 1.17.1 |

### Variables
| Variable  | Description  |
|---|---|
| **docker_version** | The version of Docker to install. |
| **repos_to_enable** | The list of rpm repositories to be enabled on the host. |
