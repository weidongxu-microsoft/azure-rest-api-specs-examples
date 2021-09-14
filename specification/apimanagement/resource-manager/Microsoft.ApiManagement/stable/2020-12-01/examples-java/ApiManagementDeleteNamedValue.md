Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for NamedValue Delete. */
public final class Main {
    /*
     * operationId: NamedValue_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteNamedValue
     */
    /**
     * Sample code: ApiManagementDeleteNamedValue.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteNamedValue(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.namedValues().deleteWithResponse("rg1", "apimService1", "testprop2", "*", Context.NONE);
    }
}
```
