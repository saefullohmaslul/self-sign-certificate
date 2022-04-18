# Self Sign Certificate

This repository containt command to generate self sign certificate using gen.sh

## Setup

To setup your certificate, please change your domain on `server-ext.cnf` and change `-subj` on file gen.sh based on:

```bash
/C= is for Country
/ST= is for STate or province
/L= is for Locality name or city
/O= is for Organisation
/OU= is for Organisation Unit
/CN= is for Common Name or domain name
/emailAddress= is for email address
```

## Running

1. Setup your requirement on `server.ext.cnf` and `-subj`
2. Running gen.sh using command

    ```bash
    chmod +x gen.sh
    ./gen.sh
    ```
3. The expected result is generate .pem file with sturcture like this:

    ```bash
    .
    ├── ca-cert.pem
    ├── ca-cert.srl
    ├── ca-key.pem
    ├── gen.sh
    ├── README.md
    ├── server-cert.pem
    ├── server-ext.cnf
    ├── server-key.pem
    └── server-req.pem
    ```