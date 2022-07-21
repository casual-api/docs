# Unique IDs
For various resources, Casual API needs to generate unique IDs for identification of a certain
resource. The format used for IDs is [Universally Unique Lexicographically Sortable Identifier (ULID)](https://github.com/ulid/spec).

These IDs are guaranteed to be unique across the API. These IDs allow you to retrieve the
timestamp of a resource creation by parsing the ID using your language's [implementation](https://github.com/ulid/spec#implementations-in-other-languages) of ULID.

```
01AN4Z07BY      79KA1307SR9X4MV3

|----------|    |----------------|
 Timestamp          Randomness
   48bits             80bits
```

You can learn more about ulid specification by reading the linked page above.

# Exceptional cases
In some cases, API might not return IDs in ULID format. This is generally the case when the
resource is derived from another source. In which case, The ID of resource retrieved from
external source is returned instead.

The example of this exceptional case is [Reddit memes resource](../../resources/memes)
