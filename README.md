# Victor - A CLI for Heroic

##### Why 'Victor`
because it was one of the options for synoyms of `heroic` or `hero`.


# Config 

victor will search ~/.victor.yaml or `-c/--config` for a config. The only **required** entry is `victor.heroic.url` 

```yaml
victor:
  heroic:
    url: http://heroic.local #required
    limits: 5000
    features: 
      - com.spotify.heroic.distributed_aggragations
    
```

`--help` is youi friend
Uses:

`victor key-inspect` : Find all `$keys`. Queries the `/metadata/key-suggest` endpoint. 

`victor tag-inspect`: Find all values for a specific tag. Queries the `/metadata/tag-value-suggest` endpoint

`victor high-cardinality`: Find tags with high cardinality(use `--threshold`). First finds all keys using `key-inspect`, which is used to make smaller queries to `/metadata/tagkey-count` endpoint.



Todo:

`victor tag-discovery`: Find all applicable tags/values for a given query 

`victor query`: Run a query, print results (datapoints included)


