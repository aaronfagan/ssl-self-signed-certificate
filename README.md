# Self Signed SSL Certificates

## Create the Private Key
`sudo openssl genrsa -out localhost.key 2048`

## Create Certificate Signing Request (CSR)
`sudo openssl req -new -out localhost.csr -key localhost.key -config config.cnf`

## Sign the SSL Certificate
`sudo openssl x509 -req -days 3650 -in localhost.csr -signkey localhost.key -out localhost.crt -extensions v3_req -extfile config.cnf`

# Contributors
* Aaron Fagan - [Github](https://github.com/aaronfagan), [Website](https://www.aaronfagan.ca/)
