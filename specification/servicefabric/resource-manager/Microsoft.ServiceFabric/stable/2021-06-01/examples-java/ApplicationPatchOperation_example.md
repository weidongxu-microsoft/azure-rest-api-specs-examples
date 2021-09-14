Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.servicefabric.models.ApplicationMetricDescription;
import com.azure.resourcemanager.servicefabric.models.ApplicationResource;
import java.util.Arrays;

/** Samples for Applications Update. */
public final class Main {
    /*
     * operationId: Applications_Update
     * api-version: 2021-06-01
     * x-ms-examples: Patch an application
     */
    /**
     * Sample code: Patch an application.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void patchAnApplication(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        ApplicationResource resource =
            manager.applications().getWithResponse("resRg", "myCluster", "myApp", Context.NONE).getValue();
        resource
            .update()
            .withTypeVersion("1.0")
            .withRemoveApplicationCapacity(false)
            .withMetrics(
                Arrays
                    .asList(
                        new ApplicationMetricDescription()
                            .withName("metric1")
                            .withMaximumCapacity(3L)
                            .withReservationCapacity(1L)
                            .withTotalApplicationCapacity(5L)))
            .apply();
    }
}
```
