# Get file ownership info
ls -l

# Grep
## Search multiple files
grep "stringToSearchFor" *.properties

## stat command
Get meta data for a file.

stat ~/someFile

# systemctl
## Find service
systemctl -l | grep {SERVICE_NAME}

## Status
systemctl status {SERVICE_NAME}

## Show properties
systemctl show --property=User,DynamicUser,MainPID,Group {SERVICE_NAME}

