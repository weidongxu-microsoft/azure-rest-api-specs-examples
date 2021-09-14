Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApiManagementService GetSsoToken. */
public final class Main {
    /*
     * operationId: ApiManagementService_GetSsoToken
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementServiceGetSsoToken
     */
    /**
     * Sample code: ApiManagementServiceGetSsoToken.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementServiceGetSsoToken(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.apiManagementServices().getSsoTokenWithResponse("rg1", "apimService1", Context.NONE);
    }
}
```
