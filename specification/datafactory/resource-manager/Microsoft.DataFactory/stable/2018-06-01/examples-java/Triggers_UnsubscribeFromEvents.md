```java
import com.azure.core.util.Context;

/** Samples for Triggers UnsubscribeFromEvents. */
public final class TriggersUnsubscribeFromEvents {
    /*
     * operationId: Triggers_UnsubscribeFromEvents
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_UnsubscribeFromEvents
     */
    /**
     * Sample code: Triggers_UnsubscribeFromEvents.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersUnsubscribeFromEvents(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .unsubscribeFromEvents("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```