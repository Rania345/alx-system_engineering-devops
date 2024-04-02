# Load balancer
## Requirements
### General
- Allowed editors: `vi`, `vim`, `emacs`
- All your files will be interpreted on Ubuntu 16.04 LTS
- All your files should end with a new line
- A `README.md` file, at the root of the folder of the project, is mandatory
- All your Bash script files must be executable
- Your Bash script must pass `Shellcheck` (version 0.3.7) without any error
- The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
- The second line of all your Bash scripts should be a comment explaining what is the script doing

### Tasks:
* **0. Double the number of webservers**
  * [0-custom_http_response_header](./0-custom_http_response_header): Bash
  script that installs and configures Nginx on a server with a custom HTTP
  response header.
    * The name of the HTTP header is `X-Served-By`.
    * The value of the HTTP header is the hostname of the server.

* **1. Install your load balancer**
  * [1-install_load_balancer](./1-install_load_balancer): Bash script that
  installs and configures HAproxy version 1.5 on a server.
    * Enables management via the init script.
    * Requests are distributed using a round-robin algorithm.

* **2-puppet custom http response header**
  * [2-puppet_custom_http_response_header.pp](./2-puppet_custom_http_response_header.pp): Bash script that
  Just as in task #0, we’d like you to automate the task of creating a custom HTTP header response, but with Puppet.
    * The name of the custom HTTP header must be X-Served-By
    * The value of the custom HTTP header must be the hostname of the server Nginx is running on