.. _doc_item_asset_barrel:

Barrel Assets
=============

Barrel attachments are inventory items that can be attached to ranged weapons.

This inherits the :ref:`CaliberAsset <doc_item_asset_caliber>` class.

Item Asset Properties
---------------------

**GUID** *32-digit hexadecimal*: Refer to :ref:`GUID <doc_data_guid>` documentation.

**Type** *enum* (``Barrel``)

**ID** *uint16*: Must be a unique identifier.

Barrel Asset Properties
-----------------------

**Bullet_Gravity_Multiplier** *float*: Multiplier for gravity's acceleration. This multiplier defaults to 4 because (as of 2023-05-18) Unturned's maximum engagement distance is rather short, but the default will be raised in the future if/when network improvements are made. It can be set to 1 for more realistic bullet drop. Gravity defaults to 9.81 m/s², or can be configured in the :ref:`doc_asset_validation`.

.. deprecated:: 3.23.7.0 **Ballistic_Drop** *float*: Replaced by ``Bullet_Gravity_Multiplier``. Existing values are automatically converted if Bullet_Gravity_Multiplier is not specified. The conversion is logged during :ref:`doc_asset_validation`.

**Braked** *flag*: Specified if a muzzle flash should be hidden.

**Durability** *byte*: Amount of quality lost after each firing of the ranged weapon. When this value is greater than 0, the item always has a visible item quality shown. Defaults to 0.

**Gunshot_Rolloff_Distance_Multiplier** *float*: Multiplier on gunshot rolloff distance. Defaults to 0.5 if Silenced, otherwise to 1.

**Silenced** *flag*: Specified if alerts should not be generated.

**Volume** *float*: Multiplier on gunfire sound volume.
