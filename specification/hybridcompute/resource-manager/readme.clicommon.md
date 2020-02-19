<!-- region Generated -->
# Dns
This directory contains the Cli common model for the Dns service.

> Metadata
``` yaml
# Migrated from Powershell's readme

title: 'ConnectedMachine'
```

``` yaml
# Migrated from Powershell's readme

clicommon:
    cli-directive:
      - select: 'operationGroup'
        where:
            operatoinGroup: 'operations'
        set:
            hide: true
      - select: 'operation'
        where:
            operationGroup: 'machines'
            operation: '(reconnect|create_or_update|update)'
        set:
            remove: true
      - select: 'operation'
        where:
            operationGroup: 'machine_extensions'
            operation: '(create_or_update|update|delete|get|list)'
        set:
            remove: true
```