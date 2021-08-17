```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes GetMonitoringData. */
public final class IntegrationRuntimesGetMonitoringData {
    /*
     * operationId: IntegrationRuntimes_GetMonitoringData
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_GetMonitoringData
     */
    /**
     * Sample code: IntegrationRuntimes_GetMonitoringData.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesGetMonitoringData(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .getMonitoringDataWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```