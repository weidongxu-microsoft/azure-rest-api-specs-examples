```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.Trigger;
import com.azure.resourcemanager.datafactory.models.TriggerResource;

/** Samples for Triggers CreateOrUpdate. */
public final class TriggersUpdate {
    /*
     * operationId: Triggers_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Update
     */
    /**
     * Sample code: Triggers_Update.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersUpdate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        TriggerResource resource =
            manager
                .triggers()
                .getWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleTrigger", null, Context.NONE)
                .getValue();
        resource.update().withProperties(new Trigger().withDescription("Example description")).apply();
    }
}
```