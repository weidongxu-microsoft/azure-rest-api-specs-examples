```java
import com.azure.core.util.Context;

/** Samples for DataFlows Get. */
public final class DataFlowsGet {
    /*
     * operationId: DataFlows_Get
     * api-version: 2018-06-01
     * x-ms-examples: DataFlows_Get
     */
    /**
     * Sample code: DataFlows_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void dataFlowsGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .dataFlows()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleDataFlow", null, Context.NONE);
    }
}
```