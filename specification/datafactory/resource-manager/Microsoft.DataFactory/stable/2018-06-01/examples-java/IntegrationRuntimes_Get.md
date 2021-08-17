```java
import com.azure.core.util.Context;

/** Samples for IntegrationRuntimes Get. */
public final class IntegrationRuntimesGet {
    /*
     * operationId: IntegrationRuntimes_Get
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Get
     */
    /**
     * Sample code: IntegrationRuntimes_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .getWithResponse(
                "exampleResourceGroup", "exampleFactoryName", "exampleIntegrationRuntime", null, Context.NONE);
    }
}
```