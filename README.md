# postgres-dynamic-query
postgres-dynamic-query

```
CREATE OR REPLACE function dValue() return numerix AS $func$
declare
  sSchema varchar2(20);
  vValue numeric;
begin
  EXECUTE 'SELECT value from '||sSchema||'.SavingDataTable' into vValue;
  return vValue;
end
$func$  LANGUAGE plpgsql;
```
