Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager_2.10.0/sdk/resourcemanager/azure-resourcemanager/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.storage.models.ManagementPolicyName;

/** Samples for ManagementPolicies Get. */
public final class Main {
    /*
     * x-ms-original-file: specification/storage/resource-manager/Microsoft.Storage/stable/2021-04-01/examples/StorageAccountGetManagementPolicy.json
     */
    /**
     * Sample code: StorageAccountGetManagementPolicies.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void storageAccountGetManagementPolicies(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .storageAccounts()
            .manager()
            .serviceClient()
            .getManagementPolicies()
            .getWithResponse("res6977", "sto2527", ManagementPolicyName.DEFAULT, Context.NONE);
    }
}
```