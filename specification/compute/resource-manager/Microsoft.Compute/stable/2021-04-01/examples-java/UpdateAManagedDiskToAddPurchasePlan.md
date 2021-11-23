Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager_2.10.0/sdk/resourcemanager/azure-resourcemanager/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.models.DiskUpdate;
import com.azure.resourcemanager.compute.models.PurchasePlanAutoGenerated;

/** Samples for Disks Update. */
public final class Main {
    /*
     * x-ms-original-file: specification/compute/resource-manager/Microsoft.Compute/stable/2021-04-01/examples/UpdateAManagedDiskToAddPurchasePlan.json
     */
    /**
     * Sample code: Update a managed disk to add purchase plan.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void updateAManagedDiskToAddPurchasePlan(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getDisks()
            .update(
                "myResourceGroup",
                "myDisk",
                new DiskUpdate()
                    .withPurchasePlan(
                        new PurchasePlanAutoGenerated()
                            .withName("myPurchasePlanName")
                            .withPublisher("myPurchasePlanPublisher")
                            .withProduct("myPurchasePlanProduct")
                            .withPromotionCode("myPurchasePlanPromotionCode")),
                Context.NONE);
    }
}
```