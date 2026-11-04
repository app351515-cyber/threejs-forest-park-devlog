# Failures, reversions, and lessons

Unsuccessful experiments are a central part of the record.

## 1 — More lighting effects did not always improve the scene

PCSS, SSGI and wind-related normal adjustment were tested, but the visual benefit and rendering cost did not justify retaining them in the normal configuration. Sunlight balance and materials mattered more than enabling everything.

## 2 — An impressive experiment may test the wrong thing

Early God Rays experiments sometimes changed the presentation scene or introduced artificial occluders to emphasize the effect. The useful question was whether they improved the **original forest/waterside scene** without altering it for the sake of a demo.

## 3 — A CPU cache caused regressions

One proposed cache introduced more management overhead than the work it saved; the recorded comparison was slower. Moving calculations into a cache is not necessarily a performance gain.

## 4 — Triangle count and draw calls are different costs

One leaf LOD experiment reduced triangles but increased draw calls. Geometry count, CPU submission, and observed frame time all matter.

## 5 — Distant trees must still look like trees

Aggressive distant proxies could reduce cost while damaging crown silhouettes and perceived density. LOD must preserve the appearance that matters at its viewing distance.

## 6 — A larger world was not automatically fast

Expansion to a 1 km layout was a successful world-building process, but foliage and shadows remained expensive. The laptop's archived 1080p/high-quality measurements do not establish 60 fps gameplay throughout the large world.

## 7 — Natural trails need irregularity

Uniformly clearing plants from paths made the ground look unnaturally sculpted. Later changes restored selected grasses and scattered rocks.

**Rule of thumb:** test in one area → observe the actual scene → measure → keep only justified changes → expand.
