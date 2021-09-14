Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for NamedValue RefreshSecret. */
public final class Main {
    /*
     * operationId: NamedValue_RefreshSecret
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementRefreshNamedValue
     */
    /**
     * Sample code: ApiManagementRefreshNamedValue.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementRefreshNamedValue(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.namedValues().refreshSecret("rg1", "apimService1", "testprop2", Context.NONE);
    }
}
```
