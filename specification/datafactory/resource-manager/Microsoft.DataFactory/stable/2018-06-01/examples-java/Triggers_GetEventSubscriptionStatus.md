```java
import com.azure.core.util.Context;

/** Samples for Triggers GetEventSubscriptionStatus. */
public final class TriggersGetEventSubscriptionStatus {
    /*
     * operationId: Triggers_GetEventSubscriptionStatus
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_GetEventSubscriptionStatus
     */
    /**
     * Sample code: Triggers_GetEventSubscriptionStatus.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersGetEventSubscriptionStatus(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .getEventSubscriptionStatusWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleTrigger", Context.NONE);
    }
}
```