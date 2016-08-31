# Authentication

* Ensuring that a particular digital user maps exactly to a particular citizen
  (that is allowed to vote) is a hard problem to solve.
* Ensuring that a potential vote has not been given away or sold prior to
  voting is an additional, hard problem to solve. 
* Ensuring that a software system is not compromised by malware capable of
  manipulating votes is an additional, hard problem to solve.

## Solutions

### Mapping digital users one-to-one to citizens

* Idea: You mail out postcards to registered voters with their asymmetric
  private key obscured by an opaque scratch-off covering, and a plainly visible
  public key. If the scratch-off is not intact, the voter requests another via
  website form, or shows up in person at an office in the county seat. The
  registration office revokes the key pair for the original card and issues
  another.

  The registration office then sends a list of public keys without any
  identifying information information to the ballot office, who encrypts a
  separate anonymous blockchain key with each public key, and publishes the
  entire list of results paired with the hash of the blockchain key.

  The voter then attempts to decrypt each entry with their private key, and
  then hash the result. When the hash matches, that is the voter's anonymous
  blockchain key. Each voter has to make, at most, a number of attempts equal
  to the number of registered voters in their district before finding their own
  key.

  The ballot office can verify that each blockchain key for that election
  belongs to a registered voter, but cannot say which one. The registration
  office can verify that each registered voter has a blockchain key available
  (by counting), but cannot even tell who bothered to decrypt their key and
  vote with it, much less what anyone in particular voted for.

  * Problems:

    * Obviously, this is a pretty complicated for the average voter. How can we
      ensure EVERY voter is capable of this, AND understands the process (as
      per Judgment of 03 March 2009 - 2 BvC 3/07 Headnote #2?
      (http://www.bundesverfassungsgericht.de/SharedDocs/Entscheidungen/EN/2009/03/cs20090303_2bvc000307en.html)

    * Does this tie their private key to their identity post-voting? (Can the
      government look up who a particular key voted for, and then look up who
      was assigned that key?)

### Ensuring votes came from a _specific_ citizen

* TBD

### Ensuring machines submitting a vote are not affected by malware capable of
    manipulating votes

* TBD
