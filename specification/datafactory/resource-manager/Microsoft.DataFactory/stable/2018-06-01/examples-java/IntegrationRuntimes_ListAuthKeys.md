Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes ListAuthKeys. */
public final class Main {
    /*
     * operationId: IntegrationRuntimes_ListAuthKeys
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_ListAuthKeys
     */
    /**
     * Sample code: IntegrationRuntimes_ListAuthKeys.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesListAuthKeys(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .listAuthKeysWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```
