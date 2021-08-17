```java
import com.azure.resourcemanager.datafactory.models.SelfHostedIntegrationRuntime;

/** Samples for IntegrationRuntimes CreateOrUpdate. */
public final class IntegrationRuntimesCreate {
    /*
     * operationId: IntegrationRuntimes_CreateOrUpdate
     * api-version: 2018-06-01
     * x-ms-examples: IntegrationRuntimes_Create
     */
    /**
     * Sample code: IntegrationRuntimes_Create.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void integrationRuntimesCreate(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .integrationRuntimes()
            .define("exampleIntegrationRuntime")
            .withExistingFactory("exampleResourceGroup", "exampleFactoryName")
            .withProperties(new SelfHostedIntegrationRuntime().withDescription("A selfhosted integration runtime"))
            .create();
    }
}
```