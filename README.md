kubealex.general.role_generate_certs
=========

The `role_generate_certs` role generates and signs certificates using a Certificate Authority (CA).

Requirements
------------

- asn1crypto
- cryptography

Role Variables
--------------

| Variable                   | Description                                              | Default Value                |
|----------------------------|----------------------------------------------------------|------------------------------|
| `ca_path`                  | Path to the CA certificate file                           | *None*                       |
| `ca_key_path`              | Path to the CA private key file                           | *None*                       |
| `ca_key_passphrase`        | Passphrase for the CA private key                         | *None*                       |
| `cert_filename`            | Filename of the generated certificate                     | `mycert`                     |
| `cert_destination_path`    | Destination path for the generated certificates           | `~/generated-certs`          |
| `cert_CN`                  | Common Name (CN) for the generated certificate            | `Sample Certificate`         |
| `cert_C`                   | Country Name (C) for the generated certificate            | `US`                         |
| `cert_L`                   | Locality Name (L) for the generated certificate           | `Galaxy`                     |
| `cert_O`                   | Organization Name (O) for the generated certificate       | `My Company`                 |
| `cert_OU`                  | Organizational Unit Name (OU) for the generated certificate | `My Lab`                  |
| `cert_san`                 | Subject Alternative Names (SAN) for the generated certificate | *omit*                     |
| `cert_generate_pkcs`       | Generate PKCS file for key, cert and CA                   | false                     |
| `archive_certs`            | Flag indicating whether to create an archive of the certificates | `false`                  |


Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - name: Test role
      hosts: localhost
      roles:
        - role: kubealex.general.role_generate_certs
          ca_path: </MY/PATH/ca_cert.pem>
          ca_key_path: </MY/PATH/ca_cert.key>
          ca_key_passphrase: <MYSECRET>

License
-------

Apache 2.0

Author Information
------------------

Alessandro Rossi <al.rossi87@gmail.com>