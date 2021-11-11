Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.dataprotection.models.ResourceGuardResource;
import java.util.HashMap;
import java.util.Map;

/** Samples for ResourceGuards Patch. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/ResourceGuardCRUD/PatchResourceGuard.json
     */
    /**
     * Sample code: Patch ResourceGuard.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void patchResourceGuard(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        ResourceGuardResource resource =
            manager
                .resourceGuards()
                .getByResourceGroupWithResponse("SampleResourceGroup", "swaggerExample", Context.NONE)
                .getValue();
        resource.update().withTags(mapOf("newKey", "newVal")).apply();
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
