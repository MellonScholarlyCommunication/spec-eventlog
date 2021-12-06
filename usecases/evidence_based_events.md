## Use case : evidence based events

A (human) agent discovers a list of network events that happened on top of an artefact and need a
proof these events are valid.

Actors:
  - A human agent (user) on the web `X`
  - A webapp `W` 
  - A pod `Pod(A)` that contains an artefact `URL-A` (e.g. an article)
  - Service Hubs : `H1, H2, ... HN`
 
 Resources:
   - Artefact : `URL-A`
   - Event Log for URL-A  : `Evt(URL-A)`

### User story

User `X` discovers an `URL-A` for an article. Via her webapp `W` she want to 
learn more about it. 

The `W` discovers an event :

- Article `URL-A` was granted an official status by `H3`.

Alas the details of this status are not availble to `X` because the information is not
public shared (e.g. behind a paywall, or closed network).

Allthough the information about the event itself is not accessible to `X` a proof/evidence
can be discoverd from the network.

### Possible implementation

The lifecycle event log contains a signed copy of an event as `H3`. The webapp `W`
can proof `H3` really granted an official status , but doesn't require access to all details.