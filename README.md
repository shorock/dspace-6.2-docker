Just a personal quick-and-dirty local version of DSpace 6.2 just to check on some things.

Assuredly not the 'right' way.  But, adequate for our immediate need.

To run:

- docker-compose build
- docker-compose run dspace-build copy-dspace
  - This, actually, is more of the 'ant update' step in usual DSpace
- docker-compose up -d

http://localhost:8080/xmlui

Notably missing - Solr is still restricted to on-the-box