Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.resourcemanager.servicefabric.models.ApplicationMetricDescription;
import com.azure.resourcemanager.servicefabric.models.ApplicationUpgradePolicy;
import com.azure.resourcemanager.servicefabric.models.ArmApplicationHealthPolicy;
import com.azure.resourcemanager.servicefabric.models.ArmRollingUpgradeMonitoringPolicy;
import com.azure.resourcemanager.servicefabric.models.ArmServiceTypeHealthPolicy;
import com.azure.resourcemanager.servicefabric.models.ArmUpgradeFailureAction;
import com.azure.resourcemanager.servicefabric.models.RollingUpgradeMode;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for Applications CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Applications_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Put an application with maximum parameters
     */
    /**
     * Sample code: Put an application with maximum parameters.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void putAnApplicationWithMaximumParameters(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .applications()
            .define("myApp")
            .withExistingCluster("resRg", "myCluster")
            .withTags(mapOf())
            .withTypeName("myAppType")
            .withTypeVersion("1.0")
            .withParameters(mapOf("param1", "value1"))
            .withUpgradePolicy(
                new ApplicationUpgradePolicy()
                    .withUpgradeReplicaSetCheckTimeout("01:00:00")
                    .withForceRestart(false)
                    .withRollingUpgradeMonitoringPolicy(
                        new ArmRollingUpgradeMonitoringPolicy()
                            .withFailureAction(ArmUpgradeFailureAction.ROLLBACK)
                            .withHealthCheckWaitDuration("00:02:00")
                            .withHealthCheckStableDuration("00:05:00")
                            .withHealthCheckRetryTimeout("00:10:00")
                            .withUpgradeTimeout("01:00:00")
                            .withUpgradeDomainTimeout("1.06:00:00"))
                    .withApplicationHealthPolicy(
                        new ArmApplicationHealthPolicy()
                            .withConsiderWarningAsError(true)
                            .withMaxPercentUnhealthyDeployedApplications(0)
                            .withDefaultServiceTypeHealthPolicy(
                                new ArmServiceTypeHealthPolicy()
                                    .withMaxPercentUnhealthyServices(0)
                                    .withMaxPercentUnhealthyPartitionsPerService(0)
                                    .withMaxPercentUnhealthyReplicasPerPartition(0)))
                    .withUpgradeMode(RollingUpgradeMode.MONITORED))
            .withMinimumNodes(1L)
            .withMaximumNodes(3L)
            .withRemoveApplicationCapacity(false)
            .withMetrics(
                Arrays
                    .asList(
                        new ApplicationMetricDescription()
                            .withName("metric1")
                            .withMaximumCapacity(3L)
                            .withReservationCapacity(1L)
                            .withTotalApplicationCapacity(5L)))
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
