Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiRelease Get. */
public final class Main {
    /*
     * operationId: ApiRelease_Get
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementGetApiRelease
     */
    /**
     * Sample code: ApiManagementGetApiRelease.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementGetApiRelease(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiReleases().getWithResponse("rg1", "apimService1", "a1", "5a7cb545298324c53224a799", Context.NONE);
    }
}
```
