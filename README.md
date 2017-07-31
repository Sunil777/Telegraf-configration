This role was derived from the Ansible lightbulb repository and was originally 
authored by Sunil Malik

## Requirements

None

## Role Variables

Available variables are listed below with default values (see `defaults/main.yml`):

    telegraf_influxdb_url: http://localhost:8086

This variable defines the InfluxDB system URL that Telegraf should feed its metrics.

    telegraf_influxdb_db_name: telegraf

This variable defines the name of the InfluxDB database the metrics should be stored.

## Dependencies

None

## Example Playbook

The most basic usage of this role in a play is as follows:

    - hosts: servers
      roles:
         - role: 'sunil.telegraf'

To setup a basic telegraf simple and direct its metrics to an external InfluxDB
system with a database name of "simple_stats" you could use any variable 
source to override the role's defaults values such as role params like this:

    - hosts: servers
      roles:
         - role: 'sunil.telegraf'
           telegraf_influxdb_url: 'http://influxdb.example.net:8086/'
           telegraf_influxdb_db_name: 'simple_stats'

Other means include play `vars`, inventory variables and `extra_vars` on the 
command line to name a few more. 

## Contributions and Feedback

Any contributions are welcome. For any bugs or feature requests,
please open an issue through Github.


## Author

Originally created by [James S Martin](https://github.com/jsmartin) and was 
ported into this role by [Sunil Malik](https://github.com/sunil777).

