# munin-wp-plugins

WordPress plugin status graphs for Munin. Shows the number of installed plugins, active plugins and updatable plugins.
Requires [WP-CLI](http://wp-cli.org/) to be available.

## Configuration

Copy the `wp_plugins` plugin to your Munin plugins directory. You can create symbolic links if the target node has more othan one WordPress site.

Add the following plugin configuration to your plugin-conf.d configs:

```
[wp_plugins]
user dave
env.WP_PATH /home/dave/wordpress/
env.WP_NAME "Dave's WordPress Site"
```

*Always* run as the regular constrained PHP user (be it www, apache), do not let the plugin run as munin, root, etc.

## License

GPLv3 (http://www.gnu.org/licenses/gpl-3.0.txt)
