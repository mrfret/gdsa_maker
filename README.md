##CURRENTLY NOT WORKING

## All credit for this goes to l3uddz. I only edited documentation for easier understanding.

# Utility to easily make google service accounts

# Install:
Install python3 and git if you haven't already:
```
sudo apt update -yqq && sudo apt install python3.10 python3-pip -yqq && sudo apt install git -yqq
```

Then for gdsa-maker:
```
sudo git clone https://github.com/mrfret/gdsa_maker && cd gdsa_maker && sudo pip3 install -r requirements.txt
```

# Authorize:
```
python3 sa_maker.py authorize
```
This will create the default config.

# Edit config:
```
sudo nano config.json
```
```
{
  "client_id": "CLIENT_ID_HERE",
  "client_secret": "CLIENT_SECRET_HERE",,
  "project_id": "PROJECT_ID_HERE"
  "service_account_folder": "/root/gdsa_maker/service_accounts"
}
```
Make sure you use the project ID and not just the name. Most of the time they are the same,
but sometimes can be different like:

projectx-364758

Check here:

https://console.cloud.google.com/cloud-resource-manager?walkthrough_id=resource-manager--create-project&_ga=2.113127300.1022120207.1667047847-124764366.1653830517

Then run authorize again

# Basic command:
  
```
python3 sa_maker.py create-service-accounts -n <prefix_of_sa> -a <number_of_sa_to_create>
```
# If you get an error message about API not being enabled, simply follow the link provided in the error and enable the required API

Usage: sa_maker.py [OPTIONS] COMMAND [ARGS]...

  service_account_maker

```
Options:
  --version           Show the version and exit.
  -v, --verbose       Adjust the logging level
  --config-path FILE  Configuration filepath  [default:
                      /root/gdsa_maker/config.json]
  --log-path FILE     Log filepath  [default: /root/gdsa_maker/activity.log]
  --token-path FILE   Token filepath  [default: /root/gdsa_maker/token.json]
  --help              Show this message and exit.

Commands:
  authorize                Authorize Google Account
  create-group             Create group
  create-service-accounts  Create service accounts
  create-teamdrive         Create teamdrive
  list-group-users         List users for a group
  list-groups              List existing groups
  list-service-accounts    List existing service accounts
  list-teamdrive-users     List users for a teamdrive
  list-teamdrives          List existing teamdrives
  list-user-accounts       List user accounts
  remove-group             Remove a group
  remove-service-accounts  Remove service accounts
  remove-teamdrive-users   Remove users from a teamdrive
  set-group-users          Set users for a group
  set-teamdrive-group      Set group for a teamdrive
  set-teamdrive-users      Set users for a teamdrive
  
  Args:
  --name, -n          Name prefix
  --amount, -a        Amount of service accounts to create
  --domain, -d        Domain of the G Suite account
  --key-prefix, -k    Name prefix of service accounts
  ```
  
