Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for LinkedServices Get. */
public final class Main {
    /*
     * operationId: LinkedServices_Get
     * api-version: 2018-06-01
     * x-ms-examples: LinkedServices_Get
     */
    /**
     * Sample code: LinkedServices_Get.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void linkedServicesGet(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .linkedServices()
            .getWithResponse("exampleResourceGroup", "exampleFactoryName", "exampleLinkedService", null, Context.NONE);
    }
}
```
