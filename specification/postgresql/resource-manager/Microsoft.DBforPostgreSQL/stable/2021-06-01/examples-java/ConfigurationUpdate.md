Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-postgresqlflexibleserver_1.0.0-beta.3/sdk/postgresqlflexibleserver/azure-resourcemanager-postgresqlflexibleserver/README.md) on how to add the SDK to your project and authenticate.

```java

/** Samples for Configurations Put. */
public final class Main {
    /*
     * operationId: Configurations_Put
     * api-version: 2021-06-01
     * x-ms-examples: Update a user configuration
     */
    /**
     * Sample code: Update a user configuration.
     *
     * @param manager Entry point to PostgreSqlManager.
     */
    public static void updateAUserConfiguration(
        com.azure.resourcemanager.postgresqlflexibleserver.PostgreSqlManager manager) {
        manager
            .configurations()
            .define("event_scheduler")
            .withExistingFlexibleServer("testrg", "testserver")
            .withValue("on")
            .withSource("user-override")
            .create();
    }
}
```