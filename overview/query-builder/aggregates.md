# Aggregates

The query builder also provides a variety of aggregate methods such as `count`, `max`, `min`, and `sum`. You may call any of these methods after constructing your query:

```text
var getResults = query.from('users')
    .count();
writeDump(getResults);
```

```text
var getResults = query.from('users')
    .max('age');
writeDump(getResults);
```

```text
var getResults = query.from('users')
    .min('age');
writeDump(getResults);
```

Of course, you may combine these methods with other clauses:

```text
var getResults = query.from('users')
    .where('active', '=', 1)
    .max('age');
writeDump(getResults);
```

