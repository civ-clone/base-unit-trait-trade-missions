# base-unit-trait-trade-missions

The `TradeMissions` unit trait: a unit type with it can carry out trade missions.

A unit type with this trait can establish a trade route with a city, or help build a wonder in one.

For example: Civ1: Caravan. Civ2: Caravan and Freight.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(TradeMissions)`:

```ts
import TradeMissions from '@civ-clone/base-unit-trait-trade-missions/TradeMissions';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, TradeMissions));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
