# MS SQL Server Reserved Keywords Grouped by Level

Total SQL Server / Transact-SQL reserved keywords: **185**

> Note: This grouping is for learning purposes. SQL Server itself does not officially classify reserved keywords as Basic, Intermediate, or Advanced.

---

# 1. Basic Keywords

Common keywords used in everyday SQL queries.

| SR# | Keyword |
|---:|---|
| 1 | ADD |
| 2 | ALL |
| 3 | ALTER |
| 4 | AND |
| 5 | ANY |
| 6 | AS |
| 7 | ASC |
| 8 | BEGIN |
| 9 | BETWEEN |
| 10 | BY |
| 11 | CASE |
| 12 | CHECK |
| 13 | COLUMN |
| 14 | COMMIT |
| 15 | CONSTRAINT |
| 16 | CREATE |
| 17 | CURRENT |
| 18 | CURRENT_DATE |
| 19 | CURRENT_TIME |
| 20 | CURRENT_TIMESTAMP |
| 21 | DATABASE |
| 22 | DECLARE |
| 23 | DEFAULT |
| 24 | DELETE |
| 25 | DESC |
| 26 | DISTINCT |
| 27 | DROP |
| 28 | ELSE |
| 29 | END |
| 30 | EXEC |
| 31 | EXECUTE |
| 32 | EXISTS |
| 33 | FOR |
| 34 | FOREIGN |
| 35 | FROM |
| 36 | FULL |
| 37 | FUNCTION |
| 38 | GROUP |
| 39 | HAVING |
| 40 | IF |
| 41 | IN |
| 42 | INDEX |
| 43 | INNER |
| 44 | INSERT |
| 45 | INTO |
| 46 | IS |
| 47 | JOIN |
| 48 | KEY |
| 49 | LEFT |
| 50 | LIKE |
| 51 | NOT |
| 52 | NULL |
| 53 | ON |
| 54 | OR |
| 55 | ORDER |
| 56 | OUTER |
| 57 | PRIMARY |
| 58 | PRINT |
| 59 | PROCEDURE |
| 60 | RIGHT |
| 61 | ROLLBACK |
| 62 | SELECT |
| 63 | SET |
| 64 | TABLE |
| 65 | THEN |
| 66 | TO |
| 67 | TOP |
| 68 | TRAN |
| 69 | TRANSACTION |
| 70 | TRIGGER |
| 71 | TRUNCATE |
| 72 | UNION |
| 73 | UNIQUE |
| 74 | UPDATE |
| 75 | USE |
| 76 | USER |
| 77 | VALUES |
| 78 | VIEW |
| 79 | WHEN |
| 80 | WHERE |
| 81 | WHILE |
| 82 | WITH |

---

# 2. Intermediate Keywords

Keywords used in joins, permissions, transactions, indexing, locking, conversions, and query options.

| SR# | Keyword |
|---:|---|
| 83 | AUTHORIZATION |
| 84 | BACKUP |
| 85 | BREAK |
| 86 | CASCADE |
| 87 | CHECKPOINT |
| 88 | CLOSE |
| 89 | CLUSTERED |
| 90 | COALESCE |
| 91 | COLLATE |
| 92 | CONTAINS |
| 93 | CONTINUE |
| 94 | CONVERT |
| 95 | CROSS |
| 96 | CURRENT_USER |
| 97 | CURSOR |
| 98 | DEALLOCATE |
| 99 | DENY |
| 100 | DISK |
| 101 | DISTRIBUTED |
| 102 | DOUBLE |
| 103 | ESCAPE |
| 104 | EXCEPT |
| 105 | EXIT |
| 106 | FETCH |
| 107 | FILE |
| 108 | FILLFACTOR |
| 109 | GRANT |
| 110 | HOLDLOCK |
| 111 | IDENTITY |
| 112 | IDENTITY_INSERT |
| 113 | IDENTITYCOL |
| 114 | INTERSECT |
| 115 | LOAD |
| 116 | MERGE |
| 117 | NATIONAL |
| 118 | NOCHECK |
| 119 | NONCLUSTERED |
| 120 | NULLIF |
| 121 | OF |
| 122 | OFF |
| 123 | OFFSETS |
| 124 | OPEN |
| 125 | OPTION |
| 126 | OVER |
| 127 | PERCENT |
| 128 | PIVOT |
| 129 | PRECISION |
| 130 | PROC |
| 131 | PUBLIC |
| 132 | RAISERROR |
| 133 | READ |
| 134 | READTEXT |
| 135 | REFERENCES |
| 136 | REPLICATION |
| 137 | RESTORE |
| 138 | RESTRICT |
| 139 | RETURN |
| 140 | REVERT |
| 141 | REVOKE |
| 142 | ROWCOUNT |
| 143 | ROWGUIDCOL |
| 144 | RULE |
| 145 | SAVE |
| 146 | SCHEMA |
| 147 | SESSION_USER |
| 148 | SETUSER |
| 149 | SOME |
| 150 | STATISTICS |
| 151 | SYSTEM_USER |
| 152 | TABLESAMPLE |
| 153 | TEXTSIZE |
| 154 | TRY_CONVERT |
| 155 | UNPIVOT |
| 156 | UPDATETEXT |
| 157 | VARYING |
| 158 | WAITFOR |
| 159 | WITHIN GROUP |
| 160 | WRITETEXT |

---

# 3. Advanced Keywords

Specialized keywords used for full-text search, external access, DBCC/admin operations, semantic search, query plans, and lower-level SQL Server features.

| SR# | Keyword |
|---:|---|
| 161 | BROWSE |
| 162 | BULK |
| 163 | COMPUTE |
| 164 | CONTAINSTABLE |
| 165 | DBCC |
| 166 | DUMP |
| 167 | ERRLVL |
| 168 | EXTERNAL |
| 169 | FREETEXT |
| 170 | FREETEXTTABLE |
| 171 | GOTO |
| 172 | KILL |
| 173 | LINENO |
| 174 | OPENDATASOURCE |
| 175 | OPENQUERY |
| 176 | OPENROWSET |
| 177 | OPENXML |
| 178 | PLAN |
| 179 | RECONFIGURE |
| 180 | SECURITYAUDIT |
| 181 | SEMANTICKEYPHRASETABLE |
| 182 | SEMANTICSIMILARITYDETAILSTABLE |
| 183 | SEMANTICSIMILARITYTABLE |
| 184 | SHUTDOWN |
| 185 | TSEQUAL |

---

# Azure Synapse Analytics Extra Reserved Keyword

| SR# | Keyword | Level |
|---:|---|---|
| 186 | LABEL | Intermediate |

---

# Usage Note

Reserved keywords can be used as object names only when delimited with square brackets.

```sql
CREATE TABLE [TABLE] (
    [SELECT] INT
);
