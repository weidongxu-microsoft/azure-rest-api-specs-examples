```java
import com.azure.core.util.Context;

/** Samples for CloudServices PowerOff. */
public final class PowerOffCloudService {
    /*
     * operationId: CloudServices_PowerOff
     * api-version: 2021-03-01
     * x-ms-examples: Stop or PowerOff Cloud Service
     */
    /**
     * Sample code: Stop or PowerOff Cloud Service.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void stopOrPowerOffCloudService(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getCloudServices()
            .powerOff("ConstosoRG", "{cs-name}", Context.NONE);
    }
}
```