```java
import com.azure.core.util.Context;

/** Samples for Triggers SubscribeToEvents. */
public final class TriggersSubscribeToEvents {
    /*
     * operationId: Triggers_SubscribeToEvents
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_SubscribeToEvents
     */
    /**
     * Sample code: Triggers_SubscribeToEvents.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersSubscribeToEvents(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .subscribeToEvents("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```