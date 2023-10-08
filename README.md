# Alternative Auto Updates Blueprint

![overview](https://raw.githubusercontent.com/ludeeus/alternative-auto-update-blueprint/main/static/overview.png)

This will automatically update the target update entity.

But it will not do the latest and greatest.
Instead it will install the latest patch version when a new minor version is realeased.
When this trigger on a version change that does not result in an update, the update will be hidden so you do not see a notification for it in the UI.


There are some exceptions:
- This will install the latest patch version if you are currently on the same minor version
- This will install all beta versions if you are on beta currently or the latest version is beta
- This will install all dev versions if you are on dev currently or the latest version is dev


Note that this will only work for update entities that supports installing a spesific version.
