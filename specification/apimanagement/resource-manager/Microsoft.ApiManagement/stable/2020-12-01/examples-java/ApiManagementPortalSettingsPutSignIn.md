Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.fluent.models.PortalSigninSettingsInner;

/** Samples for SignInSettings CreateOrUpdate. */
public final class Main {
    /*
     * operationId: SignInSettings_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementPortalSettingsUpdateSignIn
     */
    /**
     * Sample code: ApiManagementPortalSettingsUpdateSignIn.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementPortalSettingsUpdateSignIn(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .signInSettings()
            .createOrUpdateWithResponse(
                "rg1", "apimService1", new PortalSigninSettingsInner().withEnabled(true), "*", Context.NONE);
    }
}
```
