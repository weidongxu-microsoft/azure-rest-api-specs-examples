```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.GetSsisObjectMetadataRequest;

/** Samples for IntegrationRuntimeObjectMetadata Get. */
public final class IntegrationRuntimeObjectMetadataGet {
    /*
     * operationId: IntegrationRuntimeObjectMetadata_Get
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimeObjectMetadata_Get
     */
    /**
     * Sample code: IntegrationRuntimeObjectMetadata_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimeObjectMetadataGet(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimeObjectMetadatas()
            .getWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "testactivityv2",
                new GetSsisObjectMetadataRequest().withMetadataPath("ssisFolders"),
                Context.NONE);
    }
}
```