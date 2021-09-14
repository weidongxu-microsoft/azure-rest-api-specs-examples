Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiDiagnostic ListByService. */
public final class Main {
    /*
     * operationId: ApiDiagnostic_ListByService
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementListApiDiagnostics
     */
    /**
     * Sample code: ApiManagementListApiDiagnostics.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementListApiDiagnostics(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiDiagnostics().listByService("rg1", "apimService1", "echo-api", null, null, null, Context.NONE);
    }
}
```
