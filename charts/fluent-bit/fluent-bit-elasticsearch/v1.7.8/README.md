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

## Output - Elasticsearch (Elastic Cloud)


To send the logs to elastic cloud's elasticsearch, do the following changes in values.yaml, update with cloud_id, cloud_auth of your [elastic cloud](https://docs.fluentbit.io/manual/pipeline/outputs/elasticsearch).
```sh
  [OUTPUT]
      Name es
      Match kube.*
      Logstash_Format On
      Logstash_Prefix logs
      tls On
      tls.verify Off
      cloud_id XXXXXXXXXXXXXXX
      cloud_auth XXXXXXXXXXXXXXX
      Retry_Limit False
      Trace_Output On
      Trace_Error On
   ```

    


 
