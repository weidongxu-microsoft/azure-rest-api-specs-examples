Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.OpenidConnectProviderContract;

/** Samples for OpenIdConnectProvider Update. */
public final class Main {
    /*
     * operationId: OpenIdConnectProvider_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateOpenIdConnectProvider
     */
    /**
     * Sample code: ApiManagementUpdateOpenIdConnectProvider.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateOpenIdConnectProvider(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        OpenidConnectProviderContract resource =
            manager
                .openIdConnectProviders()
                .getWithResponse("rg1", "apimService1", "templateOpenIdConnect2", Context.NONE)
                .getValue();
        resource.update().withClientSecret("updatedsecret").withIfMatch("*").apply();
    }
}
```
