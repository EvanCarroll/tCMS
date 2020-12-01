tCMS
=====

A flexible perl CMS which supports multiple data models and content types

Deployment is currently:
* Set up proxy rule in your webserver
* open tmux or screen
* `starman -p $PORT www/server.psgi`

In the future, we'll make systemd service files and rpms/debs etc.

The user guide is self-hosted; After you first login, hit the 'Manual' section in the backend.

Content Types
=============
* Microblogs
* Blogs
* Video
* Audio
* Files
* About Pages

Planned development:
* Presentations
* Test Plans / Issues (crossover with App::Prove::Elasticsearch)

Data Models
===========
* DUMMY - A JSON blob.  Used for testing mostly, but could be handy for very small sites.
* Flat File - Pretty much the tCMS1 data model; a migration script is forthcoming

Planned Development:
* Elasticsearch - Documents are ideally indexed in a search engine, should be nice and fast too.
* Git - More for the APE crossover

Ideas to come:
=============

*domain* picker at top -- manage all your web properties from one place

login and registration (forces email for a domain to allow posting on said domain)
User data *also* stored in ES -- it's their profile page!

Error and Access logs immediately dumped into ES for EZ viewing in grafana

Automatic analytics!

Multiple auth models (ldap, oauth etc)

Builtin paywall -- add in LDAP users not on primary domain, give differing privs
Have all content able to assign to paywall packages

One click share to social via oauth
Mailing list blasts for paywall content
