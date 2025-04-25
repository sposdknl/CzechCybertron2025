
# Template ModBus Velin

## Overview

For Zabbix version: 7.0 and higher  
The template to monitor PLC Velin

## Setup

For debug ModeBus use Windows program [QModMaster](https://automatizace.hw.cz/qmodmaster-testovaci-programek-pro-modbus-rtutcp.html)

## Zabbix configuration

No specific Zabbix configuration is required.

### Macros used

|Name|Description|Default|
|----|-----------|-------|
{$MODBUS_ADDRESS}|<p>-</p>|8191|
{$MODBUS_COUNT}|<p>-</p>|20|
{$MODBUS_ENDPOINT}|<p>-</p>|10.15.1.210:502|
{$MODBUS_FUNCTION}|<p>-</p>|2|
{$MODBUS_SLAVEID}|<p>-</p>|1|
{$MODBUS_TYPE}|<p>-</p>|bit|

## Template links

There are no template links in this template.

## Discovery rules

|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
|-|<p>-</p>|-|-|

## Items collected

|Group|Name|Description|Type|Key and additional info|
|-----|----|-----------|----|---------------------|
|modbus|Velin readings|<p>Read value from PLC by ModeBus</p>|ZABBIX_AGENT2|modbus.get[tcp://{$MODBUS_ENDPOINT},{$MODBUS_SLAVEID},{$MODBUS_FUNCTION},{$MODBUS_ADDRESS},{$MODBUS_COUNT},{$MODBUS_TYPE}]|
|velin|Light|<p>Light value</p>|DEPENDENT ITEM|zbx.value3|
|velin|Gen 1|<p>Gen 1 value</p>|DEPENDENT ITEM|zbx.value4|
|velin|Gen 2|<p>Gen 2 value</p>|DEPENDENT ITEM|zbx.value5|
|velin|Filling pump up|<p>Filling pump up value</p>|DEPENDENT ITEM|zbx.value6|
|velin|Filing pump down|<p>Filing pump down value</p>|DEPENDENT ITEM|zbx.value7|
|velin|Main valve|<p>Main valve value</p>|DEPENDENT ITEM|zbx.value8|
|velin|Auxiliary pump up|<p>Auxiliary pump up value</p>|DEPENDENT ITEM|zbx.value9|
|velin|Auxiliary pump down|<p>Auxiliary pump down value</p>|DEPENDENT ITEM|zbx.value10|
|velin|Safety|<p>Safety value</p>|DEPENDENT ITEM|zbx.value11|
|velin|WL Error|<p>WL Error value</p>|DEPENDENT ITEM|zbx.value12|
|velin|WL Bypass|<p>WL Bypass  value</p>|DEPENDENT ITEM|zbx.value13|

## Feedback

Please report any issues with the template at https://open-tech.cz
