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
