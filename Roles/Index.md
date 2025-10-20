# Role Management

When we click Administration / Roles menu, we enter to the role management page:

<img src="images/role-management-core-3.png" alt="Role management page" class="img-thumbnail" />

Roles are used to **group permissions**. When a user has a role, then the user will have all permissions of that role.


Roles can be dynamic or static:

- **Static role**: A static role has a known **name** (like 'admin') and this name can't be changed. (But the **display name** can be changed). It's created on the system startup and can not be deleted on the UI. Thus, we can write codes based on a static role name.
- **Dynamic role**: We can create a dynamic role after deployment. Then we can grant permissions for that role, we can assign the role to some users and we can delete it. We can not know names of dynamic roles in development time.

One or more roles can be set as **default**. Default roles are assigned to newly added/registered users by default. This is not a development time property and can be set or changed after deployment.

#### Role Permissions

Since roles are used to group permissions, we can set permissions of a role while creating or editing as shown below:

<img src="images/role-permissions-core-1.png" alt="Role Permissions" class="img-thumbnail" />

*Note that not all permissions shown in the figure above.*

## Permissions

Access to Role Management features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Roles | View role records |
| Create Roles | Create new roles |
| Edit Roles | Modify existing roles |
| Delete Roles | Remove roles |

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Users](../System/Users.md) | View/manage users (assign roles to users) |
| [Organization Units](../System/OrganizationUnits.md) | Manage roles within organization units |

## Related Documentation

* [Users](../System/Users.md) - User account management
* [Organization Units](../System/OrganizationUnits.md) - Organizational structure

