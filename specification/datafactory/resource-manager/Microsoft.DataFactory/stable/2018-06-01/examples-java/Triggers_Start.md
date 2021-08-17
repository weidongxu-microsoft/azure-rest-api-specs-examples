```java
import com.azure.core.util.Context;

/** Samples for Triggers Start. */
public final class TriggersStart {
    /*
     * operationId: Triggers_Start
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Start
     */
    /**
     * Sample code: Triggers_Start.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersStart(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.triggers().start("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```