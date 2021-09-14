Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for OpenIdConnectProvider ListSecrets. */
public final class Main {
    /*
     * operationId: OpenIdConnectProvider_ListSecrets
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementOpenidConnectProviderListSecrets
     */
    /**
     * Sample code: ApiManagementOpenidConnectProviderListSecrets.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementOpenidConnectProviderListSecrets(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .openIdConnectProviders()
            .listSecretsWithResponse("rg1", "apimService1", "templateOpenIdConnect2", Context.NONE);
    }
}
```
