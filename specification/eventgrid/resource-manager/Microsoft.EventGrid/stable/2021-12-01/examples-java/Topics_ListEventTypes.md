Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-eventgrid_1.1.0-beta.3/sdk/eventgrid/azure-resourcemanager-eventgrid/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for Topics ListEventTypes. */
public final class Main {
    /*
     * x-ms-original-file: specification/eventgrid/resource-manager/Microsoft.EventGrid/stable/2021-12-01/examples/Topics_ListEventTypes.json
     */
    /**
     * Sample code: Topics_ListEventTypes.
     *
     * @param manager Entry point to EventGridManager.
     */
    public static void topicsListEventTypes(com.azure.resourcemanager.eventgrid.EventGridManager manager) {
        manager
            .topics()
            .listEventTypes("examplerg", "Microsoft.Storage", "storageAccounts", "ExampleStorageAccount", Context.NONE);
    }
}
```