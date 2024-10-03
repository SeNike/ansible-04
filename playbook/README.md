# Playbook for Installing ClickHouse, Vector, Nginx, and Lighthouse

This playbook performs the installation of the following services:
- **ClickHouse** on hosts with the `clickhouse` role.
- **Vector** on hosts with the `vector` role.
- **Nginx** on hosts with the `lighthouse` role.
- **Lighthouse** (a monitoring interface for ClickHouse) on hosts with the `lighthouse` role.

## Tasks Description

1. **Install ClickHouse** — installs and configures ClickHouse on hosts with the `clickhouse` role.
2. **Install Vector** — installs and configures Vector on hosts with the `vector` role.
3. **Install Nginx** — installs and configures Nginx on hosts with the `lighthouse` role.
4. **Install Lighthouse** — installs and configures Lighthouse on the same hosts as Nginx, as Lighthouse uses Nginx to serve the web interface.

## Parameters

- **clickhouse_version**: The version of ClickHouse to be installed, defined in the `clickhouse` role variables.
- **vector_version**: The version of Vector to be installed, defined in the `vector` role variables.
- **nginx_version**: The version of Nginx to be installed, defined in the `nginx` role variables.
- **lighthouse_version**: The version of Lighthouse to be installed, defined in the `lighthouse` role variables.

Examples of how to use these parameters can be found in the respective roles.

## Tags

Each task is tagged, allowing you to run only specific parts of the playbook:

- `clickhouse` — for installing ClickHouse.
- `vector` — for installing Vector.
- `nginx` — for installing Nginx.
- `lighthouse` — for installing Lighthouse.

### Example of Using Tags

To run only the ClickHouse installation, use the following command:

```bash
ansible-playbook site.yml --tags clickhouse
```


## Usage

To execute the playbook, run the following command:

```bash
ansible-playbook -i inventory/prod.yml site.yml
```

