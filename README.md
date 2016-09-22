# asadmin-cmd
create jdbc connection pool for postgres database<br>
test ping connection pool<br>
create jdbc resource<br>
<p>
first, copy postgres jdbc driver jar file to this directory:
</p>
<p>
C:\Program Files\glassfish-4.1.1\glassfish\lib
</p>
<ul>
<li>
asadmin create-jdbc-connection-pool --datasourceclassname=org.postgresql.ds.PGSimpleDataSource --driverclassname=org.postgresql.Driver --restype=javax.sql.DataSource --property user=postgres:password=pass:serverName=localhost:portNumber=5432:databaseName=dbName pgDbPool
</li>
<li>
asadmin ping-connection-pool pgDbPool
</li>
<li>
asadmin delete-jdbc-connection-pool pgDbPool
</li>
<li>
asadmin list-connection-pools
</li>
<li>
asadmin create-jdbc-resource --connectionpoolid=pgDbPool jdbc/pgDb
</li>
</ul>
