# Convert Basis # to a Basis Name

## Non table version
```
=SWITCH(left(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))),1),
"*", VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 2, LEN(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1)))))),
"X", VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 2, LEN(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1)))))),
"D", 1 / VALUE(VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 2, LEN(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))))))),
"+", 1 - VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 2, LEN([VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))))))/ 100,
"-", 1 - VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 2, LEN(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1)))))) / 100,
"G", 1 / (1 - VALUE(MID(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))), 3, LEN(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1)))))) / 100),
"$", 1,
"ERROR",
)
```

## Table Version

```
=SWITCH(LEFT([@Formula], 1),
"*", VALUE(MID([@Formula], 2, LEN([@Formula]))),
"X", VALUE(MID([@Formula], 2, LEN([@Formula]))),
"D", 1 / VALUE(VALUE(MID([@Formula], 2, LEN([@Formula])))),
"+", 1 - VALUE(MID([@Formula], 2, LEN([@Formula])))/ 100,
"-", 1 - VALUE(MID([@Formula], 2, LEN([@Formula]))) / 100,
"G", 1 / (1 - VALUE(MID([@Formula], 3, LEN([@Formula]))) / 100),
"$", 1,
"ERROR"
)
```
