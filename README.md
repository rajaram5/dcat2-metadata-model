# dcat2-metadata-model
WIP repository for a dcat2 based FDP metadata model.

- Model written in [SHACL](https://www.w3.org/TR/shacl/), based on the [DCAT2 spec](https://www.w3.org/TR/vocab-dcat-2/).
- Cardinalities are a rough draft, by no means final.
- External shapes (`odrl:Policy`, `dct:Standard`, etc) are referred to by `sh:class` and not by `sh:node`.
- Text based literals are defined as `sh:Literal` instead of `xsd:string`.
- `dcat:Relationship` could be [used](https://www.w3.org/TR/vocab-dcat-2/#qualified-relationship) to define the relation between the (to be defined) `:RepositoryShape` resource and a `dcat:Catalog`.
  - Nonsensical draft of the `dcat:Relation` in [`example-data.ttl`](example-data.ttl#L39-L43).
- Can we call this a [DCAT Profile](https://www.w3.org/TR/vocab-dcat-2/#profiles)?
  - Could use [`dx-prof`](https://www.w3.org/TR/dx-prof/) to describe the profile?
- Rough draft of a re3data `Repository` shape, based on [re3data/ontology](https://github.com/re3data/ontology).
- [`example-data.ttl`](example-data.ttl) contains example instance data with _all_ possible properties.

## Extensions
- Mocked a 'workflow' type extension in [shape definitions](workflow-extension-shapes.ttl) and [example instance data](workflow-extension-example-data.ttl).
- Example data [restates](workflow-extension-example-data.ttl#L5) the subproperty nature of the linking predicate between a `dcat:Catalog` and a `wfx:Workflow`.
