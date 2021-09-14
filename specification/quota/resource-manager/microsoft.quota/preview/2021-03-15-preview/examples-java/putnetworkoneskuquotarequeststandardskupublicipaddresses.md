Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-quota_1.0.0-beta.1/sdk/quota/azure-resourcemanager-quota/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.quota.models.LimitType;
import com.azure.resourcemanager.quota.models.LimitValue;
import com.azure.resourcemanager.quota.models.QuotaProperties;
import com.azure.resourcemanager.quota.models.ResourceName;

/** Samples for Quota CreateOrUpdate. */
public final class Main {
    /*
     * x-ms-original-file: specification/quota/resource-manager/Microsoft.Quota/preview/2021-03-15-preview/examples/putNetworkOneSkuQuotaRequestStandardSkuPublicIpAddresses.json
     */
    /**
     * Sample code: Quotas_PutRequest_ForNetwork_StandardSkuPublicIpAddressesResource.
     *
     * @param manager Entry point to QuotaManager.
     */
    public static void quotasPutRequestForNetworkStandardSkuPublicIpAddressesResource(
        com.azure.resourcemanager.quota.QuotaManager manager) {
        manager
            .quotas()
            .define("StandardSkuPublicIpAddresses")
            .withExistingScope(
                "subscriptions/D7EC67B3-7657-4966-BFFC-41EFD36BAAB3/providers/Microsoft.Network/locations/eastus")
            .withProperties(
                new QuotaProperties()
                    .withLimit(new LimitValue().withValue(10).withLimitObjectType(LimitType.LIMIT_VALUE))
                    .withName(new ResourceName().withValue("StandardSkuPublicIpAddresses"))
                    .withResourceType("PublicIpAddresses"))
            .create();
    }
}
```
