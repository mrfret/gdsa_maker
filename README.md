# service_account_maker

All credit to l3uddz...

Install:
```
sudo git clone https://github.com/mrfret/gdsa_maker && cd gdsa_maker && sudo pip3 install -r requirements.txt
```

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
  authorize               Authorize Google Account
  create-accounts         Create service accounts
  create-group            Create group
  create-teamdrive        Create teamdrive
  list-accounts           Retrieve existing service accounts
  list-group-users        Lists users for a group
  list-groups             Retrieve existing groups
  list-teamdrive-users    Lists users for a teamdrive
  list-teamdrives         Retrieve existing teamdrives
  remove-group            Remove a group
  remove-teamdrive-users  Remove users from a teamdrive
  set-group-users         Set users for a group
  set-teamdrive-users     Set users for a teamdrive
  
Args:
  --name, -n          Name prefix
  --amount, -a        Amount of service accounts to create
  --domain, -d        Domain of the G Suite account
  --key-prefix, -k    Name prefix of service accounts
  ```
  
  Basic command:
  
  ```
  python3 sa_maker.py create-accounts -n <prefix_of_sa> -a <number_of_sa_to_create>
  ```

