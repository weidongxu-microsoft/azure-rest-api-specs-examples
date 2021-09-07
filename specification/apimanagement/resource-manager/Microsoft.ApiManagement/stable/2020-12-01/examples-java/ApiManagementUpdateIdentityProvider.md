Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.IdentityProviderContract;
import com.azure.resourcemanager.apimanagement.models.IdentityProviderType;

/** Samples for IdentityProvider Update. */
public final class Main {
    /*
     * operationId: IdentityProvider_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateIdentityProvider
     */
    /**
     * Sample code: ApiManagementUpdateIdentityProvider.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateIdentityProvider(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        IdentityProviderContract resource =
            manager
                .identityProviders()
                .getWithResponse("rg1", "apimService1", IdentityProviderType.FACEBOOK, Context.NONE)
                .getValue();
        resource
            .update()
            .withClientId("updatedfacebookid")
            .withClientSecret("updatedfacebooksecret")
            .withIfMatch("*")
            .apply();
    }
}
```
