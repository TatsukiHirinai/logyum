```dataview
TABLE WITHOUT ID

  value AS "Valeur",

  length(rows) AS "Occurrences"

FROM ""

FLATTEN dangerosite AS value

WHERE value

GROUP BY value

SORT value
```