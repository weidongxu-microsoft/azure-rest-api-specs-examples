```java
import com.azure.core.util.Context;

/** Samples for TriggerRuns Rerun. */
public final class TriggerRunsRerun {
    /*
     * operationId: TriggerRuns_Rerun
     * api-version: 2018-06-01
     * x-ms-examples: Triggers_Rerun
     */
    /**
     * Sample code: Triggers_Rerun.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void triggersRerun(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .triggerRuns()
            .rerunWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleTrigger",
                "2f7fdb90-5df1-4b8e-ac2f-064cfa58202b",
                Context.NONE);
    }
}
```