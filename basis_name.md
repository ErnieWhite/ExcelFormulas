## Convert Basis # to a Basis Name

```
=IF(LEFT(INDIRECT(ADDRESS(ROW(),COLUMN()+1)),1)="$","NET",SWITCH(IFERROR(VALUE(INDIRECT(ADDRESS(ROW(),COLUMN()-1))),-1), 1, "LIST",
2, "INTERNAL",
3, "UMSP",
4, "CMP",
5, "STD-COST",
6, "REP-COST",
8, "AVG-COST",
9, "LASTCOST",
21, "Lnd Cost",
22, "Avg Lnd",
25, "Ord COGS",
28, "Ord Comm",
29, "Strgc List",
30, "Strgc Cost",
31, "AVG-COST",
INDIRECT(ADDRESS(ROW(),COLUMN()-1))
))
```
