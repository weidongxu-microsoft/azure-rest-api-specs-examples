Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.TriggerFilterParameters;

/** Samples for Triggers QueryByFactory. */
public final class Main {
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
