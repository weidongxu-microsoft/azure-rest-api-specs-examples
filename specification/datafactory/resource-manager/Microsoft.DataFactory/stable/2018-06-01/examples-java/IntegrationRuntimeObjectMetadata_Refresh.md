Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimeObjectMetadata Refresh. */
public final class Main {
    /*
     * operationId: IntegrationRuntimeObjectMetadata_Refresh
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimeObjectMetadata_Refresh
     */
    /**
     * Sample code: IntegrationRuntimeObjectMetadata_Refresh.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimeObjectMetadataRefresh(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimeObjectMetadatas()
            .refresh("exampleResourceGroup", "exampleFactoryName", "testactivityv2", Context.NONE);
    }
}
```
