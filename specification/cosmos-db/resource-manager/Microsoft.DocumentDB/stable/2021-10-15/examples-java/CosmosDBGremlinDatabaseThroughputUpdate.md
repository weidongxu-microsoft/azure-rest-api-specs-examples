Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager_2.10.0/sdk/resourcemanager/azure-resourcemanager/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.cosmos.models.ThroughputSettingsResource;
import com.azure.resourcemanager.cosmos.models.ThroughputSettingsUpdateParameters;
import java.util.HashMap;
import java.util.Map;

/** Samples for GremlinResources UpdateGremlinDatabaseThroughput. */
public final class Main {
    /*
     * x-ms-original-file: specification/cosmos-db/resource-manager/Microsoft.DocumentDB/stable/2021-10-15/examples/CosmosDBGremlinDatabaseThroughputUpdate.json
     */
    /**
     * Sample code: CosmosDBGremlinDatabaseThroughputUpdate.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void cosmosDBGremlinDatabaseThroughputUpdate(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .cosmosDBAccounts()
            .manager()
            .serviceClient()
            .getGremlinResources()
            .updateGremlinDatabaseThroughput(
                "rg1",
                "ddb1",
                "databaseName",
                new ThroughputSettingsUpdateParameters()
                    .withLocation("West US")
                    .withTags(mapOf())
                    .withResource(new ThroughputSettingsResource().withThroughput(400)),
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