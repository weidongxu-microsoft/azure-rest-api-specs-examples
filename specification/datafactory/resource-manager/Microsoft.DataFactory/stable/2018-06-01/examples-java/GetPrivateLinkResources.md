```java
import com.azure.core.util.Context;

/** Samples for PrivateLinkResources Get. */
public final class GetPrivateLinkResources {
    /*
     * operationId: PrivateLinkResources_Get
     * api-version: 2018-06-01
     * x-ms-examples: Get private link resources of a site
     */
    /**
     * Sample code: Get private link resources of a site.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void getPrivateLinkResourcesOfASite(
        com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager.privateLinkResources().getWithResponse("exampleResourceGroup", "exampleFactoryName", Context.NONE);
    }
}
```