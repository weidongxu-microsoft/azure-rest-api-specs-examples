Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Triggers Delete. */
public final class Main {
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
