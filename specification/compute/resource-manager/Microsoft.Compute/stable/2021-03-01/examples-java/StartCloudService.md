```java
import com.azure.core.util.Context;

/** Samples for CloudServices Start. */
public final class StartCloudService {
    /*
     * operationId: CloudServices_Start
     * api-version: 2021-03-01
     * x-ms-examples: Start Cloud Service
     */
    /**
     * Sample code: Start Cloud Service.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void startCloudService(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .start("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```