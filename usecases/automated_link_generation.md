## Use case : automated link generation

A maintainer of a pod instructs an automation agent to update artefacts with relevant
backlinks as soon as they appear in the network.

Actors:
  - The maintainer of a pod `M`
  - An automation agent working on behalf of the maintainer `AA(M)` 
  - A pod `Pod(A)` that contains an artefact `URL-A` (e.g. a dataset)
  - Service Hubs : `H1, H2, ... HN`
 
 Resources:
   - Artefact : `URL-A`
   - Event Log for URL-A  : `Evt(URL-A)`

## User story

A maintainer `M` downloads an app `AA(M)` that can understand artefact format XYZ and update it
with new information. The application watches events logs for relevant artefacts and
updates it with information newly added network resources that we made available to the pod
on top of the stored artefacts.

E.g.

- An app that knows IIIF could automatically add annotations to an annotation layer database
when they are discovered in the Event log.
- An app that knows HTML can create back links to published versions , cited references into local pod artefacts
- An app that know signatures can add digital signatures to a joint local pod artefact

## Possible consequences

In this way there can be a decoupling of services relevant for maintaining (and proving) event logs (the orchestrator) and
making sense of the inboxes, and application that provide Pod services on top of the event logs.

### Relevant for
 - Cultural heritage: increasing interconnectedness of the cultural heritage collection data