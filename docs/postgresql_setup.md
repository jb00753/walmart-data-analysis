# Local PostgreSQL setup

PostgreSQL 18 is installed and its Windows service is running on this computer. The project database will be named `m5_walmart`.

Open PowerShell and run:

```powershell
& 'C:\Program Files\PostgreSQL\18\bin\createdb.exe' -h 127.0.0.1 -p 5432 -U postgres -W m5_walmart
```

Enter the PostgreSQL `postgres` account password at the prompt. The password will not appear as you type. Do not put it in this repository or send it in chat.

Verify the database exists:

```powershell
& 'C:\Program Files\PostgreSQL\18\bin\psql.exe' -h 127.0.0.1 -p 5432 -U postgres -W -d m5_walmart -c 'SELECT current_database();'
```

The expected result is `m5_walmart`. If `createdb` reports that the database already exists, run the verification command before making any changes.

The database is local to this computer. The raw M5 CSV files remain in `data/raw/m5-forecasting-accuracy/` and are ignored by Git.
