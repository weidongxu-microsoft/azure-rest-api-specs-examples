Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.UpdateIntegrationRuntimeNodeRequest;

/** Samples for IntegrationRuntimeNodes Update. */
public final class Main {
    /*
     * operationId: IntegrationRuntimeNodes_Update
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimeNodes_Update
     */
    /**
     * Sample code: IntegrationRuntimeNodes_Update.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimeNodesUpdate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimeNodes()
            .updateWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleIntegrationRuntime",
                "Node_1",
                new UpdateIntegrationRuntimeNodeRequest().withConcurrentJobsLimit(2),
                Context.NONE);
    }
}
```
