# distinct

Filter das Ergebnis auf doppelte Objecte:

```c#
var data = await enrollments  
    .Where(e => e.Grade == 5)  
    .Select(e => e.StudentId)  
    .Distinct()  
    .ToListAsync();
```

# .ToQueryString();

Um ein IQueryable in eine SQL Abfrage oder andere Sprachen zu konvertieren, kann man .ToQueryString() verwenden:

```c#
Console.WriteLine(query.ToQueryString());
```

