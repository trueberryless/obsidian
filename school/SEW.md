3 Schritte: Datenquelle definieren, Query definiere, ausführen

async bei Interface noch nicht, weil kein Body, somit kein await. Deswegen erst bei Implementierung.

ARepository brauchen wir für Datenzugriff (Schreiben, Lesen, ...). Deswegen Ausimplementierung.

Das DbSet sorgt für die korrekte Verbindung zwischen Objekten und Datenbank. Mithilfe des DbSets werden alle Änderung in beide Richtungen synchronisiert.

## Agenda

- Expression Class anschauen
- Dependency Injection