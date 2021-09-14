Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiManagementService List. */
public final class Main {
    /*
     * operationId: ApiManagementService_List
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListServiceBySubscription
     */
    /**
     * Sample code: ApiManagementListServiceBySubscription.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListServiceBySubscription(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiManagementServices().list(Context.NONE);
    }
}
```
