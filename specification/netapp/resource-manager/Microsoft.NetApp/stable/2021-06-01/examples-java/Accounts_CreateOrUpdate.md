Read the [SDK documentation](https://github.com/Azure/azure-sdk-for-java/blob/azure-resourcemanager-netapp_1.0.0-beta.5/sdk/netapp/azure-resourcemanager-netapp/README.md) on how to add the SDK to your project and authenticate.

```java
import com.azure.resourcemanager.netapp.models.ActiveDirectory;
import java.util.Arrays;

/** Samples for Accounts CreateOrUpdate. */
public final class Main {
    /*
     * operationId: Accounts_CreateOrUpdate
     * api-version: 2021-06-01
     * x-ms-examples: Accounts_CreateOrUpdate
     */
    /**
     * Sample code: Accounts_CreateOrUpdate.
     *
     * @param manager Entry point to NetAppFilesManager.
     */
    public static void accountsCreateOrUpdate(com.azure.resourcemanager.netapp.NetAppFilesManager manager) {
        manager
            .accounts()
            .define("account1")
            .withRegion("eastus")
            .withExistingResourceGroup("myRG")
            .withActiveDirectories(
                Arrays
                    .asList(
                        new ActiveDirectory()
                            .withUsername("ad_user_name")
                            .withPassword("ad_password")
                            .withDomain("10.10.10.3")
                            .withDns("10.10.10.3, 10.10.10.4")
                            .withSmbServerName("SMBServer")
                            .withOrganizationalUnit("Engineering")
                            .withSite("SiteName")
                            .withAesEncryption(true)
                            .withLdapSigning(false)
                            .withLdapOverTls(false)))
            .create();
    }
}
```
