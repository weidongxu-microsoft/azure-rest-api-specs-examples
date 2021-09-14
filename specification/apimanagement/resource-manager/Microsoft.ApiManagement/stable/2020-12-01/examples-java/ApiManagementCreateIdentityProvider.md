Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.apimanagement.models.IdentityProviderType;

/** Samples for IdentityProvider CreateOrUpdate. */
public final class Main {
    /*
     * operationId: IdentityProvider_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateIdentityProvider
     */
    /**
     * Sample code: ApiManagementCreateIdentityProvider.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateIdentityProvider(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .identityProviders()
            .define(IdentityProviderType.FACEBOOK)
            .withExistingService("rg1", "apimService1")
            .withClientId("facebookid")
            .withClientSecret("facebookapplicationsecret")
            .create();
    }
}
```
