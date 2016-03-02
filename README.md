==Java Managed VM with Cloud SQL Second Generation using junixsocket example==

This is an example on how to use Cloud SQL Second Generation on Java Managed VMs. Managed VMs run Cloud SQL Proxy and are able to expose Cloud SQL 2nd generation databases as unix sockets.

In order to use unix sockets on Java we use https://github.com/kohlschutter/junixsocket

Code adapted from https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/managed_vms/cloudsql.

To run this code you need to:

1. Create a Cloud SQL 2nd gen instance on the same project you will deploy this example.
2. Connect to this instance and create a database.
3. Enable Google Cloud SQL API on the project's API Manager.
4. Replace cloud_sql_instances, SQL_INSTANCE_URL, SQL_DATABASE_NAME on src/appengine/app.yaml with the values for your project.
5. Deploy the project by running mvn gcloud:deploy
6. The code will be deployed to csql-dot-<YOUR-PROJECT-ID>.appspot.com
