```java
/** Samples for Factories CreateOrUpdate. */
public final class FactoriesCreateOrUpdate {
    /*
     * operationId: Factories_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: Factories_CreateOrUpdate
     */
    /**
     * Sample code: Factories_CreateOrUpdate.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesCreateOrUpdate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .factories()
            .define("exampleFactoryName")
            .withRegion("East US")
            .withExistingResourceGroup("exampleResourceGroup")
            .create();
    }
}
```