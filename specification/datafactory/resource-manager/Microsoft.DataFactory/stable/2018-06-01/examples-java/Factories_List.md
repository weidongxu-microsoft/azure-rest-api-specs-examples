Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-datafactory_1.0.0-beta.5/sdk/datafactory/azure-resourcemanager-datafactory/README.md) on how to add the SDK to your project and authenticate.

```java

import com.azure.core.util.Context;

/** Samples for Factories List. */
public final class Main {
    /*
     * operationId: Factories_List
     * api-version: 2018-06-01
     * x-ms-examples: Factories_List
     */
    /**
     * Sample code: Factories_List.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesList(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.factories().list(Context.NONE);
    }
}
```
