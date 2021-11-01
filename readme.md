## kirki - options 

```
<?php
ITClan_Kirki::add_section('color_settings', array(
	'title'          => esc_html__('Theme Color', 'ic-core'),
	'panel'          => 'theme_options',
	'capability'     => 'edit_theme_options',
	'theme_supports' => '',
));


ITClan_Kirki::add_field( 'theme_config_id', [
	'type'        => 'color',
	'settings'    => 'primary_color',
	'label'       => __( 'Primary Color', 'ic-core' ),
	'section'     => 'color_settings',
	'default'     => '#005EEB',
] );

```

## add settings
```
include( IC_INC_DIR . '/kirki-options/theme-color.php' );
```

## retrive
```
$text_color = get_theme_mod( 'text_color', '#005EEB' );
color: '. esc_attr($primary_color) .';
```


## include to function
```
require_once( IC_INC_DIR . '/theme-color.php' );
wp_add_inline_style( 'ic-core', $theme_color );
```