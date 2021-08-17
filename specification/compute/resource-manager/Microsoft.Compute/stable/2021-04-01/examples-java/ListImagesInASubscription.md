```java
import com.azure.core.util.Context;

/** Samples for Images List. */
public final class ListImagesInASubscription {
    /*
     * operationId: Images_List
     * api-version: 2021-04-01
     * x-ms-examples: List all virtual machine images in a subscription.
     */
    /**
     * Sample code: List all virtual machine images in a subscription.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllVirtualMachineImagesInASubscription(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure.virtualMachines().manager().serviceClient().getImages().list(Context.NONE);
    }
}
```