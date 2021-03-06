---
layout: default
title: Docs | Change 'createSynonym'
---

<!-- ====================================================== -->
<!-- GENERATED BY ChangeDocGenerator DO NOT MODIFY MANUALLY -->
<!-- ====================================================== -->

  <script>
  $(function() {
    $( "#changelog-tabs" ).tabs();
  });
</script>

# Change: 'createSynonym'

Creates a synonym

## Available Attributes ##

<table class='attribs'>
<tr><th>Name</th><th>Description</th></tr>
<tr><td class="name">objectCatalogName</td><td class="desc"><span class="right"></span></td></tr>
<tr><td class="name" required>objectName</td><td class="desc"><span class="right"><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span></td></tr>
<tr><td class="name">objectSchemaName</td><td class="desc"><span class="right"></span></td></tr>
<tr><td class="name">objectType</td><td class="desc"><span class="right"><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span><span class="right"><b>Required for: </b>db2</span></td></tr>
<tr><td class="name">private</td><td class="desc"><span class="type">boolean</span><span class="right"></span></td></tr>
<tr><td class="name">replaceIfExists</td><td class="desc"><span class="type">boolean</span><span class="right"></span></td></tr>
<tr><td class="name">synonymCatalogName</td><td class="desc"><span class="right"></span></td></tr>
<tr><td class="name" required>synonymName</td><td class="desc"><span class="right"><span class="sample">E.g. <span class="val">&#x27;A String&#x27;</span></span></span></td></tr>
<tr><td class="name">synonymSchemaName</td><td class="desc"><span class="right"></span></td></tr>
</table>

<div id='changelog-tabs'>
<ul>
    <li><a href="#tab-xml">XML Sample</a></li>
    <li><a href="#tab-yaml">YAML Sample</a></li>
    <li><a href="#tab-json">JSON Sample</a></li>
  </ul>
<div id='tab-xml'>
{% highlight xml %}
<changeSet author="liquibase-docs" id="createSynonym-example">
    <pro:createSynonym objectName="A String"
            objectType="A String"
            private="true"
            replaceIfExists="false"
            synonymName="A String"/>
</changeSet>
{% endhighlight %}
</div>
<div id='tab-yaml'>
{% highlight yaml %}
changeSet:
  id: createSynonym-example
  author: liquibase-docs
  changes:
  - createSynonym:
      objectName: A String
      objectType: A String
      private: true
      replaceIfExists: false
      synonymName: A String

{% endhighlight %}
</div>
<div id='tab-json'>
{% highlight json %}
{
  "changeSet": {
    "id": "createSynonym-example",
    "author": "liquibase-docs",
    "changes": [
      {
        "createSynonym": {
          "objectName": "A String",
          "objectType": "A String",
          "private": true,
          "replaceIfExists": false,
          "synonymName": "A String"
        }
      }]
    
  }
}

{% endhighlight %}
</div>
</div>


## SQL Generated From Above Sample (SQL Server)

{% highlight sql %}
CREATE SYNONYM [A String] FOR [A String];


{% endhighlight %}

## Database Support

<table style='border:1;'>
<tr><th>Database</th><th>Notes</th><th>Auto Rollback</th></tr>
<tr><td>DB2/LUW</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>DB2/z</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>Derby</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Firebird</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>H2</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>HyperSQL</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>INGRES</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Informix</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>MariaDB</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>MySQL</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Oracle</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>PostgreSQL</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>SQL Server</td><td><b>Supported</b></td><td><b>Yes</b></td></tr>
<tr><td>SQLite</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Sybase</td><td>Not Supported</td><td><b>Yes</b></td></tr>
<tr><td>Sybase Anywhere</td><td>Not Supported</td><td><b>Yes</b></td></tr>
</table>
