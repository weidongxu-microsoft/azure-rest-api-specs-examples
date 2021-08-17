```java
import com.azure.core.util.Context;

/** Samples for PrivateEndPointConnections ListByFactory. */
public final class PrivateEndPointConnectionsListByFactory {
    /*
     * operationId: PrivateEndPointConnections_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: privateEndPointConnections_ListByFactory
     */
    /**
     * Sample code: privateEndPointConnections_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void privateEndPointConnectionsListByFactory(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.privateEndPointConnections().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```