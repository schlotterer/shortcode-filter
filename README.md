# shortcode-filter
JS override to fix WP creating a new shortcode block every time yo paste one.

Just add the file and enqueue in the admin with these dependencies.

wp_enqueue_script(
        'custom-block-handler',
        get_template_directory_uri() . '/assets/built/js/raw-handler.js', // Path to your custom JS file
        array( 'wp-blocks', 'wp-hooks', 'wp-element' ), // Dependencies required for the script to work
        '1.0',
        true
    );
