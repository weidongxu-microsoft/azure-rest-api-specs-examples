Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-quota_1.0.0-beta.1/sdk/quota/azure-resourcemanager-quota/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Usages Get. */
public final class Main {
    /*
     * x-ms-original-file: specification/quota/resource-manager/Microsoft.Quota/preview/2021-03-15-preview/examples/getNetworkOneSkuUsages.json
     */
    /**
     * Sample code: Quotas_UsagesRequest_ForNetwork.
     *
     * @param manager Entry point to QuotaManager.
     */
    public static void quotasUsagesRequestForNetwork(com.azure.resourcemanager.quota.QuotaManager manager) {
        manager
            .usages()
            .getWithResponse(
                "MinPublicIpInterNetworkPrefixLength",
                "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/eastus",
                Context.NONE);
    }
}
```