# Specification Template

Namespace ID
: <br/>"mrn"

Registration Information
: 
{style="empty"}
 - Registration version number: 1
 - Registration date: 2017-xx-xx

Declared Registrant of the Namespace
: <br/>Registering organization:
{style="empty"}
 - International Association of Lighthouse Authorities (IALA)
 - 10 rue des Gaudines
 - 78100
 - St Germain en Laye
 - France
 - Email: contact@iala-aism.org

<br/>

: <br/>Designated Contact:
{style="empty"}
 - International Association of Lighthouse Authorities (IALA)
 - Email: info@mrnregistry.org
 - http://www.mrnregistry.org/


Declaration of structure:

      The Namespace Specific String (NSS) of all URNs that use the
      "mrn" NID shall have the following structure:

      <URN>   ::= "urn:mrn:" <OID> ":" <OSS>

      <OID>   ::= 1*(ALPHA / DIGIT) ; Organizational ID

      <OSS>   ::= <OSNID> ":" <OSNS> ; Organizational specific string
                
      <OSNID> ::= 1*(ALPHA / DIGIT / "-") 
                  ; Organizational specific namespace ID

      <OSNS>  ::= 1*<URN chars> ; Organizational specific namespace string

      DIGIT   ::= %x30-39 ; 0-9

      ALPHA   ::= %x61-7A ; a-z

      Basics of the ABNF notation used :

       " " literals (terminal character strings); terms not in quotes are
           non-terminals

       /   alternatives

       ()  indicates a sequence group, used as a single alternative or as a
           single repeating group

       <a>*<b>  indicates that the following term or group can repeat at
                least <a> and at most <b> times; default values are 0 and
              infinity, respectively

       ;   comment  
       
       <URN chars>  As defined in [@!RFC2141]                    

Relevant ancillary documentation:
: <br/>  The process for assigning unique organizational IDs is managed by IALA.
         Details and application process can be found at http://www.mrnregistry.org.

Identifier uniqueness considerations:
: <br/>Guaranteeing uniqueness is a two-way process. First, IALA will guarantee that each
       organization will be assigned a unique organizational id that will never be reused.
       Second, each organization must guarantee that they do not assign identical organizational
       specific strings (OSS).
   

Identifier persistence considerations:
: <br/>Each individual organization must guarantee that assigned URNs will 
       not be reused and will remain valid beyond the lifecycle of the referenced 
       resources. However, it should be noted that although the URNs remain valid, 
       the status of the referenced resource may change.

Process of identifier assignment:
: <br/>While the assignment of OIDs for each organization is managed by IALA. 
       The assignment of organization specific namespace ids and strings are fully 
       managed by each individual organization. 

Process of identifier resolution:
: <br/>  There are no plans to provide a general available resolution mechanism.
         However, organizations are free to setup resolution servers for
         all or part of the URNs assigned under their organizational id.

Rules for Lexical Equivalence:
: <br/>  The entire URN is case insensitive.


Conformity with URN syntax:
: <br/>  There are no additional characters reserved except as noted in
         the ABNF above.

Validation mechanism:
: <br/>  In the case of each sub-namespace, there will be namespace-
         specific rules for determining validity. There are no plans to
         provide a central repository for these rules.

Scope:
: <br/>Global.