Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.IdentityProviderType;

/** Samples for IdentityProvider Delete. */
public final class Main {
    /*
     * operationId: IdentityProvider_Delete
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementDeleteIdentityProvider
     */
    /**
     * Sample code: ApiManagementDeleteIdentityProvider.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementDeleteIdentityProvider(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .identityProviders()
            .deleteWithResponse("rg1", "apimService1", IdentityProviderType.AAD, "*", Context.NONE);
    }
}
```
