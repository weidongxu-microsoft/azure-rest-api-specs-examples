```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes GetStatus. */
public final class IntegrationRuntimesGetStatus {
    /*
     * operationId: IntegrationRuntimes_GetStatus
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_GetStatus
     */
    /**
     * Sample code: IntegrationRuntimes_GetStatus.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesGetStatus(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .getStatusWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```