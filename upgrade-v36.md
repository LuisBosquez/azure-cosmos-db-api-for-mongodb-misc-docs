# Upgrade to Azure Cosmos DB's API for MongoDB engine version 3.6

## Your database account qualifies to be updated to the latest version of Azure Cosmos DB's API for MongoDB.

Upgrading to the latest version of the service will provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

The upgrade process will not provide any service interruptions or downtime. It will also not require any data or index migrations. As soon as you start the process, your account will be queued to proceed with the upgrade. You will be notified when your account has finished upgrading.

Check for the updated functionality in this version: [Wire protocol support (v3.6)](https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36)

1. Benefits of upgrading to version 3.6

   - Enhanced performance and stability
   - Support for new database commands
   - Support for aggregation pipeline by default and new aggregation stages
   - Support for ChangeStream
   - Support for Compound Indexes
   - Cross-partition support for the following operations: UPDATE, DELETE, COUNT, and ORDER BY
   - Improved performance for the following aggregate operations: COUNT, SKIP, LIMIT, and GROUP BY

2. Changes from previous engine versions

   - MongoDB collections will only have the _id property indexed by default
   - Per request timeout is going to be 30 seconds
   - Recommended time to refresh idle connections is now 30 minutes
3. Action required
   After the upgrade, the connection string to the MongoDB service in your application will need to be updated as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: `{GlobalDatabaseAccountName}.mongo.cosmos.azure.com` but it might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.
