```java
import com.azure.core.util.Context;

/** Samples for DataFlows ListByFactory. */
public final class DataFlowsListByFactory {
    /*
     * operationId: DataFlows_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: DataFlows_ListByFactory
     */
    /**
     * Sample code: DataFlows_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void dataFlowsListByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.dataFlows().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```