```java
import com.azure.core.util.Context;

/** Samples for PipelineRuns Get. */
public final class PipelineRunsGet {
    /*
     * operationId: PipelineRuns_Get
     * api-version: 2018-06-01
     * x-ms-examples: PipelineRuns_Get
     */
    /**
     * Sample code: PipelineRuns_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void pipelineRunsGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .pipelineRuns()
            .getWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "2f7fdb90-5df1-4b8e-ac2f-064cfa58202b", Context.NONE);
    }
}
```