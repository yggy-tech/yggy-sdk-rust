<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/logo-dark.svg">
    <img src="assets/logo-light.svg" alt="yggy" height="56">
  </picture>
</p>

<h1 align="center">yggy SDK for Rust</h1>

<p align="center">Typed client for the yggy API, built on reqwest.</p>

## Install

The crate `yggy-sdk` is not published yet. Until it is, depend on the repository:

```toml
[dependencies]
yggy-sdk = { git = "https://github.com/yggy-tech/yggy-sdk-rust" }
```

## Example

List the projects your key can see:

```rust
use reqwest::header::{HeaderMap, HeaderValue};
use yggy_sdk::apis::{configuration::{ApiKey, Configuration}, projects_api};

#[tokio::main]
async fn main() -> Result<(), Box<dyn std::error::Error>> {
    let mut headers = HeaderMap::new();
    headers.insert("x-yggy-organization-id", HeaderValue::from_static("acme-corp"));

    let mut configuration = Configuration::new();
    configuration.client = reqwest::Client::builder().default_headers(headers).build()?;
    configuration.api_key = Some(ApiKey { prefix: None, key: std::env::var("YGGY_API_KEY")? });

    let response = projects_api::list_projects(&configuration, None, None, None, None, None).await?;
    for project in response.projects {
        println!("{}", project.name);
    }
    Ok(())
}
```

## Known limitation

The generated `upload_document` does not send the file part yet. Upload documents with the [yggy CLI](https://github.com/yggy-tech/yggy-cli) or the REST API until a wrapper lands.

## Authenticate

Create an API key in yggy under **Developers → API keys** and keep it in an environment variable. A key that belongs to one organization needs nothing else. A personal key can see several organizations, so name the one you want in the `x-yggy-organization-id` header, by id or slug, as the example does.

See [Authentication](https://docs.yggy.tech/developers/authentication/) for key types and permissions.

## What you can call

Projects, documents (upload, status, extracted facts, download, retry), questions over a project or a whole organization, chat, entity lookup by identity, the ontology overview and graph exports. The [API reference](https://docs.yggy.tech/developers/rest/reference/) lists every operation with its parameters. For a first walkthrough, follow the [quickstart](https://docs.yggy.tech/developers/quickstart/).

## Generated code

Everything except this file is generated from the yggy OpenAPI document, so a change here is overwritten by the next sync. Report bugs or request an operation by opening an issue in this repository, or write to [support](https://yggy.tech/support).

## License

Apache-2.0. See [LICENSE](LICENSE).
