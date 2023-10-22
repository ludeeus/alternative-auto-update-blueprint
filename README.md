# Alternative Auto Updates Blueprint

![overview](https://raw.githubusercontent.com/ludeeus/alternative-auto-update-blueprint/main/static/overview.png)

This will automatically update the target update entity.

But it will not do the latest and greatest.
Instead it will install the latest patch version when a new minor version is released.
When this trigger on a version change that does not result in an update, the update will be hidden so you do not see a notification for it in the UI.


There are some exceptions:
- This will install the latest patch version if you are currently on the same minor version
- This will install all beta versions if you are on beta currently or the latest version is beta
- This will install all dev versions if you are on dev currently or the latest version is dev


Note that this will only work for update entities that supports installing a spesific version.

## Examples

### New minor version released

If you are currently running `2023.1.5`, when `2023.2.0` -> `2023.2.99` are released, nothing will happen.

When `2023.3.0` is released, it will install the latest patch of the previous minor version (`2023.2.99` in this example).


### New patch

If you are currently running `2023.1.5`, if `2023.1.6` is released (newer patch on the same minor version), this will be installed.

## Beta versions

If you are running `2023.1.5` and `2023.2.0b0` is released, this is installed.
If you are running `2023.1.0b0` and `2023.2.0` is released, this is installed.

## Dev versions

If you are running `2023.1.5` and `2023.2.0dev0` is released, this is installed.
If you are running `2023.1.0dev0` and `2023.2.0` is released, this is installed.


## Import directly in Home Assistant

[Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2Fludeeus%2Falternative-auto-update-blueprint%2Fmain%2Falternative_auto_updates.yaml)


<details>
<summary>
🤫
</summary>

## Download with HACS

[Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/redirect/hacs_repository/?owner=ludeeus&repository=alternative-auto-update-blueprint&category=blueprint)

</details>