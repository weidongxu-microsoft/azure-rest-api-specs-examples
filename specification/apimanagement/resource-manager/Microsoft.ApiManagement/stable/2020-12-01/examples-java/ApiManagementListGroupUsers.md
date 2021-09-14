Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for GroupUser List. */
public final class Main {
    /*
     * operationId: GroupUser_List
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListGroupUsers
     */
    /**
     * Sample code: ApiManagementListGroupUsers.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListGroupUsers(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.groupUsers().list("rg1", "apimService1", "57d2ef278aa04f0888cba3f3", null, null, null, Context.NONE);
    }
}
```
