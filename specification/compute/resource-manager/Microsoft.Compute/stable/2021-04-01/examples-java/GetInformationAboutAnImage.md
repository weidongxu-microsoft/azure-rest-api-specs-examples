```java
import com.azure.core.util.Context;

/** Samples for Images GetByResourceGroup. */
public final class GetInformationAboutAnImage {
    /*
     * operationId: Images_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get information about a virtual machine image.
     */
    /**
     * Sample code: Get information about a virtual machine image.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getInformationAboutAVirtualMachineImage(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getImages()
            .getByResourceGroupWithResponse("myResourceGroup", "myImage", null, Context.NONE);
    }
}
```