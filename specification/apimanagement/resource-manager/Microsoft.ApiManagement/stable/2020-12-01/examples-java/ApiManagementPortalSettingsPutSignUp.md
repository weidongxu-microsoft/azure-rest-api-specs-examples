Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.apimanagement.fluent.models.PortalSignupSettingsInner;
import com.azure.resourcemanager.apimanagement.models.TermsOfServiceProperties;

/** Samples for SignUpSettings CreateOrUpdate. */
public final class Main {
    /*
     * operationId: SignUpSettings_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementPortalSettingsUpdateSignUp
     */
    /**
     * Sample code: ApiManagementPortalSettingsUpdateSignUp.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementPortalSettingsUpdateSignUp(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .signUpSettings()
            .createOrUpdateWithResponse(
                "rg1",
                "apimService1",
                new PortalSignupSettingsInner()
                    .withEnabled(true)
                    .withTermsOfService(
                        new TermsOfServiceProperties()
                            .withText("Terms of service text.")
                            .withEnabled(true)
                            .withConsentRequired(true)),
                "*",
                Context.NONE);
    }
}
```
