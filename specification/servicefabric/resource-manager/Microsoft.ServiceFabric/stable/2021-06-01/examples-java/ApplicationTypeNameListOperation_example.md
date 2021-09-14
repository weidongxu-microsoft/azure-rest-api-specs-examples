Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for ApplicationTypes List. */
public final class Main {
    /*
     * operationId: ApplicationTypes_List
     * api-version: 2021-06-01
     * x-ms-examples: Get a list of application type name resources
     */
    /**
     * Sample code: Get a list of application type name resources.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void getAListOfApplicationTypeNameResources(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.applicationTypes().listWithResponse("resRg", "myCluster", Context.NONE);
    }
}
```
