Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import java.util.HashMap;
import java.util.Map;

/** Samples for ResourceGuards Put. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/ResourceGuardCRUD/PutResourceGuard.json
     */
    /**
     * Sample code: Create ResourceGuard.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void createResourceGuard(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .resourceGuards()
            .define("swaggerExample")
            .withRegion("WestUS")
            .withExistingResourceGroup("SampleResourceGroup")
            .withTags(mapOf("key1", "val1"))
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
