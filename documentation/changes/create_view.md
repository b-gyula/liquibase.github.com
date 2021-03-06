---
layout: default
title: Docs | Change 'createView'
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'createView'

Create a new database view

## Available Attributes ##

<table class='attribs'>
<tr><th>Name</th><th>Description</th></tr>
<tr><td class="name">catalogName</td><td class="desc">Name of the catalog<span class="right"><span class="since">@ v3.0</span><span class="sample">E.g. <span class="val">&#x27;cat&#x27;</span></span></span></td></tr>
<tr><td class="name">encoding</td><td class="desc">Name of the encoding (as specified in <a href="http://docs.oracle.com/javase/7/docs/api/java/nio/charset/Charset.html">java.nio.Charset javadoc</a>) used in the file defined in the `path` attribute<span class="right"><span class="default">Default: <span class="val">&#x27;utf-8&#x27;</span></span></span></td></tr>
<tr><td class="name">fullDefinition</td><td class="desc"><span class="type">boolean</span>Set to true if selectQuery is the entire view definition. False if the CREATE VIEW header should be added<span class="right"><span class="since">@ v3.3</span></span></td></tr>
<tr><td class="name">path</td><td class="desc">Path to file containing view definition<span class="right"><span class="since">@ v3.6</span><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span></td></tr>
<tr><td class="name">relativeToChangelogFile</td><td class="desc"><span class="type">boolean</span>Whether the file path is relative to the root changelog file rather than to the classpath.<span class="right"></span></td></tr>
<tr><td class="name">remarks</td><td class="desc">Comments stored for the view<span class="right"><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span></td></tr>
<tr><td class="name">replaceIfExists</td><td class="desc"><span class="type">boolean</span>Use 'create or replace' syntax<span class="support"><b>Supported by: </b>db2, firebird, h2, hsqldb, ingres, mariadb, mssql, mysql, oracle, postgresql, sqlite, sybase</span><span class="right"><span class="since">@ v1.5</span></span></td></tr>
<tr><td class="name">schemaName</td><td class="desc">Name of the schema<span class="right"><span class="sample">E.g. <span class="val">&#x27;public&#x27;</span></span></span></td></tr>
<tr><td class="name">[XML: text content] / selectQuery</td><td class="desc">SQL for generating the view<span class="right"><span class="sample">E.g. <span class="val">&#x27;select id, name from person where id &gt; 10&#x27;</span></span></span><span class="right"><b>Required for: </b>informix</span><span class="right"><b>Note:</b> <i></i> the content of the tag in XML</span></td></tr>
<tr><td class="name" required>viewName</td><td class="desc">Name of the view to create<span class="right"><span class="sample">E.g. <span class="val">&#x27;v_person&#x27;</span></span></span></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs" id="createView-example">
    <createView catalogName="cat"
            encoding="A String"
            fullDefinition="true"
            path="A String"
            relativeToChangelogFile="true"
            remarks="A String"
            replaceIfExists="false"
            schemaName="public"
            viewName="v_person">select id, name from person where id > 10</createView>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: createView-example
  author: liquibase-docs
  changes:
  - createView:
      catalogName: cat
      encoding: A String
      fullDefinition: true
      path: A String
      relativeToChangelogFile: true
      remarks: A String
      replaceIfExists: false
      schemaName: public
      selectQuery: select id, name from person where id > 10
      viewName: v_person

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "createView-example",
    "author": "liquibase-docs",
    "changes": [
      {
        "createView": {
          "catalogName": "cat",
          "encoding": "A String",
          "fullDefinition": true,
          "path": "A String",
          "relativeToChangelogFile": true,
          "remarks": "A String",
          "replaceIfExists": false,
          "schemaName": "public",
          "selectQuery": "select id, name from person where id > 10",
          "viewName": "v_person"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}
CREATE VIEW cat.v_person AS select id,
 name from person where id > 10;


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2/LUW</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>DB2/z</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Derby</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Firebird</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>H2</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>HyperSQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>INGRES</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Informix</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>MariaDB</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>MySQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>PostgreSQL</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SQLite</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
</table>
