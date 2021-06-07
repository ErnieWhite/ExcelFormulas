# Convert Basis # to a Basis Name

## Non table version
```

```

## Table Version

```
=IF(LEFT([@Formula], 1) = "$", "NET", SWITCH(IFERROR(VALUE([@[Basis '#]]), -1),

```
