Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for SignUpSettings GetEntityTag. */
public final class Main {
    /*
     * operationId: SignUpSettings_GetEntityTag
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementHeadSignUpSettings
     */
    /**
     * Sample code: ApiManagementHeadSignUpSettings.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementHeadSignUpSettings(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager.signUpSettings().getEntityTagWithResponse("rg1", "apimService1", Context.NONE);
    }
}
```
