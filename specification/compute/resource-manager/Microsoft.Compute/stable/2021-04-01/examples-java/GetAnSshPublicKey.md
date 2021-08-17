```java
import com.azure.core.util.Context;

/** Samples for SshPublicKeys GetByResourceGroup. */
public final class GetAnSshPublicKey {
    /*
     * operationId: SshPublicKeys_Get
     * api-version: 2021-04-01
     * x-ms-examples: Get an ssh public key.
     */
    /**
     * Sample code: Get an ssh public key.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void getAnSshPublicKey(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSshPublicKeys()
            .getByResourceGroupWithResponse("myResourceGroup", "mySshPublicKeyName", Context.NONE);
    }
}
```