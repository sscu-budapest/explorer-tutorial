# Hungarian Elections

```{include} ../homes/hungarian_elections.md
```

## ERD

> this is an [ERD Diagram](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model) / [Schema Diagram](https://en.wikipedia.org/wiki/Database_schema) mix, explained clearly here. Maybe


```{mermaid}
erDiagram
  affiliation {    
    VARCHAR party__pid FK     
    VARCHAR org__nid FK 
  }
  party {    
    VARCHAR pid PK 
  }
  nominating_organization {    
    VARCHAR nid PK 
  }
  candidate {    
    VARCHAR cid PK 
  }
  district_hierarchy {    
    VARCHAR parent__gid FK     
    VARCHAR child__gid FK 
  }
  geographical_unit {    
    VARCHAR name      
    VARCHAR level_info      
    VARCHAR gid PK 
  }
  election {    
    BOOLEAN is_individual      
    DATETIME start_date      
    VARCHAR eid PK 
  }
  election_precinct {    
    VARCHAR name      
    VARCHAR geo_info      
    FLOAT eligible_voters      
    BOOLEAN external_votes      
    VARCHAR geo_parent__gid FK     
    VARCHAR election__eid FK     
    VARCHAR pid PK 
  }
  vote_record {    
    INTEGER vote_count      
    VARCHAR org__nid FK     
    VARCHAR precinct__pid FK     
    VARCHAR vid PK 
  }
  affiliation ||--|{ party : "party__pid -> pid"
  affiliation ||--|{ nominating_organization : "org__nid -> nid"
  district_hierarchy ||--|{ geographical_unit : "child__gid -> gid; parent__gid -> gid"
  election_precinct ||--|{ geographical_unit : "geo_parent__gid -> gid"
  election_precinct ||--|{ election : "election__eid -> eid"
  vote_record ||--|{ election_precinct : "precinct__pid -> pid"
  vote_record ||--|{ nominating_organization : "org__nid -> nid"
```


## Exploration / Analysis



## Tables

> There are 9 tables




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Affiliation Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/affiliation.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 257 × 2 (6.92 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/affiliation-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Candidate Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/candidate.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 0 × 1 (0.01 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/candidate-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Nominating Organization Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/nominating_organization.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 219 × 1 (3.07 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/nominating_organization-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Election Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 28 × 3 (0.94 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**District Hierarchy Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/district_hierarchy.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 3224 × 2 (125.96 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/district_hierarchy-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Geographical Unit Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/geographical_unit.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 3229 × 3 (128.04 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/geographical_unit-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Party Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/party.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 206 × 1 (2.66 kB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/party-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Election Precinct Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election_precinct.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 272194 × 7 (25.87 MB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:02
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election_precinct-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




:::::{panels} :column: col-12

::::{div} row

```{div} col-9
**Vote Record Table**
```

```{div} col-3
 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/vote_record.csv">{badge}`Download CSV,badge-primary`</a>
```
::::

^^^
::::{div} row

```{div} col-4
**Size**: 1996280 × 4 (49.57 MB)
```

```{div} col-5
**Last Changed**: 2022-05-15 20:03
```

```{div} col-3

 <a href="https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/vote_record-profile.html">{badge}`Open Table Profile,badge-success`</a>

```

::::

:::::




## Sources

- project url: https://github.com/sscu-budapest/electiondata
- data downloaded from
  - https://valtor.valasztas.hu
  - https://valtor.valasztas.hu/valtort/jsp/tmd1.jsp?TIP=2

