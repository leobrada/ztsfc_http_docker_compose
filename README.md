# ZTSFC_HTTP_DOCKER_COMPOSE
This is the docker compose solution for the ZTSFC framework published on the NetSys 2021 [1].
In the following it is explained how to set up the ZTSFC framework in a docker environment.

## docker_compose.yml
Start with creating your own **docker_compose.yml** file. As a template it is recommended to use the **example_docker_compose.yml**.
Here all important things are exemplarily defined already. Starting from this template, you can adjust it for your own purposes.

[1] Bradatsch, Leonard, Frank Kargl, and Oleksandr Miroshkin. "Zero Trust Service Function Chaining." Electronic Communications of the EASST 80 (2021).

## ZTSFC HTTP PEP
For the **ZTSFC HTTP PEP** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_pep.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_pep/cert**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_pep/config**.
You can use **example_conf.yml** as template.

### policies
Create a config file **policies.yml** in the directory **./ztsfc_http_pep/policies**.
You can use **example_policies.yml** as template.

### passwwd
Create a passwd file **passwd.txt** in the directory **./ztsfc_http_pep/passwd**.
You can use **example_passwd.yml** as template.
The **passwd.txt** file has the structure: userName:salt:sha512Hash

## ZTSFC HTTP PDP
For the **ZTSFC HTTP PDP** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_pdp.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_pdp/cert**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_pdp/config**.
You can use **example_conf.yml** as template.

### policies
Create a config file **policies.yml** in the directory **./ztsfc_http_pdp/policies**.
You can use **example_policies.yml** as template.

## ZTSFC HTTP PIP
For the **ZTSFC HTTP PIP** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_pip.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_pip/certs**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_pip/config**.
You can use **example_conf.yml** as template.

## ZTSFC HTTP SERVICE
For the **ZTSFC HTTP SERVICE** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_service.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_service/certs**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_service/config**.
You can use **example_conf.yml** as template.

## ZTSFC HTTP SERVICE FUNCTION IPS
For the **ZTSFC HTTP SERVICE FUNCTION IPS** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_ips.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_sf_ips/certs**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_sf_ips/config**.
You can use **example_conf.yml** as template.

## ZTSFC HTTP SERVICE FUNCTION LOGGER
For the **ZTSFC HTTP SERVICE FUNCTION LOGGER** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_sf_logger.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_sf_logger/certs**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_sf_logger/config**.
You can use **example_conf.yml** as template.

## ZTSFC HTTP SFP LOGIC
For the **ZTSFC HTTP SFP LOGIC** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_sfp_logic.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **./ztsfc_http_sfp_logic/cert**.

### config
Create a config file **conf.yml** in the directory **./ztsfc_http_sfp_logic/config**.
You can use **example_conf.yml** as template.

### policies
Create a config file **policies.yml** in the directory **./ztsfc_http_sfp_logic/policies**.
You can use **example_policies.yml** as template.
