```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes ListAuthKeys. */
public final class IntegrationRuntimesListAuthKeys {
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