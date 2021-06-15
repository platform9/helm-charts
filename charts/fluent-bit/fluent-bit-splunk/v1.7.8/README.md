# Fluent Bit Helm Chart

[Fluent Bit](https://fluentbit.io) is a fast and lightweight log processor and forwarder or Linux, OSX and BSD family operating systems.

## Installation

To add the `pf9` helm repo, run:

```sh
helm repo add pf9 https://platform9.github.io/helm-charts
```

To install a release named `fluent-bit`, run:

```sh
helm install fluent-bit pf9/fluent-bit
```

## Output - Splunk 

```sh
To send the logs to Splunk cloud, do the following changes in values.yaml

  [OUTPUT]
    Name splunk
    Match *
    Host XXXXXXXXXXXXXXXXXXX (Hostname of the target Splunk Cloud service)
    Port 8088
    Splunk_Token XXXXXXXXXXXXXXXXXXX (Specify the Authentication Token for the HTTP Event Collector interface)
    tls On
    tls.verify Off

```

 