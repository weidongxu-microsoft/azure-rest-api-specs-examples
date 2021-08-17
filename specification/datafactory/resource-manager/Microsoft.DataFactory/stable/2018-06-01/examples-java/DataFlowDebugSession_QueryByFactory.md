```java
import com.azure.core.util.Context;

/** Samples for DataFlowDebugSession QueryByFactory. */
public final class DataFlowDebugSessionQueryByFactory {
    /*
     * operationId: DataFlowDebugSession_QueryByFactory
     * api-version: 2018-06-01
     * x-ms-examples: DataFlowDebugSession_QueryByFactory
     */
    /**
     * Sample code: DataFlowDebugSession_QueryByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void dataFlowDebugSessionQueryByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.dataFlowDebugSessions().queryByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```