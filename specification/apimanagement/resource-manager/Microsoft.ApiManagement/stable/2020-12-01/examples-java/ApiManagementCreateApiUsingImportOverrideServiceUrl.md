Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.apimanagement.models.ApiCreateOrUpdatePropertiesWsdlSelector;
import com.azure.resourcemanager.apimanagement.models.AuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.BearerTokenSendingMethods;
import com.azure.resourcemanager.apimanagement.models.ContentFormat;
import com.azure.resourcemanager.apimanagement.models.OAuth2AuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.OpenIdAuthenticationSettingsContract;
import com.azure.resourcemanager.apimanagement.models.Protocol;
import com.azure.resourcemanager.apimanagement.models.SoapApiType;
import com.azure.resourcemanager.apimanagement.models.SubscriptionKeyParameterNamesContract;
import java.util.Arrays;

/** Samples for Api CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Api_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateApiUsingImportOverrideServiceUrl
     */
    /**
     * Sample code: ApiManagementCreateApiUsingImportOverrideServiceUrl.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateApiUsingImportOverrideServiceUrl(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apis()
            .define("apidocs")
            .withExistingService("rg1", "apimService1")
            .withValue("http://apimpimportviaurl.azurewebsites.net/api/apidocs/")
            .withFormat(ContentFormat.fromString("swagger-link"))
            .withServiceUrl("http://petstore.swagger.wordnik.com/api")
            .withPath("petstoreapi123")
            .create();
    }
}
```
