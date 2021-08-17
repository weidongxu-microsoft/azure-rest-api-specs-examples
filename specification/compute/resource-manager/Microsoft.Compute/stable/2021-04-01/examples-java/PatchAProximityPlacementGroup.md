```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.ProximityPlacementGroupUpdate;
import java.util.HashMap;
import java.util.Map;

/** Samples for ProximityPlacementGroups Update. */
public final class PatchAProximityPlacementGroup {
    /*
     * operationId: ProximityPlacementGroups_Update
     * api-version: 2021-04-01
     * x-ms-examples: Create a proximity placement group.
     */
    /**
     * Sample code: Create a proximity placement group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createAProximityPlacementGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getProximityPlacementGroups()
            .updateWithResponse(
                "myResourceGroup",
                "myProximityPlacementGroup",
                new ProximityPlacementGroupUpdate().withTags(mapOf("additionalProp1", "string")),
                Context.NONE);
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