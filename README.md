# Managing secrets with SOPS and GCP KMS

This is a sample repository use [sops](https://github.com/mozilla/sops) to encrypt and decrypt secret with GCP KMS.

## Prerequisites

- Access to GCP KMS keys via IAM
- SOPS - https://github.com/mozilla/sops/releases

## Encrypt secrets

Move to the `./env/dev` and `sops -e -i values.yaml`

## Decrypt secrets

Move to the `./env/dev` and `sops -d -i values.yaml`

## Install the chart

```bash
    sops -d -i values.yaml
    helm install --name=sopssecret --debug --dry-run ./sec -f ./sec/env/dev/values.yaml
```
