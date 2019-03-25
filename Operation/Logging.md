# Logging

The privacy platform stores logs at the system, application and user levels.  This allows for robust reporting and troubleshooting in the event of errors.

## System Level Logs

Anything that a system admin does is logged.  You can gain access to these logs through the admin portal.

## Tenant Level Logs

Each operation that occurs via manual or automated means generates a log entry in the tenant log layer.  This data can be exported to performan analytics on usage and security.

## Application Level Logs

Each operation that occurs via manual or automated means generates a log entry in the application log layer.  This data can be exported to performan analytics on usage and security.

## Cloud Level Logs

Every resource that supported the operation of the platform has logging enabled.  These logs are pumped to an Azure Log Analytics resource.  You can perform various reporting on the access to these resources using the Azure Logging reporting query language.