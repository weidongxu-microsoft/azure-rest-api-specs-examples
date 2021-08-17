```java
import com.azure.core.util.Context;

/** Samples for DataFlows Delete. */
public final class DataFlowsDelete {
    /*
     * operationId: DataFlows_Delete
     * api-version: 2018-06-01
     * x-ms-examples: DataFlows_Delete
     */
    /**
     * Sample code: DataFlows_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void dataFlowsDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .dataFlows()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleDataFlow", Context.NONE);
    }
}
```