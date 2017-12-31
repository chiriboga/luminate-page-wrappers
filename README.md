# luminate-page-wrappers
Collection of very simple Luminate CMS Page Wrappers

Quick Additions to the page

```html
<!-- Begin Luminate Meta Tags: Title, Description, Keywords-->
<title><t:value id="title">title</t:value></title>
<t:if test="isNull(description)">
    <meta name="Description" content="Default Description if NONE is set on the page in LCMS" />
</t:if>
<t:else>
    <t:set id="mydesc" value="toText(description, '') " />
    <t:set id="mydesc" value="escapeQuotes(mydesc) " />
    <t:set id="mydesc" value="replace(mydesc,'\\\'','&#39;')" />
    <t:set id="mydesc" value='replace(mydesc,"\\\"","&quot;")' />
    <meta name="Description" content="${mydesc}" />
</t:else>
<t:value id="meta.keywords">meta.keywords</t:value>
<t:value id="meta.description">meta.description</t:value>
```

This code will show different links if the user is logged in or not
```html
<!-- Deal with the user being Logged in or not -->
<t:if test="crm('[[S1:user_name]]') == ''">
  User IS LOGGED IN
</t:if>
<t:else>
  user is NOT logged in
</t:else>
```


## Twitter Bootstrap 3
While taking into account that other factors may have an impact on how this functions, Here is a very basic example of Twitter Bootstrap 3 and Luminate CMS.

Check out - **bootstrap3.html**

