# Geocoder-Tableau-Extension

Working Repository for BEC & GVEC for work done on the Geocoding Tableau Extension.

Geocode addresses within a Tableau Dashboard, and allow Dashboard Filters and Actions to interact with the map.

## Administration

**Repository Admin:** John R Lister - Geospatial Applications Developer, Bluebonnet Electric Cooperative

**Primary Author:** Courtney Pesak - GIS Manager/System Administrator, Guadalupe Valley Electric Cooperative

## Contributing
* Pulling, committing, forking:
    * Pull requests are welcome!
    * For individual development and requested changes please fork the repository.
    * **DO NOT COMMIT YOUR API KEYS**
       * Accidents happen, Admin will try to control the accidental publishing of API tokens
       * It really falls on **YOU** the developer, if you don't want someone using your token... don't expose it! 

* Issue Tracking
   * For issues please open an issue tracking ticket to discuss what is going wrong.
   * Review the Bug Tracking Card sheet to see the status of your issue

Please make sure to update tests as appropriate.

## The Geeky stuff

Spin up a local Web Service to test your Extensions:
```bash
# Development is easy when you are able to serve your extensions on a URL 
# We don't always have a designated Web Server available to mess around on...
# BUT WE CAN SPIN UP A LOCAL HOST HTTP SERVER
# Execute this bad boy in the location of your extension to generate a URL Like:
# http://localhost:8888/index.html SPIN IT UP WHERE YOUR EXTENSION CODE LIVES
python -m SimpleHTTPServer 8888
```

Structure your .TREX File like so:
```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest manifest-version="0.1" xmlns="http://www.tableau.com/xml/extension_manifest">
  <dashboard-extension id="com.tableau.extensions.blah bla.blah" extension-version="0.6.0">
    <default-locale>en_US</default-locale>
    <name resource-id="name"/>
    <description>BEC Sample</description>
    <author name="John R Lister - GIS Whizzle Shnizzle" email="imafrican@imnotexposingmyemail.coop" organization="BEC" website="https://www.tableau.com"/>
    <min-api-version>0.8</min-api-version>
    <source-location>
      <url>http://localhost:8888/index.html</url>
    </source-location>
    <icon>some really cool icon ID... ask John for his</icon>
    <permissions>
      <permission>full data</permission>
    </permissions>
  </dashboard-extension>
  <resources>
    <resource id="name">
      <text locale="en_US">BEC Sample</text>
    </resource>
  </resources>
</manifest>
```

## Usage

```python
import foobar

foobar.pluralize('word') # returns 'words'
foobar.pluralize('goose') # returns 'geese'
foobar.singularize('phenomena') # returns 'phenomenon'
```



## License
[MIT](https://choosealicense.com/licenses/mit/)


