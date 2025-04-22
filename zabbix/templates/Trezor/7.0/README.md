
# Template ModBus Trezor

## Overview

For Zabbix version: 7.0 and higher  
The template to monitor PLC Trezor

## Setup

For debug ModeBus use Windows program {QModMaster}[https://automatizace.hw.cz/qmodmaster-testovaci-programek-pro-modbus-rtutcp.html]

## Zabbix configuration

No specific Zabbix configuration is required.

### Macros used

|Name|Description|Default|
|----|-----------|-------|
{$MODBUS_ADDRESS}|<p>-</p>|0|
{$MODBUS_COUNT}|<p>-</p>|8|
{$MODBUS_ENDPOINT}|<p>-</p>|10.15.1.215:502|
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
|modbus|Trezor readings|<p>Read value from PLC by ModeBus</p>|ZABBIX_AGENT2|modbus.get[tcp://{$MODBUS_ENDPOINT},{$MODBUS_SLAVEID},{$MODBUS_FUNCTION},{$MODBUS_ADDRESS},{$MODBUS_COUNT},{$MODBUS_TYPE}]|
|trezor|Lock|<p>Lock value</p>|DEPENDENT ITEM|zbx.value0|
|trezor|Doors|<p>Doors value</p>|DEPENDENT ITEM|zbx.value1|

## Feedback

Please report any issues with the template at https://open-tech.cz
