For Connect
```Server=doska.kupeyka.com,1433;Database=doska;User=sa;Password=secret;```

For Imprt dump
`docker exec -i some-mysql sh -c 'exec mysql -uuser -ppassword database' < /some/path/on/your/host/all-databases.sql`

For export dump
`docker exec some-mysql sh -c 'exec mysqldump --all-databases -uuser -ppassword database' > /some/path/on/your/host/all-databases.sql`
