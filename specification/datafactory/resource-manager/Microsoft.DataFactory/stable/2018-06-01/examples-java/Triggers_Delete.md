```java
import com.azure.core.util.Context;

/** Samples for Triggers Delete. */
public final class TriggersDelete {
    /*
     * operationId: Triggers_Delete
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Delete
     */
    /**
     * Sample code: Triggers_Delete.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersDelete(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .deleteWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```