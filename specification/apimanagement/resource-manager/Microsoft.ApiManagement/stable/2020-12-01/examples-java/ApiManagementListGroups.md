Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Group ListByService. */
public final class Main {
    /*
     * operationId: Group_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListGroups
     */
    /**
     * Sample code: ApiManagementListGroups.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListGroups(com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.groups().listByService("rg1", "apimService1", null, null, null, Context.NONE);
    }
}
```
