## Go

These settings apply only when `--go` is specified on the command line.

``` yaml $(go)
go:
  license-header: MICROSOFT_APACHE_NO_VERSION
  namespace: servicebus
  clear-output-folder: true
```

### Go multi-api

``` yaml $(go) && $(multiapi)
batch:
  - tag: package-2017-04
  - tag: package-2015-08
```

### Tag: package-2017-04 and go

These settings apply only when `--tag=package-2017-04 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2017-04' && $(go)
output-folder: $(go-sdk-folder)/services/servicebus/mgmt/2017-04-01/servicebus
```

### Tag: package-2015-08 and go

These settings apply only when `--tag=package-2015-08 --go` is specified on the command line.
Please also specify `--go-sdk-folder=<path to the root directory of your azure-sdk-for-go clone>`.

``` yaml $(tag) == 'package-2015-08' && $(go)
output-folder: $(go-sdk-folder)/services/servicebus/mgmt/2015-08-01/servicebus
```