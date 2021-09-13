Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for DeletedServices GetByName. */
public final class Main {
    /*
     * operationId: DeletedServices_GetByName
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetDeletedServiceByName
     */
    /**
     * Sample code: ApiManagementGetDeletedServiceByName.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetDeletedServiceByName(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.deletedServices().getByNameWithResponse("apimService3", "westus", Context.NONE);
    }
}
```
