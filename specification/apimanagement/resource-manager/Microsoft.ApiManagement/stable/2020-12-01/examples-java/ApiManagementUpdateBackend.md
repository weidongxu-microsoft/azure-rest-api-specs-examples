Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.BackendContract;
import com.azure.resourcemanager.apimanagement.models.BackendTlsProperties;

/** Samples for Backend Update. */
public final class Main {
    /*
     * operationId: Backend_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateBackend
     */
    /**
     * Sample code: ApiManagementUpdateBackend.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateBackend(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        BackendContract resource =
            manager.backends().getWithResponse("rg1", "apimService1", "proxybackend", Context.NONE).getValue();
        resource
            .update()
            .withDescription("description5308")
            .withTls(new BackendTlsProperties().withValidateCertificateChain(false).withValidateCertificateName(true))
            .withIfMatch("*")
            .apply();
    }
}
```
