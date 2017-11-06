- Conversions
  - [PDF Generation](#pdf-generation)
  - [CNXML to XHTML](#cnxml-to-xhtml)
  - [CNXML validation](#cnxml-validation)
  - [XHTML validation](#xhtml-validation)

  # CNXML to XHTML

  There are 4 different CNXML is converted to XHTML:

  - `CNXML -> Raw XHTML`: This is the XHTML on [cnx.org](#cnxorg) and uses XSLT files in [rhaptos.cnxmlutils](https://github.com/Connexions/rhaptos.cnxmlutils)
  - `CNXML -> Raw XHTML -> Baked XHTML`: This is the XHTML on [cnx.org](#cnx-org) and uses a special CSS file associated with the Book (source in [cnx-recipes](https://github.com/Connexions/cnx-recipes) ) and the Raw XHTML files and converts them using the CSS file and the CSS engine in [cnx-easybake](https://github.com/Connexions/cnx-easybake)
  - `CNXML -> Docbook -> PDF XHTML`: This is the format for PDF Generation. It uses Docbook-XSL files in [oer.exports](https://github.com/Connexions/oer.exports). It is being **deprecated** in favor of the _Baked XHTML_
  - `CNXML -> Legacy XHTML`: This is the XHTML on [legacy.cnx.org](#legacycnxorg). It uses a custom XSLT file somewhere. This conversion is being **deprecated** in favor of the _Raw or Baked XHTML_.


  # CNXML Validation

  This is described as a Relax-NG file in [cnxml](https://github.com/Connexions/cnxml).

  # XHTML Validation

  This is described as a Relax-NG file in [cnxml](https://github.com/Connexions/cnxml).
