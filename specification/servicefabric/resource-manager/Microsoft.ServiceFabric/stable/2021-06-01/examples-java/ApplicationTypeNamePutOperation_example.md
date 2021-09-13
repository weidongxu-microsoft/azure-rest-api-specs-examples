Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-servicefabric_1.0.0-beta.2/sdk/servicefabric/azure-resourcemanager-servicefabric/README.md) on how to add the SDK to your project and authenticate.

```java
import java.util.HashMap;
import java.util.Map;

/** Samples for ApplicationTypes CreateOrUpdate. */
public final class Main {
    /*
     * operationId: ApplicationTypes_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Put an application type
     */
    /**
     * Sample code: Put an application type.
     *
     * @param manager Entry point to ServiceFabricManager.
     */
    public static void putAnApplicationType(com.azure.resourcemanager.servicefabric.ServiceFabricManager manager) {
        manager
            .applicationTypes()
            .define("myAppType")
            .withExistingCluster("resRg", "myCluster")
            .withTags(mapOf())
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
