## Use case : discover lifecycle events for an artefact

A (human) agent discovers an artefact URL-A an requires information about which (scholarly) services
in the world added service event on top of this record and can learn more about these events.

Actors:
  - A human agent (user) on the web `X`
  - A (scholarly) webapp `W` 
  - A pod `Pod(A)` that contains an artefact `URL-A`
  - Service Hubs : `H1, H2, ... HN`
 
 Resources:
   - Artefact : `URL-A`
   - Event Log for URL-A  : `Evt(URL-A)`

 ### User story

A user `X` discovers by some mechanism an artefact `URL-A` on the Web and wants to learn more about it.
User `X` browser is equipped with an webapp/plugin `W` that can retrieve relevant contextual information
about this artefact. 

The user `X` instructs her webapp/plugin to search who in the network provides services in her field of
interest (academia, erfgoed, press, ...)

The webapp/plugin `W` discovers a list of services that provides extra values on top of the artefact.
The app can list these service events in a chronological or customized order (e.g. user `X` is know to have 
a preference of what services interests her). 

The service events allows user `X` to judge the relevance of the artefact `URL-A` and learn more about the
details.

### Relevant for
 - Cultural heritage: knowing what happened to (the metadata of) an object, eg. where it has been preserved, digitized or whether it has been 'on a loan' in a different institution.