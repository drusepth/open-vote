# Vote Transparency

- After voting, the voter is assigned a unique hash receipt that is not tied to
  their identity. From that point on, however, they can look up that hash at
  any point in time to see who the vote was cast for.
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

## Technical implementation

* System for assigning a collision-less hash to users after voting TBD

* System for instilling confidence in voters that their hash is unique and
  not shared with any other candidates who voted the same way TBD.
