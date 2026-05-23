# MS SQL Server Reserved Keywords

Total SQL Server / Transact-SQL reserved keywords: **185**

> Note: Azure Synapse Analytics has one extra reserved keyword: `LABEL`.

## Reserved Keywords

| SR# | Keyword |
|---:|---|
| 1 | ADD |
| 2 | ALL |
| 3 | ALTER |
| 4 | AND |
| 5 | ANY |
| 6 | AS |
| 7 | ASC |
| 8 | AUTHORIZATION |
| 9 | BACKUP |
| 10 | BEGIN |
| 11 | BETWEEN |
| 12 | BREAK |
| 13 | BROWSE |
| 14 | BULK |
| 15 | BY |
| 16 | CASCADE |
| 17 | CASE |
| 18 | CHECK |
| 19 | CHECKPOINT |
| 20 | CLOSE |
| 21 | CLUSTERED |
| 22 | COALESCE |
| 23 | COLLATE |
| 24 | COLUMN |
| 25 | COMMIT |
| 26 | COMPUTE |
| 27 | CONSTRAINT |
| 28 | CONTAINS |
| 29 | CONTAINSTABLE |
| 30 | CONTINUE |
| 31 | CONVERT |
| 32 | CREATE |
| 33 | CROSS |
| 34 | CURRENT |
| 35 | CURRENT_DATE |
| 36 | CURRENT_TIME |
| 37 | CURRENT_TIMESTAMP |
| 38 | CURRENT_USER |
| 39 | CURSOR |
| 40 | DATABASE |
| 41 | DBCC |
| 42 | DEALLOCATE |
| 43 | DECLARE |
| 44 | DEFAULT |
| 45 | DELETE |
| 46 | DENY |
| 47 | DESC |
| 48 | DISK |
| 49 | DISTINCT |
| 50 | DISTRIBUTED |
| 51 | DOUBLE |
| 52 | DROP |
| 53 | DUMP |
| 54 | ELSE |
| 55 | END |
| 56 | ERRLVL |
| 57 | ESCAPE |
| 58 | EXCEPT |
| 59 | EXEC |
| 60 | EXECUTE |
| 61 | EXISTS |
| 62 | EXIT |
| 63 | EXTERNAL |
| 64 | FETCH |
| 65 | FILE |
| 66 | FILLFACTOR |
| 67 | FOR |
| 68 | FOREIGN |
| 69 | FREETEXT |
| 70 | FREETEXTTABLE |
| 71 | FROM |
| 72 | FULL |
| 73 | FUNCTION |
| 74 | GOTO |
| 75 | GRANT |
| 76 | GROUP |
| 77 | HAVING |
| 78 | HOLDLOCK |
| 79 | IDENTITY |
| 80 | IDENTITY_INSERT |
| 81 | IDENTITYCOL |
| 82 | IF |
| 83 | IN |
| 84 | INDEX |
| 85 | INNER |
| 86 | INSERT |
| 87 | INTERSECT |
| 88 | INTO |
| 89 | IS |
| 90 | JOIN |
| 91 | KEY |
| 92 | KILL |
| 93 | LEFT |
| 94 | LIKE |
| 95 | LINENO |
| 96 | LOAD |
| 97 | MERGE |
| 98 | NATIONAL |
| 99 | NOCHECK |
| 100 | NONCLUSTERED |
| 101 | NOT |
| 102 | NULL |
| 103 | NULLIF |
| 104 | OF |
| 105 | OFF |
| 106 | OFFSETS |
| 107 | ON |
| 108 | OPEN |
| 109 | OPENDATASOURCE |
| 110 | OPENQUERY |
| 111 | OPENROWSET |
| 112 | OPENXML |
| 113 | OPTION |
| 114 | OR |
| 115 | ORDER |
| 116 | OUTER |
| 117 | OVER |
| 118 | PERCENT |
| 119 | PIVOT |
| 120 | PLAN |
| 121 | PRECISION |
| 122 | PRIMARY |
| 123 | PRINT |
| 124 | PROC |
| 125 | PROCEDURE |
| 126 | PUBLIC |
| 127 | RAISERROR |
| 128 | READ |
| 129 | READTEXT |
| 130 | RECONFIGURE |
| 131 | REFERENCES |
| 132 | REPLICATION |
| 133 | RESTORE |
| 134 | RESTRICT |
| 135 | RETURN |
| 136 | REVERT |
| 137 | REVOKE |
| 138 | RIGHT |
| 139 | ROLLBACK |
| 140 | ROWCOUNT |
| 141 | ROWGUIDCOL |
| 142 | RULE |
| 143 | SAVE |
| 144 | SCHEMA |
| 145 | SECURITYAUDIT |
| 146 | SELECT |
| 147 | SEMANTICKEYPHRASETABLE |
| 148 | SEMANTICSIMILARITYDETAILSTABLE |
| 149 | SEMANTICSIMILARITYTABLE |
| 150 | SESSION_USER |
| 151 | SET |
| 152 | SETUSER |
| 153 | SHUTDOWN |
| 154 | SOME |
| 155 | STATISTICS |
| 156 | SYSTEM_USER |
| 157 | TABLE |
| 158 | TABLESAMPLE |
| 159 | TEXTSIZE |
| 160 | THEN |
| 161 | TO |
| 162 | TOP |
| 163 | TRAN |
| 164 | TRANSACTION |
| 165 | TRIGGER |
| 166 | TRUNCATE |
| 167 | TRY_CONVERT |
| 168 | TSEQUAL |
| 169 | UNION |
| 170 | UNIQUE |
| 171 | UNPIVOT |
| 172 | UPDATE |
| 173 | UPDATETEXT |
| 174 | USE |
| 175 | USER |
| 176 | VALUES |
| 177 | VARYING |
| 178 | VIEW |
| 179 | WAITFOR |
| 180 | WHEN |
| 181 | WHERE |
| 182 | WHILE |
| 183 | WITH |
| 184 | WITHIN GROUP |
| 185 | WRITETEXT |

## Azure Synapse Analytics Extra Reserved Keyword

| SR# | Keyword |
|---:|---|
| 186 | LABEL |

## Usage Note

Reserved keywords can be used as object names only when delimited, for example:

```sql
CREATE TABLE [TABLE] (
    [SELECT] INT
);
