Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-apimanagement_1.0.0-beta.2/sdk/apimanagement/azure-resourcemanager-apimanagement/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.apimanagement.models.AdditionalLocation;
import com.azure.resourcemanager.apimanagement.models.ApiManagementServiceIdentity;
import com.azure.resourcemanager.apimanagement.models.ApiManagementServiceSkuProperties;
import com.azure.resourcemanager.apimanagement.models.ApiVersionConstraint;
import com.azure.resourcemanager.apimanagement.models.ApimIdentityType;
import com.azure.resourcemanager.apimanagement.models.CertificateConfiguration;
import com.azure.resourcemanager.apimanagement.models.CertificateConfigurationStoreName;
import com.azure.resourcemanager.apimanagement.models.HostnameConfiguration;
import com.azure.resourcemanager.apimanagement.models.HostnameType;
import com.azure.resourcemanager.apimanagement.models.SkuType;
import com.azure.resourcemanager.apimanagement.models.UserIdentityProperties;
import com.azure.resourcemanager.apimanagement.models.VirtualNetworkType;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for ApiManagementService CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ApiManagementService_CreateOrUpdate
     * api-version: 2020-12-01
     * x-ms-examples: ApiManagementCreateServiceWithSystemCertificates
     */
    /**
     * Sample code: ApiManagementCreateServiceWithSystemCertificates.
     *
     * @param manager Entry point to ApiManagementManager.
     */
    public static void apiManagementCreateServiceWithSystemCertificates(
        com.azure.resourcemanager.apimanagement.ApiManagementManager manager) {
        manager
            .apiManagementServices()
            .define("apimService1")
            .withRegion("Central US")
            .withExistingResourceGroup("rg1")
            .withSku(new ApiManagementServiceSkuProperties().withName(SkuType.BASIC).withCapacity(1))
            .withPublisherEmail("apim@autorestsdk.com")
            .withPublisherName("autorestsdk")
            .withTags(mapOf("tag1", "value1", "tag2", "value2", "tag3", "value3"))
            .withCertificates(
                Arrays
                    .asList(
                        new CertificateConfiguration()
                            .withEncodedCertificate("*******Base64 encoded Certificate******************")
                            .withCertificatePassword("Password")
                            .withStoreName(CertificateConfigurationStoreName.CERTIFICATE_AUTHORITY)))
            .create();
    }

    @SuppressWarnings("unchecked")
    private static <T> Map<String, T> mapOf(Object... inputs) {
        Map<String, T> map = new HashMap<>();
        for (int i = 0; i < inputs.length; i += 2) {
            String key = (String) inputs[i];
            T value = (T) inputs[i + 1];
            map.put(key, value);
        }
        return map;
    }
}
```
