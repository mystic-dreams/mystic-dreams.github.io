# Skills

## Types

### Attacks

#### Basic

Non-MP consuming, single target skill. Deals 100% damage.

#### Single target

Targets the closest enemy, with multiple hits.

#### Multiple target

Targets multiple enemies around, with either a high damage single hit or multiple small damage hits.

** The MP cost for a multi-target attack should cost more than the equivalent of using a single target attack on all the enemies. This is to discourage spamming of multiple target skills only.

### Utility

#### Movement

Teleport is the primary movement skill.

#### Regeneration

Heal user's HP

** This can come in the form of life steal as well.

### Passives

- Max MP increase
- Max MP increase
- MP regeneration rate increase
- Crit Rate increase
- MP leech

** There will not be buff skills. We will always cast buffs skills. Since buffs will always be active, we can simplify this to make it passive instead.

## Design Decisions

### Cooldowns

Skills will not have cooldowns. The amount of skills castable is already controlled by the MP. However, this implies that the MP cost of the attack skills must outweigh the MP recovery rate to ensure skills cannot be spammed. Should the player prep a lot of MP potions, so be it. They deserve it.

### Code Structure

Due to the diverse range of effects of each skill, each skill entity shall be created individually rather than a template with injected data models. This reduces the complexity of implementation, but will encounter repeated code.