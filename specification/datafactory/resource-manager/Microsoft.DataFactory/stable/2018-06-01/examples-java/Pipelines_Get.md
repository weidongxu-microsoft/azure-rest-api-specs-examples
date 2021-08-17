```java
import com.azure.core.util.Context;

/** Samples for Pipelines Get. */
public final class PipelinesGet {
    /*
     * operationId: Pipelines_Get
     * api-version: 2018-06-01
     * x-ms-examples: Pipelines_Get
     */
    /**
     * Sample code: Pipelines_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void pipelinesGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .pipelines()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "examplePipeline", null, Context.NONE);
    }
}
```