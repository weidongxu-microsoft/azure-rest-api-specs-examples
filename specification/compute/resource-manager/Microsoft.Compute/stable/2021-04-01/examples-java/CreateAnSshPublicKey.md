```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.compute.fluent.models.SshPublicKeyResourceInner;

/** Samples for SshPublicKeys Create. */
public final class CreateAnSshPublicKey {
    /*
     * operationId: SshPublicKeys_Create
     * api-version: 2021-04-01
     * x-ms-examples: Create a new SSH public key resource.
     */
    /**
     * Sample code: Create a new SSH public key resource.
     *
     * @param azure The entry point for accessing resource management APIs in Azure.
     */
    public static void createANewSSHPublicKeyResource(com.azure.resourcemanager.AzureResourceManager azure) {
        azure
            .virtualMachines()
            .manager()
            .serviceClient()
            .getSshPublicKeys()
            .createWithResponse(
                "myResourceGroup",
                "mySshPublicKeyName",
                new SshPublicKeyResourceInner().withLocation("westus").withPublicKey("{ssh-rsa public key}"),
                Context.NONE);
    }
}
```