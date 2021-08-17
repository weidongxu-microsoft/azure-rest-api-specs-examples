```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.LinkedIntegrationRuntimeRequest;

/** Samples for IntegrationRuntimes RemoveLinks. */
public final class IntegrationRuntimesRemoveLinks {
    /*
     * operationId: IntegrationRuntimes_RemoveLinks
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
            .removeLinksWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                "exampleIntegrationRuntime",
                new LinkedIntegrationRuntimeRequest().withLinkedFactoryName("exampleFactoryName-linked"),
                Context.NONE);
    }
}
```