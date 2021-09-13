Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.AuthorizationServerContract;

/** Samples for AuthorizationServer Update. */
public final class Main {
    /*
     * operationId: AuthorizationServer_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateAuthorizationServer
     */
    /**
     * Sample code: ApiManagementUpdateAuthorizationServer.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateAuthorizationServer(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        AuthorizationServerContract resource =
            manager
                .authorizationServers()
                .getWithResponse("rg1", "apimService1", "newauthServer", Context.NONE)
                .getValue();
        resource.update().withClientId("update").withClientSecret("updated").withIfMatch("*").apply();
    }
}
```
