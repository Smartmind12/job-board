# devICT job board

## requirements

- docker + docker compose
- that's mainly it!
- for a nicer local dev experience, having go and some go IDE integration set up is likely worthwhile

## running locally

```
$ docker compose up
```

## accessing the database

```
$ make psql
```

## slack integration

setting the `SLACK_HOOK` env var will enable posting new jobs to Slack to the provided Slack hook url. if not configured, this functionality will simply be disabled

## email integration

for testing email sending locally, it is recommended that you use [mailtrap](http://mailtrap.io), then copy `.env.example` to `.env` and add your configuration there

## database migrations

[golang-migrate](https://github.com/golang-migrate/migrate) is used for db migrations. the server runs migrations as it starts up, so unless you're adding new migrations or doing other stuff with the migration files you shouldn't have to worry about this tool.
