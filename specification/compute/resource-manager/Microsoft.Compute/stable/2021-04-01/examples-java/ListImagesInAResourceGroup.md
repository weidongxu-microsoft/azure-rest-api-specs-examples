```java
import com.azure.core.util.Context;

/** Samples for Images ListByResourceGroup. */
public final class ListImagesInAResourceGroup {
    /*
     * operationId: Images_ListByResourceGroup
     * api-version: 2021-04-01
     * x-ms-examples: List all virtual machine images in a resource group.
     */
    /**
     * Sample code: List all virtual machine images in a resource group.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void listAllVirtualMachineImagesInAResourceGroup(
        com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getImages()
            .listByResourceGroup("myResourceGroup", Context.NONE);
    }
}
```