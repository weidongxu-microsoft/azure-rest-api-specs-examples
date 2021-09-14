Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApplicationTypeVersions List. */
public final class Main {
    /*
     * operationId: ApplicationTypeVersions_List
     * api-version: 2021-06-01
     * x-ms-examples: Get a list of application type version resources
     */
    /**
     * Sample code: Get a list of application type version resources.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getAListOfApplicationTypeVersionResources(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.applicationTypeVersions().listWithResponse("resRg", "myCluster", "myAppType", Context.NONE);
    }
}
```
