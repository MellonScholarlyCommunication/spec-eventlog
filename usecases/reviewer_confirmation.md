## Use case : reviewer confirmation

An external reviewer has reviewed an artifact on the Data Pod. The owner
of the Data Pod updates the artifact with a new version. The reviewer
needs to be notified in some way to confirm that the previous review 
is still valid for the new version of the artifact.

Source: Jury Theorems of Peer Review, Arvan et al 2022

Actors:

- A reviewer `R`
- A researcher `A` and her Data Pod `Pod(A)`
- An artifact version 1 `URI(A)-v1`
- A revision of the artifact version 2 `URI(A)-v2`
- A review of version 1 `URI(R){URI(A)-v1}`
- A confirmation that the review of version1 is valid for version 2 `URI(R){URI(A)-v2}`
- 
