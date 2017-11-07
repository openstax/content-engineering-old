# Services
List of OpenStax services
  - [cnx.org](#cnxorg)
  - [archive.cnx.org](#archivecnxorg)
  - [publishing.cnx.org](#publishingcnxorg)
  - [legacy.cnx.org](#legacycnxorg)
**Note:** You can visit each URL in the list of services, but they don’t all have a homepage. For example: https://archive.cnx.org/contents/9a1df55a-b167-4736-b5ad-15d996704270%403.2 shows the Table of Contents for the Calculus textbook and you can click the links to read a Page in the Book. The current way to do it is to go to cnx.org , navigate to a book, and then change the URL to be `archive.cnx.org` instead of `cnx.org` . There is currently and existing PR regarding this: https://github.com/Connexions/webview/pull/1583 . **Note:** RM This line once it is merged. 
  # cnx.org

  ### Provides

  - the single-page app for reading content (Books and Pages) in a browser.


  ### Repositories
  - [webview](https://github.com/Connexions/webview)

  ### Talks to

  - [archive.cnx.org](#archivecnxorg)
  - [exercises.openstax.org](https://github.com/openstax/exercises)
  - [tutor.openstax.org](https://github.com/openstax/tutor)


  # archive.cnx.org

  This provides **read-only** access to the archive of published content.

  ### Provides

  - retrieving content (Books and Pages)
  - searching for content
  - retrieving metadata about content


  ### Accepts

  - published content (by virtue of being in the Postgres DB)


  ### Repositories

  - [cnx-archive](https://github.com/Connexions/cnx-archive)
    - [cnx-db](https://github.com/Connexions/cnx-db)
    - [cnx-epub](https://github.com/Connexions/cnx-epub)
    - [cnx-query-grammar](https://github.com/Connexions/cnx-query-grammar)
    - [rhaptos.cnxmlutils](https://github.com/Connexions/rhaptos.cnxmlutils)


  # publishing.cnx.org

  This acts as the publishing endpoint. It can either accept a specially-formatted EPUB3 file, or it listens to database changes (when publishing using [legacy.cnx.org](#legacycnxorg)). If a book is marked as needing to be baked, [cnx-easybake](https://github.com/Connexions/cnx-easybake) runs using a CSS file in [cnx-recipes](https://github.com/Connexions/cnx-recipes)

  ### Requires
  - [cnx-publishing](https://github.com/Connexions/cnx-publishing)
    - [cnx-archive](https://github.com/Connexions/cnx-archive)
    - [cnx-epub](https://github.com/Connexions/cnx-epub)
    - [cnx-easybake](https://github.com/Connexions/cnx-easybake)
    - [cnx-recipes](https://github.com/Connexions/cnx-recipes)

  ### Talks to
  - [archive.cnx.org](#archivecnxorg) using the Postgres DB

  ### Listens to
  - [legacy.cnx.org](#legacycnxorg) publish events using the Postgres DB

  ### Accepts
  - specially formatted epub3 documents for publishing


  # legacy.cnx.org

  This Zope application is how content is edited and published.

  ### Repositories
  - All the ones in the https://github.com/Rhaptos org

  ### Talks to
  - [publishing.cnx.org](#publishingcnxorg) using the Postgres DB when content is published
