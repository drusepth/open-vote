# Vote Transparency

- After voting, the voter is assigned a unique hash receipt that is not tied to
  their identity. From that point on, however, they can look up that hash at
  any point in time to see who that specific vote was cast for.
- This lookup allows for public inspection of votes and vote counts, leading
  to confidence that vote counts and values are fair.
- Additionally, being able to look up your own vote later to ensure it hasn't
  changed in value leads to confidence that voter fraud is not occurring (via
  crowd acceptance that each person's vote is properly cast unless reported,
  since it's easy enough to see that a vote hasn't changed).

## Potential Problems

1. Someone claiming their vote has changed (upon looking up their hash) can
   instill doubt in the system if there is no way to prove they voted for a
   particular candidate (the same or different than their hash lookup result).

2. Someone that loses their post-voting hash can not retrieve it if they hear
   about vote fraud and want to double-check their vote, which could lead to
   additional distrust/resentment of the system. ("Why not just use paper?")

   * Might be able to solve this by voters calculating their own hash from
     information given to them that's tied to their identity (see:
     authentication.md) -- which could allow them to recalculate their hash
     later on. Need to ensure this cannot be used to tie the whole process
     together to prove someone voted for something particular, though. Probably
     need some pro-crypto here to handle this.

## Technical implementation

* System for assigning a guaranteed-collision-less hash to users after voting
  TBD.

* System for instilling confidence in voters that their hash is unique and
  not shared with any other candidates who voted the same way TBD. (To ensure
  that looking up "your vote" for Candidate X is its own individual vote,
  rather than potentially a singular vote across multiple people for the same
  candidate.)
