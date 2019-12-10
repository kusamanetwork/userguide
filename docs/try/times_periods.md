# Kusama time cheat sheet
### Periods of common actions and attributes
*NOTE: Kusama is 4x as fast as Polkadot will be, except for blocktimes where Polkadot will also have 6 second blocktimes.*

- Block: 6 seconds 
- Epoch: 1 hour (600 slots x 6 seconds)
- Session: 1 hour (6 sessions per Era)
- Era: 6 hours (3600 slots x 6 seconds)

A maximum of one block per slot can be in a chain.

### Democracy 

- Voting period: 1 week
    - How long the public can vote on a referendum
- Launch period: 1 week
    - How long the public can select which proposal to hold a referendum on. i.e., Every week, the highest-weighted proposal will be selected to have a referendum.
- Enactment period: 8 days
    - Time it takes for a succssful referendum to be implemented on the network
- Cool-off period: 7 days
- Emergency voting period: 3 hours
    - The voting period after the technical committee expidites voting

### Council

- Term duration: 6 hours
- Voting period (for council seats): 6 hours

### Staking, Validating, and Nominating

- Term duration: 6 hours
    - The time for which a validator is in the set after being elected. Note, this duration can be shortened in the case that a validator misbehaves.
- Term effect
    - The winners of the election begin validating in the second session of the era. They will continue validating through the first session of the next era.
- Nomination period: 6 hours
    - Every 6 hours, a new validator set is elected according to Phragmen's method.
- Bonding duration: 7 days
    - How long until your funds will be transferrable after unbonding
- Slash defer duration: 7 days

### Treasury

- Period between spends: 6 days
