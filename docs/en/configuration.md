# Configuration

**Example Definition:**

    protected $fields = [
        'example' => [
            'type'   => 'anomaly.field_type.addon',
            'config' => [
                'type'       => null,
                'search'     => null,
                'theme_type' => null,
                'handler'    => 'Anomaly\AddonFieldType\AddonFieldTypeOptions@handle'
            ]
        ]
    ];

### `type`

The type of addons to display in the dropdown. Valid options are `null`, `module`, `theme`, `plugin`, `extension`, or `field_type`. The default value is `null`.

### `search`

The extension search argument. Any valid extension search string like `anomaly.module.files::storage_adapter.*` can be used. The default value is `null`.

This option is ignored unless the extension type is chosen.

### `theme_type`

The theme type to display. Valid options are `null`, `admin`, or `standard`. The default value is `null`.

This option is ignored unless the theme type is chosen.

### `handler`

The options handler callable string. Any valid callable class string can be used. The default value is `'Anomaly\AddonFieldType\AddonFieldTypeOptions@handle'`.

The handler is responsible for setting the available options on the field type instance.

**NOTE:** This option can not be through the GUI configuration. 