CQ5-RequireJS
=============

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/3lux/cq5-requirejs/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

JSP code to enable dynamic creation of requireJS calls based on the components dropped in a CQ5 page template.

1. Place this code in the head or headlibs.jsp file of your page template component.

2. Add a `String[]` (multi) property called "requireJS" to your components that have a requireJS configuration.

  **For example (via .content.xml template file):**
  ```xml
  <jcr:root xmlns:sling="http://sling.apache.org/jcr/sling/1.0" xmlns:cq="http://www.day.com/jcr/cq/1.0" xmlns:jcr="http://www.jcp.org/jcr/1.0"
   jcr:primaryType="cq:Component"
   jcr:title="Color Picker"
   sling:resourceSuperType="foundation/components/parbase"
   allowedParents="[*/parsys]"
   componentGroup="My Components"
   requireJS="[jquery,color_picker]"/>
   ```

3. Tweak the script tag at the bottom to match the location of your require.min.js and configuration files.

4. Enjoy!

