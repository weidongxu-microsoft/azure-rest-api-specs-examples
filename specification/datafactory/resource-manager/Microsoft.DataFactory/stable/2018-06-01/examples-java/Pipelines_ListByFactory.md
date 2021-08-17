```java
import com.azure.core.util.Context;

/** Samples for Pipelines ListByFactory. */
public final class PipelinesListByFactory {
    /*
     * operationId: Pipelines_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: Pipelines_ListByFactory
     */
    /**
     * Sample code: Pipelines_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void pipelinesListByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.pipelines().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```