# Data Type Mapping

## .NET to MySQL

|              .NET               |               MySQL               |
| :-----------------------------: | :-------------------------------: |
|         System.Boolean          |          boolean, bit(1)          |
|           System.Byte           |         tinyint unsigend          |
|          System.Byte[]          | binary, varbinary, blob, longblob |
| System.Data.Spatial.DbGeometry  |             geometry              |
| System.Data.Spatial.DbGeography |             geometry              |
|         System.DateTime         |             datetime              |
|      System.DateTimeOffset      |             datetime              |
|         System.Decimal          |              decimal              |
|          System.Double          |              double               |
|           System.Guid           |             char(36)              |
|          System.Int16           |             smallint              |
|          System.Int32           |                int                |
|          System.Int64           |              bigint               |
|          System.SByte           |              tinyint              |
|          System.Single          |               float               |
|          System.String          |   char, varchar, text, longtext   |
|         System.TimeSpan         |               time                |



## MySQL to .NET

|                            MySQL                             |              .NET               |
| :----------------------------------------------------------: | :-----------------------------: |
|                    bool, boolean, bit(1)                     |         System.Boolean          |
|                       tinyint unsigend                       |           System.Byte           |
| binary, varbinary, tinyblob, blob, mediumblob, longblob, char byte |          System.Byte[]          |
|                           geometry                           | System.Data.Spatial.DbGeometry  |
|                           geometry                           | System.Data.Spatial.DbGeography |
|                           datetime                           |         System.DateTime         |
|                        datetimeoffset                        |      System.DateTimeOffset      |
| decimal, numeric, dec, fixed, bigint unsigned, float unsigned, double unsigned, serial |         System.Decimal          |
|                         double, real                         |          System.Double          |
|                           char(36)                           |           System.Guid           |
|                        smallint, year                        |          System.Int16           |
|          int, integer, smallint unsigned, mediumint          |          System.Int32           |
|         bigint, int unsigned, integer unsigned, bit          |          System.Int64           |
|                           tinyint                            |          System.SByte           |
|                            float                             |          System.Single          |
| char, varchar, tinytext, text, mediumtext, longtext, set, enum, nchar, national char, nvarchar, national varchar, character varying |          System.String          |
|                             time                             |         System.TimeSpan         |
