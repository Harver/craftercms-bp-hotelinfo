# Crafter CMS Blueprint: Hotel Info

Hotel Info is a stylish multiple page Crafter 3 blueprint with video backgrounds. It's based on the HOTEL FREE CSS TEMPLATE theme by [The Bootstrap Themes](http://www.free-css.com/free-css-templates/page207/hotel) 

# Known Issues

## Video Playback on Safari
In Safari (Chrome and Firefox work properly), videos are not displayed. This seems to occur due to lack of implementation for [206 Partial Content](https://httpstatuses.com/206) and its associated headers. However, this can be fixed by configuring Tomcat to serve this files statically.

To do this, edit the file `apache-tomcat/conf/server.xml` and add a context like this:

    <Context docBase="../../data/repos/sites/<your-site>/sandbox/static-assets/video" path="/static-assets/video" />

You may need to tweak the docbase a bit, to begin with, replace `<your-site>` with your site's name. You may also prefer to point to `published/` instead of `sandbox/`, and for your live site, it's a different path, similar to `/opt/crafter/bin/delivery/data/deployer/deployments/<your-environment>/<your-site>/`.
More information in [Tomcat's docs](https://tomcat.apache.org/tomcat-8.0-doc/config/context.html).

# Additional Licenses
The Art Showcase blueprint also contains the following resources:

- Sea View Drone HD Free Video Background from https://www.youtube.com/watch?v=nkxGbhQzLMM under Public Domain License
