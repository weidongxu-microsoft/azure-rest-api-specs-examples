Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for ApplicationTypeVersions Delete. */
public final class Main {
    /*
     * operationId: ApplicationTypeVersions_Delete
     * api-version: 2021-06-01
     * x-ms-examples: Delete an application type version
     */
    /**
     * Sample code: Delete an application type version.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void deleteAnApplicationTypeVersion(
        com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager.applicationTypeVersions().delete("resRg", "myCluster", "myAppType", "1.0", Context.NONE);
    }
}
```
