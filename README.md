# config-repo
configuration repository
This Repository stores all the configuration information required by all micro services across environments and versions.
It centralizes config management, helps maintain consistency, and simplifies deployment and environment management.
This repository acts as a single source of truth for configuration properties such as database URLs, API keys, feature flags, and environment-specific settings.

The config server reads configurations from the Git repository and serves them to client microservices dynamically.
All microservices are configured to fetch their configuration from this config server at startup and refresh on changes if necessary.

