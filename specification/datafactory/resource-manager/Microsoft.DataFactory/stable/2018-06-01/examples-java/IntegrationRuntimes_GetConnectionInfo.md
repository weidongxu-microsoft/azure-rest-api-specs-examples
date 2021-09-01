Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes GetConnectionInfo. */
public final class Main {
    /*
     * operationId: IntegrationRuntimes_GetConnectionInfo
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_GetConnectionInfo
     */
    /**
     * Sample code: IntegrationRuntimes_GetConnectionInfo.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesGetConnectionInfo(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .getConnectionInfoWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```
