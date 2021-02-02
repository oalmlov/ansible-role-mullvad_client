# mullvad_client

A role to install and configure the mullvad linux client.

## Table of content

* [Default Variables](#default-variables)
  * [mullvad_client_base_url](#mullvad_client_base_url)
  * [mullvad_connection](#mullvad_connection)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### mullvad_client_base_url

Base URL where binary files are downloaded from.

#### Default value

```YAML
mullvad_client_base_url: https://mullvad.net/download/app
```

### mullvad_connection

A dictionary containing information to setup your connection. Either set or ommit 'servername' to connect to a specific server or choose one at random by country and city.

#### Default value

```YAML
mullvad_connection:
  account_id: ''
  relay:
    type: ''
    country: ''
    city: ''
  generate_wg_keys: true
  connect_on_install: true
  connect_on_startup: true
```

#### Example usage

```YAML
mullvad_connection:
  account_id: 123456789
  relay:
    type: wireguard
    country: se
    city: got
    servername: se9-wireguard
  generate_wg_keys: true
  connect_on_install: true
  connect_on_startup: true
```

## Dependencies

None.

## License

MIT

## Author

oalmlov
