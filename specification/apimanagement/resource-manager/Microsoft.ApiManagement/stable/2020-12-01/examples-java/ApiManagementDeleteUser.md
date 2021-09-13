Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for User Delete. */
public final class Main {
    /*
     * operationId: User_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteUser
     */
    /**
     * Sample code: ApiManagementDeleteUser.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteUser(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .users()
            .deleteWithResponse("rg1", "apimService1", "5931a75ae4bbd512288c680b", "*", null, null, null, Context.NONE);
    }
}
```
