```java
import com.azure.core.util.Context;

/** Samples for Triggers ListByFactory. */
public final class TriggersListByFactory {
    /*
     * operationId: Triggers_ListByFactory
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_ListByFactory
     */
    /**
     * Sample code: Triggers_ListByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersListByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.triggers().listByFactory("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```