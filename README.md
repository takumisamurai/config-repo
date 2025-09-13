# config-repo
configuration repository

This Repository stores all the configuration information required by all micro services across environments and versions.

It centralizes config management, helps maintain consistency, and simplifies deployment and environment management.

This repository acts as a single source of truth for configuration properties such as database URLs, API keys, feature flags, and environment-specific settings.

The config server reads configurations from the Git repository and serves them to client microservices dynamically.

All microservices are configured to fetch their configuration from this config server at startup and refresh on changes if necessary.




Spring Cloud Config Server merges configuration files in a specific order of precedence when you request a config for an application and profile, such as http://localhost:8888/user-service/dev. Here’s why it fetches multiple files like application.yml, application-dev.yml, and user-service-dev.yml:

Order of Property Sources and Precedence Rules
application.yml

Global/shared config applied to all applications regardless of name or profile.

application-{profile}.yml (e.g., application-dev.yml)

Global config specific to the Spring profile (dev, prod, etc.), overrides global defaults.

{application}.yml (e.g., user-service.yml)

Application-specific config that applies regardless of profile.

{application}-{profile}.yml (e.g., user-service-dev.yml)

Most specific config for the given application and profile, highest precedence.
