Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-purview_1.0.0-beta.1/sdk/purview/azure-resourcemanager-purview/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.purview.models.Account;
import java.util.HashMap;
import java.util.Map;

/** Samples for Accounts Update. */
public final class Main {
    /*
     * operationId: Accounts_Update
     * api-version: 2021-07-01
     * x-ms-examples: Accounts_Update
     */
    /**
     * Sample code: Accounts_Update.
     *
     * @param manager Entry point to PurviewManager.
     */
    public static void accountsUpdate(com.azure.resourcemanager.purview.PurviewManager manager) {
        Account resource =
            manager
                .accounts()
                .getByResourceGroupWithResponse("SampleResourceGroup", "account1", Context.NONE)
                .getValue();
        resource.update().withTags(mapOf("newTag", "New tag value.")).apply();
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
