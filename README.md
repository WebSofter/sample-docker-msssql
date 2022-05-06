For Connect
```Server=doska.kupeyka.com,1433;Database=doska;User=sa;Password=secret;```

# Backup the data volume
docker run --rm \
       -v sqldata:/sqldata \
       -v $pwd\:/backup \
       ubuntu tar cvf /backup/backup.tar /sqldata

# Remove existing data volume (clear up old data, if exists)
docker volume rm sqldata

# Restore the data volume
docker run --rm \
       -v sqldata:/sqldata \
       -v $pwd\:/backup \
       ubuntu tar xvf /backup/backup.tar -C sqldata --strip 1
