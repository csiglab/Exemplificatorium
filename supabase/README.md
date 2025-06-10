# Supabase Docker

> This is a minimal Docker Compose setup for self-hosting Supabase. Follow the steps [here](https://supabase.com/docs/guides/hosting/docker) to get started.

## Rest

```bash
export SUPABASE_CLIENT_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyAgCiAgICAicm9sZSI6ICJhbm9uIiwKICAgICJpc3MiOiAic3VwYWJhc2UtZGVtbyIsCiAgICAiaWF0IjogMTY0MTc2OTIwMCwKICAgICJleHAiOiAxNzk5NTM1NjAwCn0.dc_X5iR_VP_qT0zsiyj_I_OZ2T9FtRU2BBNWN8Bu4GE

curl 'http://localhost:8000/rest/v1/persona?select=*' \
-H "apikey: $SUPABASE_CLIENT_ANON_KEY" \
-H "Authorization: Bearer $SUPABASE_CLIENT_ANON_KEY"
```

```sql
query {
  personaCollection {
    edges {
      node {
        id
        name
        # add any other fields you have in your persona table
      }
    }
  }
}
`` `

## Supabase Analytics

- [Self-Hosting Analytics](https://supabase.com/docs/reference/self-hosting-analytics/introduction)

## References

- [Supabase](https://righteous-guardian-68f.notion.site/Supabase-fc35bd2a37c842019c3db1399dc7190a?source=copy_link)
- ...
