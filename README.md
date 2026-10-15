<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/logo-dark.svg">
    <img src="assets/logo-light.svg" alt="yggy" height="56">
  </picture>
</p>

<h1 align="center">yggy SDK for Python</h1>

<p align="center">Typed client for the yggy API. Python 3.9 or newer.</p>

## Install

The PyPI package `yggy` is not published yet. Until it is, install from GitHub:

```bash
pip install git+https://github.com/yggy-tech/yggy-sdk-python
```

## Example

List the projects your key can see:

```python
import os

import yggy

configuration = yggy.Configuration(
    host="https://api.yggy.tech",
    api_key={"apiKeyAuth": os.environ["YGGY_API_KEY"]},
)

with yggy.ApiClient(configuration) as api_client:
    api_client.set_default_header("x-yggy-organization-id", "acme-corp")
    response = yggy.ProjectsApi(api_client).list_projects()
    for project in response.projects:
        print(project.name)
```

## Authenticate

Create an API key in yggy under **Developers → API keys** and keep it in an environment variable. A key that belongs to one organization needs nothing else. A personal key can see several organizations, so name the one you want in the `x-yggy-organization-id` header, by id or slug, as the example does.

See [Authentication](https://docs.yggy.tech/developers/authentication/) for key types and permissions.

## What you can call

Projects, documents (upload, status, extracted facts, download, retry), questions over a project or a whole organization, chat, entity lookup by identity, the ontology overview and graph exports. The [API reference](https://docs.yggy.tech/developers/rest/reference/) lists every operation with its parameters. For a first walkthrough, follow the [quickstart](https://docs.yggy.tech/developers/quickstart/).

## Generated code

Everything except this file is generated from the yggy OpenAPI document, so a change here is overwritten by the next sync. Report bugs or request an operation by opening an issue in this repository, or write to [support](https://yggy.tech/support).

## License

Apache-2.0. See [LICENSE](LICENSE).
