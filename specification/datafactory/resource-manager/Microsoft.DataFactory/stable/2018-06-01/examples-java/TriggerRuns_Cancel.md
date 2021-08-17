```java
import com.azure.core.util.Context;

/** Samples for TriggerRuns Cancel. */
public final class TriggerRunsCancel {
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