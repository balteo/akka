# mergeLatest

Merge multiple sources.

@ref[Fan-in stages](../index.md#fan-in-stages)

## Signature

## Description

MergeLatest joins elements from N input streams into stream of lists of size N.
i-th element in list is the latest emitted element from i-th input stream.
MergeLatest emits list for each element emitted from some input stream,
but only after each input stream emitted at least one element


@@@div { .callout }

**emits** when element is available from some input and each input emits at least one element from stream start

**completes** all upstreams complete (eagerClose=false) or one upstream completes (eagerClose=true)
@@@
