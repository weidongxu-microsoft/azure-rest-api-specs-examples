```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimeObjectMetadata Refresh. */
public final class IntegrationRuntimeObjectMetadataRefresh {
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