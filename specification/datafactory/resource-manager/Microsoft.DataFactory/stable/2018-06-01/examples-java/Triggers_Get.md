```java
import com.azure.core.util.Context;

/** Samples for Triggers Get. */
public final class TriggersGet {
    /*
     * operationId: Triggers_Get
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Get
     */
    /**
     * Sample code: Triggers_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", null, Context.NONE);
    }
}
```