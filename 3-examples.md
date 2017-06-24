# Examples

   All the examples provided in the following section are hypothetical
   examples.  Real world naming schemes will most likely look different.

   Using the MRN identifier scheme a vessel with an IMO number of 9743368 could be identified as
   follows:

   >  urn:mrn:imo:imo-number:9743368

   The governing organization of how to assign IMO numbers is the
   International Maritime Organization (IMO).  IMO may have delegated
   the actual assignment of numbers to another organization.  But IMO is
   still the organization who has determined that an IMO number is an
   unique seven-digit number. Within the context of maritime resource names the organizational id
   (OID) refers to the organization who governs the syntax and rules of
   a particular resource type.  In the above case the organizational ID
   is "imo".

   Each organization further divides the organizational specific string
   (OSS), which is the part following "imo", into two parts.  An
   organizational specific namespace ID (OSNID) which is a unique
   identifier within the governing organization for a particular type of
   resource. In this example, we have used "imo-number" but it could
   just as well have been "imonumber" or just "number".

   The second part is the organizational specific namespace string
   (OSNS).  Which is the only part that differs for resources of the
   same type, in this case it is "9743368".  The organizational specific
   namespace string is (as the name implies) specific for a combination of a
   OID and OSNID.  In this case the organizational specific namespace
   string is always a 7 digit IMO number.
   
   Another way to identify the same vessel might be to use its MMSI number.
   Here the identifier could look like this:

   > urn:mrn:itu:mmsi:538070999

   In this case ITU is the governing body because MMSI numbers are based
   on recommendation M.585 from ITU.  It might be that national bodies
   does the actual assignment of MMSI numbers, but ITU is the governing
   body for the standardization of MMSI numbers.

   As can be seen from these two examples.  The same vessel can be
   identified by multiple different identifiers.  This is no different
   to a person who might be identified either by his driver license
   number or his social security id.  Multiple identities can identify
   the same entity.  Some parameters frequently used for identification,
   such as 'names of people', do most of the time qualify as
   identifiers, as they are not guaranteed to be unique.  A single
   identifier must refer to one and only one identity.

   The concept of URNs can be taken from a very coarse grained level to
   a very fine grained level.  For example, a container ship might be
   identified by one of the two previous URL's.  The containers aboard
   the ship might be identified with an URN adapting the ISO 6346
   identifier scheme for container ids.

   > urn:mrn:bic:container-id:csqu3054383

   Finally, individual items in a single container might be identified
   by another URN scheme.  It might even be possible to integrate with
   URNs defined outside of the urn:mrn namespace.  For example, all
   items in a container might be identified by an electronic product
   code ([@!RFC5134]).  In other words, the usage of URNs as identifiers
   are not limited to those defined within this document.  In the future
   other non-maritime sectors might even adopt similar naming schemes
   based on URNs to facilitate easier integration across sector
   boundaries.

   An identifier does not need to be a physical object, but can be a
   virtual item such as an electronic document.  For example, IMO might
   decide that all of their documents would use a "publications" prefix.
   So
    
   > urn:mrn:imo:publications:if110s
    
   would refer to the publication "IMO SOLAS Consolidated Spanish
   Edition, 2014 IF110S"

   On the other hand an organization such as IALA might decide that all
   of their publications would follow another format where the category
   of the publication is included in the identifier.  For example, a
   recommendation could be
   
   > urn:mrn:iala:publications:recommendation:e-nav-140 

   while the identifier of a guideline might be written as

   > urn:mrn:iala:publications:guideline:synchronisation-of-lights-1069

   As can be seen from the previous example the Organizational specific
   namespace string can be split into multiple hierarchies.  It is all
   up to the governing organization how they want to structure their
   identifiers.

   Another example of identifiers with multiple hierarchies could be an
   identifier scheme for lights and buoys.  Here IALA could choose to
   let the OSNS consist of \<CountryCode\>:\<National Identifier\>.  For
   example
   
   > urn:mrn:iala:aton:us:1234x5

   There are no requirements that organizations are permanent entities.
   For example, the European STM Validation project could choose to use
   "stm" as their organizational id.  So, for example, a voyage id in
   this project might look like
   
   > urn:mrn:stm:voyage:id:xcus231230 
   
   Internally in the project they can use xcus231230 to refer to a
   voyage plan.  But when working with external systems or other
   projects the full URN can be used in case other projects uses another
   type of identifier for a particular voyage.

   As can be seen from all these examples.  The scheme is highly
   adaptable.  Each organization can choose their own layout for a
   specific type of identifiers.  It is easy to fit existing identifiers
   into the naming scheme.  And it provides good context information
   about the type of the identifier in comparison to something simple
   like a random UUID.