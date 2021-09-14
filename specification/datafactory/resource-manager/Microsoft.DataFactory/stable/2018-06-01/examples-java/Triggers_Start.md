Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Triggers Start. */
public final class Main {
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
