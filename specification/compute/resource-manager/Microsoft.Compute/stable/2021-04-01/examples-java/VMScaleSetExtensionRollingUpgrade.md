```java
import com.azure.core.util.Context;

/** Samples for VirtualMachineScaleSetRollingUpgrades StartExtensionUpgrade. */
public final class VMScaleSetExtensionRollingUpgrade {
    /*
     * operationId: VirtualMachineScaleSetRollingUpgrades_StartExtensionUpgrade
     * api-version: 2021-04-01
     * x-ms-examples: Start an extension rolling upgrade.
     */
    /**
     * Sample code: Start an extension rolling upgrade.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void startAnExtensionRollingUpgrade(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getVirtualMachineScaleSetRollingUpgrades()
            .startExtensionUpgrade("myResourceGroup", "{vmss-name}", Context.NONE);
    }
}
```