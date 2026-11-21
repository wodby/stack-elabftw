# eLabFTW application stack for Kubernetes on Wodby

Deploy eLabFTW, the open source electronic lab notebook, on Kubernetes with
Wodby.

This repository defines the Wodby stack manifests and default service
composition for eLabFTW.

<!-- wodby:generated:start -->

## Stack contract

- [eLabFTW stack on Wodby](https://wodby.com/stacks/elabftw)
- [Browse Wodby application stacks](https://wodby.com/stacks)
- [Wodby stack documentation](https://wodby.com/docs/2.0/stacks/)
- [Stack manifest reference](https://wodby.com/docs/2.0/stacks/template/)

## Service definitions

- [eLabFTW service](https://github.com/wodby/service-elabftw)
- [MySQL service](https://github.com/wodby/service-mysql)
- [OpenSMTPD service](https://github.com/wodby/service-opensmtpd)

## What's included

| Component / service | Default configuration |
| --- | --- |
| eLabFTW<br>`elabftw` | required; enabled by default; volumes: `data` 20 GB; links: `mysql` → `mysql`, `sendmail` → `opensmtpd` |
| MySQL<br>`mysql` | required; enabled by default; volumes: `data` 10 GB |
| OpenSMTPD<br>`opensmtpd` | optional; disabled by default |

Enabled optional services are selected by default but can be excluded when an
app is created. Disabled optional services are available but not selected by
default. Required services cannot be excluded.

## Validate the stack manifest

```bash
wodby stack validate-manifest stack.yml --org <org-id>
```

<!-- wodby:generated:end -->
