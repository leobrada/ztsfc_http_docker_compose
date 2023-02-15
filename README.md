# ZTSFC_HTTP_DOCKER_COMPOSE
This is the docker compose solution for the ZTSFC framework published on the NetSys 2021 [1].
In the following it is explained how to set up the ZTSFC framework in a docker environment.

## docker_compose.yml
Start with creating your own **docker_compose.yml** file. As a template it is recommended to use the **example_docker_compose.yml**.
Here all important things are exemplarily defined already. Starting from this template, you can adjust it for your own purposes.

[1] Bradatsch, Leonard, Frank Kargl, and Oleksandr Miroshkin. "Zero Trust Service Function Chaining." Electronic Communications of the EASST 80 (2021).

## ZTSFC PEP
For the **ZTSFC PEP** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_pep.
Follow the instructions there to build the image.

## ZTSFC LDAP
For this docker container the image **osixia/openldap** is used. 

### bootstrap.ldif
You need to create a **bootstrap.ldif** file.
This file is used to populate the LDAP directory.
Please use the **example_bootstrap.ldif** file as an template.

### secrets
You need to create files that contain the passwords for the users **admin**, **config** and **readonly**. 
The files must be named **admin_pw.txt**, **config_pw.txt**, **readonly_pw.txt** respectively.
The files must be placed into the directory **secrets**.
In this directory you can also find example files.
The respective files must also be specified in the **docker_compose.yml** file:
 > LDAP_ADMIN_PASSWORD_FILE: /run/secrets/admin_pw  
 > LDAP_CONFIG_PASSWORD_FILE: /run/secrets/config_pw  
 > LDAP_READONLY_USER_PASSWORD_FILE: /run/secrets/readonly_pw

### certs
In the **certs** directory you must place the certificates for the LDAP service. First, a CA certificate is needed. The LDAP service accepts only certificates signed by this CA when presented by a connecting party.
Second, the certificate and private key for the LDAP service itself is needed.
This certificate information must be specified in the **docker_compose.yml** file:
 > LDAP_TLS_CRT_FILENAME: "ztsfc_http_ldap.crt"  
 > LDAP_TLS_KEY_FILENAME: "ztsfc_http_ldap_priv.key"  
 > LDAP_TLS_CA_CRT_FILENAME: "CA.crt"

## ZTSFC PDP
For the **ZTSFC PDP** component we use the docker image from https://github.com/vs-uulm/ztsfc_http_pdp.
Follow the instructions there to build the image.

### certs
Create your certificate (incl. private key) you present during the TLS handshake. Also define the CA certificate.
Both certificates and private key need to located in the directory **certs**.

### config
Create a config file **conf.yml** in the directory **config**.
You can use **example_conf.yml** as template.