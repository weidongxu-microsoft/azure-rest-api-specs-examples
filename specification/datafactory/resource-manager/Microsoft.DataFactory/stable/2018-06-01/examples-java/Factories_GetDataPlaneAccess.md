```java
import com.azure.core.util.Context;
import com.azure.resourcemanager.datafactory.models.UserAccessPolicy;

/** Samples for Factories GetDataPlaneAccess. */
public final class FactoriesGetDataPlaneAccess {
    /*
     * operationId: Factories_GetDataPlaneAccess
     * api-version: 2018-06-01
     * x-ms-examples: Factories_GetDataPlaneAccess
     */
    /**
     * Sample code: Factories_GetDataPlaneAccess.
     *
     * @param manager Entry point to DataFactoryManager.
     */
    public static void factoriesGetDataPlaneAccess(com.azure.resourcemanager.datafactory.DataFactoryManager manager) {
        manager
            .factories()
            .getDataPlaneAccessWithResponse(
                "exampleResourceGroup",
                "exampleFactoryName",
                new UserAccessPolicy()
                    .withPermissions("r")
                    .withAccessResourcePath("")
                    .withProfileName("DefaultProfile")
                    .withStartTime("2018-11-10T02:46:20.2659347Z")
                    .withExpireTime("2018-11-10T09:46:20.2659347Z"),
                Context.NONE);
    }
}
```