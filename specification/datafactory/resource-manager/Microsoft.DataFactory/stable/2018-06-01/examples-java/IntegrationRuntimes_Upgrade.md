```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes Upgrade. */
public final class IntegrationRuntimesUpgrade {
    /*
     * operationId: IntegrationRuntimes_Upgrade
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Upgrade
     */
    /**
     * Sample code: IntegrationRuntimes_Upgrade.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesUpgrade(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .upgradeWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", Context.NONE);
    }
}
```