Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.models.ApiVersionSetContract;
import com.azure.resourcemanager.apimanagement.models.VersioningScheme;

/** Samples for ApiVersionSet Update. */
public final class Main {
    /*
     * operationId: ApiVersionSet_Update
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementUpdateApiVersionSet
     */
    /**
     * Sample code: ApiManagementUpdateApiVersionSet.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementUpdateApiVersionSet(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        ApiVersionSetContract resource =
            manager.apiVersionSets().getWithResponse("rg1", "apimService1", "vs1", Context.NONE).getValue();
        resource
            .update()
            .withDisplayName("api set 1")
            .withVersioningScheme(VersioningScheme.SEGMENT)
            .withDescription("Version configuration")
            .withIfMatch("*")
            .apply();
    }
}
```
