---
layout: default
title: Docs | Change 'renameColumn'
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'renameColumn'

Renames an existing column

## Available Attributes ##

<table class='attribs'>
<tr><th>Name</th><th>Description</th></tr>
<tr><td class="name">catalogName</td><td class="desc">Name of the catalog<span class="right"><span class="since">@ v3.0</span><span class="sample">E.g. <span class="val">&#x27;cat&#x27;</span></span></span></td></tr>
<tr><td class="name">columnDataType</td><td class="desc">Data type of the column<span class="right"><span class="sample">E.g. <span class="val">&#x27;int&#x27;</span></span></span><span class="right"><b>Required for: </b>mariadb, mysql</span></td></tr>
<tr><td class="name" required>newColumnName</td><td class="desc">Name to rename the column to<span class="right"><span class="sample">E.g. <span class="val">&#x27;full_name&#x27;</span></span></span></td></tr>
<tr><td class="name" required>oldColumnName</td><td class="desc">Name of the existing column to rename<span class="right"><span class="sample">E.g. <span class="val">&#x27;name&#x27;</span></span></span></td></tr>
<tr><td class="name">remarks</td><td class="desc">Remarks of the column<span class="right"><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span></td></tr>
<tr><td class="name">schemaName</td><td class="desc">Name of the schema<span class="right"><span class="sample">E.g. <span class="val">&#x27;public&#x27;</span></span></span></td></tr>
<tr><td class="name" required>tableName</td><td class="desc">Name of the table containing that the column to rename<span class="right"><span class="sample">E.g. <span class="val">&#x27;person&#x27;</span></span></span></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs" id="renameColumn-example">
    <renameColumn catalogName="cat"
            columnDataType="int"
            newColumnName="full_name"
            oldColumnName="name"
            remarks="A String"
            schemaName="public"
            tableName="person"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: renameColumn-example
  author: liquibase-docs
  changes:
  - renameColumn:
      catalogName: cat
      columnDataType: int
      newColumnName: full_name
      oldColumnName: name
      remarks: A String
      schemaName: public
      tableName: person

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "renameColumn-example",
    "author": "liquibase-docs",
    "changes": [
      {
        "renameColumn": {
          "catalogName": "cat",
          "columnDataType": "int",
          "newColumnName": "full_name",
          "oldColumnName": "name",
          "remarks": "A String",
          "schemaName": "public",
          "tableName": "person"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (MySQL)

{% highlight sql %}
ALTER TABLE cat.person CHANGE name full_name INT COMMENT 'A String';


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
<tr><td>SQLite</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Sybase</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Sybase Anywhere</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
</table>
