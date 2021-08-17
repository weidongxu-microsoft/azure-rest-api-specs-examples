```java
import com.azure.core.util.Context;

/** Samples for Triggers Stop. */
public final class TriggersStop {
    /*
     * operationId: Triggers_Stop
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Stop
     */
    /**
     * Sample code: Triggers_Stop.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersStop(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.triggers().stop("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```