Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Backend Get. */
public final class Main {
    /*
     * operationId: Backend_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetBackend
     */
    /**
     * Sample code: ApiManagementGetBackend.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetBackend(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.backends().getWithResponse("rg1", "apimService1", "sfbackend", Context.NONE);
    }
}
```
