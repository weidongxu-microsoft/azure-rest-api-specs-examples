```java
import com.azure.core.util.Context;

/** Samples for Pipelines Delete. */
public final class PipelinesDelete {
    /*
     * operationId: Pipelines_Delete
     * api-version: 2018-06-01
     * x-ms-examples: Pipelines_Delete
     */
    /**
     * Sample code: Pipelines_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void pipelinesDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .pipelines()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "examplePipeline", Context.NONE);
    }
}
```