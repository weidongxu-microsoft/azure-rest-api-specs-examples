Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
/** Samples for Factories CreateOrUpdate. */
public final class Main {
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
