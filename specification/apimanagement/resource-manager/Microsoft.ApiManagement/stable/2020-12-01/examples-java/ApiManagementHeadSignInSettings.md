Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for SignInSettings GetEntityTag. */
public final class Main {
    /*
     * operationId: SignInSettings_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadSignInSettings
     */
    /**
     * Sample code: ApiManagementHeadSignInSettings.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadSignInSettings(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.signInSettings().getEntityTagWithResponse("rg1", "apimService1", Context.NONE);
    }
}
```
