```java
import com.azure.core.util.Context;

/** Samples for SshPublicKeys GenerateKeyPair. */
public final class GenerateSshKeyPair {
    /*
     * operationId: SshPublicKeys_GenerateKeyPair
     * api-version: 2021-04-01
     * x-ms-examples: Generate an SSH key pair.
     */
    /**
     * Sample code: Generate an SSH key pair.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void generateAnSSHKeyPair(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSshPublicKeys()
            .generateKeyPairWithResponse("myResourceGroup", "mySshPublicKeyName", Context.NONE);
    }
}
```