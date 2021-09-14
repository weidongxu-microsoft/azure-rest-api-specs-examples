Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.servicefabric.models.DiagnosticsStorageAccountConfig;
import com.azure.resourcemanager.servicefabric.models.DurabilityLevel;
import com.azure.resourcemanager.servicefabric.models.EndpointRangeDescription;
import com.azure.resourcemanager.servicefabric.models.NodeTypeDescription;
import com.azure.resourcemanager.servicefabric.models.ReliabilityLevel;
import com.azure.resourcemanager.servicefabric.models.SettingsParameterDescription;
import com.azure.resourcemanager.servicefabric.models.SettingsSectionDescription;
import com.azure.resourcemanager.servicefabric.models.UpgradeMode;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for Clusters CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Clusters_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Put a cluster with minimum parameters
     */
    /**
     * Sample code: Put a cluster with minimum parameters.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void putAClusterWithMinimumParameters(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .clusters()
            .define("myCluster")
            .withRegion("eastus")
            .withExistingResourceGroup("resRg")
            .withTags(mapOf())
            .withDiagnosticsStorageAccountConfig(
                new DiagnosticsStorageAccountConfig()
                    .withStorageAccountName("diag")
                    .withProtectedAccountKeyName("StorageAccountKey1")
                    .withBlobEndpoint("https://diag.blob.core.windows.net/")
                    .withQueueEndpoint("https://diag.queue.core.windows.net/")
                    .withTableEndpoint("https://diag.table.core.windows.net/"))
            .withFabricSettings(
                Arrays
                    .asList(
                        new SettingsSectionDescription()
                            .withName("UpgradeService")
                            .withParameters(
                                Arrays
                                    .asList(
                                        new SettingsParameterDescription()
                                            .withName("AppPollIntervalInSeconds")
                                            .withValue("60")))))
            .withManagementEndpoint("http://myCluster.eastus.cloudapp.azure.com:19080")
            .withNodeTypes(
                Arrays
                    .asList(
                        new NodeTypeDescription()
                            .withName("nt1vm")
                            .withClientConnectionEndpointPort(19000)
                            .withHttpGatewayEndpointPort(19007)
                            .withDurabilityLevel(DurabilityLevel.BRONZE)
                            .withApplicationPorts(
                                new EndpointRangeDescription().withStartPort(20000).withEndPort(30000))
                            .withEphemeralPorts(new EndpointRangeDescription().withStartPort(49000).withEndPort(64000))
                            .withIsPrimary(true)
                            .withVmInstanceCount(5)))
            .withReliabilityLevel(ReliabilityLevel.SILVER)
            .withUpgradeMode(UpgradeMode.AUTOMATIC)
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
