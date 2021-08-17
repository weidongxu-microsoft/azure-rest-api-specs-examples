```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.DedicatedHostGroupInner;
import java.util.Arrays;
import java.util.HashMap;
import java.util.Map;

/** Samples for DedicatedHostGroups CreateOrUpdate. */
public final class CreateOrUpdateADedicatedHostGroup {
    /*
     * operationId: DedicatedHostGroups_CreateOrUpdate
     * api-version: 2021-04-01
     * x-ms-examples: Create or update a dedicated host group.
     */
    /**
     * Sample code: Create or update a dedicated host group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createOrUpdateADedicatedHostGroup(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDedicatedHostGroups()
            .createOrUpdateWithResponse(
                "myResourceGroup",
                "myDedicatedHostGroup",
                new DedicatedHostGroupInner()
                    .withLocation("westus")
                    .withTags(mapOf("department", "finance"))
                    .withZones(Arrays.asList("1"))
                    .withPlatformFaultDomainCount(3)
                    .withSupportAutomaticPlacement(true),
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