```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.TriggerFilterParameters;

/** Samples for Triggers QueryByFactory. */
public final class TriggersQueryByFactory {
    /*
     * operationId: Triggers_QueryByFactory
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_QueryByFactory
     */
    /**
     * Sample code: Triggers_QueryByFactory.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersQueryByFactory(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggers()
            .queryByFactoryWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                new TriggerFilterParameters().withParentTriggerName("exampleTrigger"),
                Context.NONE);
    }
}
```