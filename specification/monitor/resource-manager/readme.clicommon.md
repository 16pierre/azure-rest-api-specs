<!-- region Generated -->
# Dns
This directory contains the Cli common model for the Dns service.

> Metadata


``` yaml
# Migrated from Powershell's readme
title: Monitor
clicommon:
    cli-directive:
      - select: 'enumValue'
        where:
            enumSchema: 'comparison_operation_type'
            enumValue: 'equals'
        set:
            enumValue: 'equal'
      - select: 'property'
        where:
            schemaObject: 'activity_log_alert_leaf_condition'
            property: 'equals'
        set:
            name: 'equal'
      - select: 'operationGroup'
        where:
            operationGroup: 'metric_alerts_status'
        set:
            name: 'metric_alert_status'
      - select: 'operation'
        where:
            operationGroup: 'activity_log_alerts'
            operation: 'update'
        hide: true
      - select: 'operation'
        where:
            operationGroup: 'metric_alerts'
            operation: '^(create_or_update|update)$'
        hide: true
      - select: 'parameter'
        where:
            operationGroup: '^(metric_alerts|alert_rules|alert_rule_incidents)$'
            parameter: 'rule_name'
        set:
            name: name
      - select: 'property'
        where:
            objectSchema: '^(alert_rule_resource|alert_rule_resource_patch)$'
            property: 'is_enabled'
        set:
            name: 'enabled'
      - select: 'operation'
        where:
            operationGroup: 'alert_rules'
            operation: '^(create_or_update|delete|update)$'
        hide: true
      - select: 'operation'
        where:
            operationGroup: 'log_profiles'
            operation: '^(create_or_update|update)$'
        hide: true
      - select: 'property'
        where:
            objectSchema: '^(autoscale_setting_resource|autoscale_setting_resource_patch)$'
            property: 'target_resource_uri'
        set:
            name: 'target_resource_id'
      - where:
            objectSchema: '^(action_group|action_group_resource)$'
            property: 'group_short_name'
        name: 'short_name'
      - where:
            operationGroup: 'action_groups'
            operation: 'update'
        remove: true
      - where:
            operationGroup: 'metrics'
            parameter: 'interval'
        alias: TimeGrain
      - where:
            operationGroup: 'metrics'
            parameter: 'resource_uri'
        name: 'resource_id'
      - where:
            operationGroup: 'metric_definitions'
            operation: 'list'
        hide: true
      - where:
            operationGroup: 'scheduled_query_rules'
            parameter: 'rule_name'
        name: name
      - where:
            operationGroup: 'scheduled_query_rules'
            operation: '^(create_or_update|update)$'
        hide: true
      - where:
            operationGroup: 'diagnostic_settings_category'
            parameter: 'resource_uri'
        name: 'resource_id'
      - where:
            operationGroup: 'baselines'
            operation: 'list'
        remove: true
```