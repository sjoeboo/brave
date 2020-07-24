# Brave - A CLI for Heroic

##### Why 'Brave`
because it was one of the options for synoyms of `heroic` or `hero`.


# Config 

brave will search ~/.brave.yaml or `-c/--config` for a config. The only **required** entry is `brave.heroic.url` 

```yaml
brave:
  heroic:
    url: http://heroic.local #required
    limits: 5000
    features: 
      - com.spotify.heroic.distributed_aggragations
    
```

`--help` is youi friend
Uses:

`brave key-inspect` : Find all `$keys`. Queries the `/metadata/key-suggest` endpoint. 

`brave tag-inspect`: Find all values for a specific tag. Queries the `/metadata/tag-value-suggest` endpoint

`brave high-cardinality`: Find tags with high cardinality(use `--threshold`). First finds all keys using `key-inspect`, which is used to make smaller queries to `/metadata/tagkey-count` endpoint.



Todo:

`brave tag-discovery`: Find all applicable tags/values for a given query 

`brave query`: Run a query, print results (datapoints included)


