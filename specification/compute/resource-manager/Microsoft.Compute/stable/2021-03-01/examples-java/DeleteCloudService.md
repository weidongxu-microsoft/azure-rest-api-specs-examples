```java
import com.azure.core.util.Context;

/** Samples for CloudServices Delete. */
public final class DeleteCloudService {
    /*
     * operationId: CloudServices_Delete
     * api-version: 2021-03-01
     * x-ms-examples: Delete Cloud Service
     */
    /**
     * Sample code: Delete Cloud Service.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void deleteCloudService(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .delete("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```