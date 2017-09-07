# Compare 2 versions of HTML files


```shell
# Assumes there are 2 XHTML files: col-master.xhtml and col-new.xhtml
xmllint --pretty 2 col-master.xhtml > col-master.pretty.xhtml 
xmllint --pretty 2 col-new.xhtml    > col-new.pretty.xhtml 
diff col-master.pretty.xhtml col-new.pretty.xhtml 
```


<details>

<summary>Click me to see example output</summary>

```diff
diff col12074-master.pretty.xhtml col12074-new.pretty.xhtml 
5,9c5
<     ><link
<         rel="stylesheet"
<         href="../css/ccap-university-physics.css"
<         type="text/css"
<     /><title
---
>     ><title
16a13,16
>     /><link
>         rel="stylesheet"
>         type="text/css"
>         href="../../css/ccap-university-physics.css"
22c22
<         id="idm30481946848"
---
>         id="idm544640446160"
73c73
<               id="idm30482357104"
---
>               id="idm544639412288"
75c75
<                 id="idm30482357104"
---
>                 id="idm544639412288"
87c87
<             >PDF Generated: 2017/08/18 09:21:45</div
---
>             >PDF Generated: 2017/09/07 10:51:41</div
298c298
<                 href="#idm30481999856"
---
>                 href="#idm544640165920"
314c314
<                     href="#idm30482292144"
---
>                     href="#idm544640130480"
```

</details>


# List versions of installed packages

```shell
qa00$ for f in /var/cnx/venvs/*/src/*/; do echo $f; cd $f && git log -1 --oneline && cd; done
```

<details>
<summary>Click me to see example output</summary>

```
/var/cnx/venvs/archive/src/cnx-archive/
6f37cf1 fix setup.py to see templates folder (#513)
/var/cnx/venvs/archive/src/cnx-db/
66c203a Fix typo in migration update_latest_trigger
/var/cnx/venvs/archive/src/cnx-epub/
b95c334 Merge pull request #126 from Connexions/fix-sanitize-xml
/var/cnx/venvs/archive/src/cnx-query-grammar/
8484d2c Bump version
/var/cnx/venvs/archive/src/rhaptos.cnxmlutils/
9ec4b5f Merge pull request #160 from Connexions/fix-windows-characters
/var/cnx/venvs/authoring/src/cnx-authoring/
602c066 Merge pull request #247 from Connexions/use-codecov
/var/cnx/venvs/authoring/src/cnx-epub/
b95c334 Merge pull request #126 from Connexions/fix-sanitize-xml
/var/cnx/venvs/authoring/src/cnx-query-grammar/
8484d2c Bump version
/var/cnx/venvs/authoring/src/openstax-accounts/
f96049d Merge pull request #24 from Connexions/unittest-skipping
/var/cnx/venvs/publishing/src/cnx-archive/
6f37cf1 fix setup.py to see templates folder (#513)
/var/cnx/venvs/publishing/src/cnx-db/
66c203a Fix typo in migration update_latest_trigger
/var/cnx/venvs/publishing/src/cnx-easybake/
24b4d70 Support Namespaces (#72)
/var/cnx/venvs/publishing/src/cnx-epub/
b95c334 Merge pull request #126 from Connexions/fix-sanitize-xml
/var/cnx/venvs/publishing/src/cnx-publishing/
8def828 reword some log messages - add one when task picked up from queue (#174)
/var/cnx/venvs/publishing/src/cnx-query-grammar/
8484d2c Bump version
/var/cnx/venvs/publishing/src/cssselect2/
560b4c4 Merge pull request #6 from Connexions/selector-source-line
/var/cnx/venvs/publishing/src/openstax-accounts/
f96049d Merge pull request #24 from Connexions/unittest-skipping
/var/cnx/venvs/publishing/src/rhaptos.cnxmlutils/
9ec4b5f Merge pull request #160 from Connexions/fix-windows-characters
```

</details>
