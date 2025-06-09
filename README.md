# trly-dev
quad-ops deployment for trly.dev


## Bootstrap Environment
1. pre-create secrets for porkbun api key and api secret key
``` bash
set +o history
export PORKBUN_API_KEY=your-porkbun-api-key
export PORKBUN_API_SECRET_KEY=your-porkbun-api-secret
podman secret create acme_email <(echo <your-email-address)
podman secret create porkbun-api-key <(echo $PORKBUN_API_KEY)
podman secret create porkbun-api-secret-key <(echo $PORKBUN_API_SECRET_KEY)
set -o history
```
