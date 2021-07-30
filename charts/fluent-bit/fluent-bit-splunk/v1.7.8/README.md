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


To send the logs to Splunk cloud, do the following changes in values.yaml, update with Host, Splunk_Token of your [Splunk cloud](https://docs.fluentbit.io/manual/pipeline/outputs/splunk).
```sh
  [OUTPUT]
    Name splunk
    Match *
    Host XXXXXXXXXXXXXXXXXXX (Hostname of the target Splunk Cloud service)
    Port 8088
    Splunk_Token XXXXXXXXXXXXXXXXXXX 
    tls On
    tls.verify Off
   ```
   The Splunk_Token is to Specify the Authentication Token for the [HTTP Event Collector](https://docs.splunk.com/Documentation/SplunkCloud/8.0.2006/Data/UsetheHTTPEventCollector?ref=hk) interface
    


 
