Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;
import com.azure.resourcemanager.servicefabric.models.UpgradableVersionsDescription;

/** Samples for Clusters ListUpgradableVersions. */
public final class Main {
    /*
     * operationId: Clusters_ListUpgradableVersions
     * api-version: 2021-06-01
     * x-ms-examples: Get upgrade path
     */
    /**
     * Sample code: Get upgrade path.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getUpgradePath(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .clusters()
            .listUpgradableVersionsWithResponse(
                "resRg",
                "myCluster",
                new UpgradableVersionsDescription().withTargetVersion("7.2.432.9590"),
                Context.NONE);
    }
}
```
