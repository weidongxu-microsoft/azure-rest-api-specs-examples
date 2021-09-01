Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for TriggerRuns Cancel. */
public final class Main {
    /*
     * operationId: TriggerRuns_Cancel
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Cancel
     */
    /**
     * Sample code: Triggers_Cancel.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersCancel(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggerRuns()
            .cancelWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleTrigger",
                "2f7fdb90-5df1-4b8e-ac2f-064cfa58202b",
                Context.NONE);
    }
}
```
