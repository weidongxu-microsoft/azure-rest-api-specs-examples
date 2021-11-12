Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-dataprotection_1.0.0-beta.1/sdk/dataprotection/azure-resourcemanager-dataprotection/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.core.util.Context;

/** Samples for RecoveryPoints Get. */
public final class Main {
    /*
     * x-ms-original-file: specification/dataprotection/resource-manager/Microsoft.DataProtection/stable/2021-07-01/examples/BackupInstanceOperations/GetRecoveryPoint.json
     */
    /**
     * Sample code: Get Recovery Point.
     *
     * @param manager Entry point to DataProtectionManager.
     */
    public static void getRecoveryPoint(com.azure.resourcemanager.dataprotection.DataProtectionManager manager) {
        manager
            .recoveryPoints()
            .getWithResponse(
                "PratikPrivatePreviewVault1",
                "000pikumar",
                "testInstance1",
                "7fb2cddd-c5b3-44f6-a0d9-db3c4f9d5f25",
                Context.NONE);
    }
}
```
