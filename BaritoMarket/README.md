### What is BaritoMarket?
BaritoMarket is the first thing you will see when you use this whole BaritoLog thing, so basically its the UI of the BaritoLog where client regist their app to the BaritoLog. Some things that you can do with BaritoMarket beside app registration are creating new logs and monitoring your logs(see the status and etc).

Click [here](https://github.com/BaritoLog/BaritoMarket) for further explanation.

### How to Setup
There's explanation on the link above about how to setup locally the BaritoMarket for development. But here's the thing you can do if error's happening:

* PG:Bad Connection: Connection Refused
- please do the below command to solve this(Mac)
`brew services restart postgresql`

* psql: FATA:: role "postgres" does not exist
- try to login to your postgres db
`psql -d postgres`
  and then run this command
`\du`
  If there is no user called "postgres", then create one with this
  `CREATE USER "username" SUPERUSER;`
