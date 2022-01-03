## Use case : discover unknown artefacts in the network

A webapp is looking for an unknown artefact `URL-B` in the network
and therefore needs to discover actors and data pods that maintain/store those artefacts.

Actors:
  - A webapp `W` 
  - An automation agent working on behalf of the webapp `AA(W)` 
  - Data Pod `Pod(A)` that contains an artefact `URL-A`
  - Data Pod `Pod(B)` that contains an artefact `URL-B`
  - Service Hub  `H1` 
 
 Resources:
   - Artefact : `URL-A`, `URL-B`
   - Event Log hosted by H1 for URL-A  : `Evt(URL-A)`
   - Event Log hosted by Pod(B) for URL-B  : `Evt(URL-B)`

 ### User story

A webapp `W` want to display a list of artefacts, but it doesn't know any. It just knows a Service Hub `H1`.
It instructs `AA(W)` to go and find artefacts starting from `H1`.

The automation agent `AA(W)` discovers all the event logs of `H1`, among which `Evt(URL-A)`. 
It reads the events about `URL-A` and discovers an event that link to `Pod(B)`, because it also seems to know something about `URL-A`.

The automation agent `AA(W)` discovers all the event logs of `Pod(B)`, among which `Evt(URL-B)`. 
It reads the events about `URL-B` and now knows the link to `URL-B`.

### Relevant for
 - Cultural heritage: finding relevant CH object to populate you portal application with
