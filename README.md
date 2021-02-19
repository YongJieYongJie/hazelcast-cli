# Hazelcast CLI

An _extremely_ thin wrapper around the client console app by Hazelcast, for
connecting to a running Hazelcast cluster and performing various operations.


## Example Usage

```shell
> curl --location --remote-name https://raw.githubusercontent.com/YongJieYongJie/hazelcast-cli/main/hz-cli
> chmod u+x ./hz-cli
> ./hz-cli -h <host-ip> -p <port, e.g. 5701> -u <username>

# After connecting to the cluster...

# List all the available distributed objects.
hazelcast[default] > instances

# Change to the relevant object we are interested in.
hazelcast[default] > ns <name-of-map>

# Perform relevant operation: listing stats, clearing, etc.
hazelcast[name-of-map] > m.stats
hazelcast[name-of-map] > m.clear
```


## Credits

The underlying client for actually connecting to the Hazelcast cluster:
ClientConsoleApp.java at
https://github.com/hazelcast/hazelcast/blob/master/hazelcast/src/main/java/com/hazelcast/client/console/ClientConsoleApp.java

Inspiration: StackOverflow discussion at
https://stackoverflow.com/a/41306500/5821101.