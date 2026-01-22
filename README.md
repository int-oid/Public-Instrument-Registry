```
INSTRUMENT OF THE INTERNATIONAL ORGANIZATION FOR IDENTITY DOCUMENTS  
ON THE ESTABLISHMENT OF THE PUBLIC INSTRUMENT REGISTRY  

PREAMBLE  
THE SECRETARIAT OF THE INTERNATIONAL ORGANIZATION FOR IDENTITY DOCUMENTS (OIDI),  
RECOGNISING the imperative for transparent, machine-actionable legal instruments governing the operations of the Organization;  
NOTING the need for unambiguous identification, citation, and relationship tracking across all instruments issued by the Organization;  
HEREBY ADOPTS this binding Framework for the Public Instrument Registry maintained by the Office of Legal Affairs.  

CHAPTER 1  
GENERAL PROVISIONS  

Article 1  
Definitions  

1. For the purposes of this Framework:  
   a. "Instrument" means any legally operative text issued by OIDI organs;  
   b. "IOID ID" means the unique alphanumeric identifier assigned under Article 4;  
   c. "Official Journal" means the publication series defined in Article 6;  
   d. "Sector" refers to the classification system in Article 3;  
   e. "Citation Prefix" denotes the journal-sector code combination specified in Article 14;  
   f. "Registry" means the Public Instrument Registry maintained by the Office of Legal Affairs.  

Article 2  
Scope of Application  

1. This Framework applies to all instruments adopted by OIDI organs after 1 February 2026.
2. Instruments predating this Framework shall be retrofitted with IOID IDs by the Office of Legal Affairs by 31 December 2026.  

CHAPTER 2  
CLASSIFICATION SYSTEM  

Article 3  
Sector Classification  

1. Instruments shall be classified into exactly one sector according to the table in paragraph 2.  
2. Sector definitions:  
   a. Code 0 - Consolidated Acts: Codified texts integrating all amendments to base instruments;  
   b. Code 1 - Constitutional: Founding charters, core principles, and constitutional amendments;  
   c. Code 2 - External Relations: Treaties, agreements, and memoranda of understanding;  
   d. Code 3 - Institutional: Statutes of offices, committees, and organizational bodies;  
   e. Code 4 - Legislation: Binding general rules applicable to categories of addressees;  
   f. Code 5 - Administrative: Specific decisions, mandates, appointments, and internal acts;  
   g. Code 6 - Assets and Intellectual Property: Licenses, copyright/trademark authorizations, branding rules;  
   h. Code 7 - Jurisprudence: Rulings, dispute resolutions, and advisory opinions;  
   i. Code 8 - Technical: Standards, specifications, schemas, and interoperability protocols;  
   j. Code 9 - Preparatory: Drafts, proposals, consultation papers, and non-binding initiatives.  
3. Sector assignment is final upon adoption and may not be altered thereafter.  

Article 4  
Identifier System  

1. Every instrument shall be assigned a permanent, immutable IOID ID in the format [S][YYYY][T][SSSSSS] where:  
   a. S = Sector code (one digit, per Article 3);  
   b. YYYY = Calendar year of adoption (four digits);  
   c. T = Type code (one uppercase letter from {A-H, J, K, M, N, P-T, V-Z});  
   d. SSSSSS = Six-character sequence (alphanumeric, excluding I, L, O, U).  
2. Overflow Mechanism:  
   a. Should the sequence space for a (Sector, Year, Type) triplet be exhausted:  
      i. The identifier length extends to 13 characters by appending an extension digit E (0-9);  
      ii. E increments only after SSSSSS reaches ZZZZZZ;  
      iii. Systems shall accept both 12- and 13-character identifiers.  
3. Examples:  
   a. 82026TK3M2AB: Sector 8 (Technical), 2026, Standard-type, sequence K3M2AB;  
   b. 42027RZZZZZZ1: Sector 4 (Legislation), 2027, Regulation-type, sequence ZZZZZZ, extension 1.  

Article 5  
Instrument Types and Legal Force  

1. Instruments shall bear exactly one type code with corresponding legal effect:  
   a. Code C - Charter: Constitutional supremacy; Mandatory Publication: Yes (Journal L);  
   b. Code A - Agreement: Binding on signatory parties; Mandatory Publication: Yes (Journal L);  
   c. Code S - Statute: Binding on OIDI organs/bodies; Mandatory Publication: Yes (Journal L);  
   d. Code R - Regulation: Binding general application; Mandatory Publication: Yes (Journal L);  
   e. Code D - Decision: Binding on specific addressees; Mandatory Publication: Conditional (Article 7);  
   f. Code M - Mandate: Administrative authority; Mandatory Publication: Yes (Journal C);  
   g. Code L - License: Contractual obligations; Mandatory Publication: Yes (Journal C);  
   h. Code T - Standard: Recommended or mandatory by reference; Mandatory Publication: Yes (Journal T);  
   i. Code P - Proposal: Non-binding; Mandatory Publication: No;  
   j. Code N - Notice: Informational; Mandatory Publication: Yes (Journal C);  
   k. Code O - Opinion: Non-binding interpretive guidance; Mandatory Publication: Yes (Journal C).  
2. Legal force is void without publication in the Official Journal per Article 7.  

CHAPTER 3  
PUBLICATION AND LEGAL EFFECT  

Article 6  
Official Journal Series  

1. Three publication series are established:  
   a. Series L: Binding instruments of general application; Access Requirement: Mandatory public search;  
   b. Series C: Administrative and informational instruments; Access Requirement: Mandatory public search;  
   c. Series T: Technical specifications and interoperability protocols; Access Requirement: Priority access for implementers.  
2. Publication constitutes formal promulgation. Entry into force occurs 20 days post-publication unless otherwise specified.  

Article 7  
Publication Requirements  

1. The following instruments must be published to acquire legal effect:  
   a. All instruments of Sectors 1, 2, 3, and 4;  
   b. Standards (Sector 8, Type T) referenced in binding instruments;  
   c. Decisions (Sector 5, Type D) of general application;  
   d. All instruments in Journal series L and T.  
2. Preparatory instruments (Sector 9) may be published for transparency but carry no legal force.  

CHAPTER 4  
REGISTRY OPERATIONS  

Article 8  
Metadata Schema  

1. Each published instrument shall include machine-readable metadata containing:  
   a. IOID ID, Title, Sector, Type, Journal Series, Status (In Force/Adopted/Drafting/Suspended/Expired/Repealed);  
   b. Adoption Date, Entry-into-Force Date, Expiry/Repeal Date;  
   c. Adopting Authority, Legal Basis, Amendment History, Related Instruments;  
   d. SHA-256 cryptographic hash of authentic text;  
   e. Language versions and full-text index.  
2. Metadata shall be accessible via standardized interfaces and bulk export mechanisms.  

Article 9  
Amendment and Consolidation Protocol  

1. Amendments shall be issued as new instruments with distinct IOID IDs, explicitly referencing the amended instrument.  
2. Consolidated Acts (Sector 0) shall integrate all amendments into a single text while preserving:  
   a. Original IOID IDs of source instruments;  
   b. Complete amendment history via cryptographic hashes;  
   c. Explicit repeal/expiration markers.  
3. Repealed instruments remain publicly accessible with status "Repealed".  

Article 10  
Access and Transparency  

1. All instruments with status "In Force" or "Adopted" shall be publicly accessible without authentication via the Registry.  
2. Draft instruments (Sector 9, status "Drafting") shall be restricted to authorized OIDI personnel.  
3. Programmatic access to the Registry shall be provided via standardized interfaces, including:  
   a. Machine-readable APIs with published specifications;  
   b. Feeds per Journal series in standard syndication formats;  
   c. Daily bulk exports in open data formats.  

Article 11  
Integration Principles  

1. The Registry shall serve as the single authoritative source for all published OIDI instruments.  
2. The Office of Legal Affairs shall establish technical specifications to enable:  
   a. Interoperability with internal systems;  
   b. Synchronization with external repositories through standardized protocols;  
   c. Verification of instrument authenticity and integrity.  
3. Such specifications shall be published as Standards (Type T) in the Registry.  

Article 12  
Identifier Assignment Protocol  

1. The Office of Legal Affairs shall assign IOID IDs according to:  
   a. Sector: Determined by primary subject matter;  
   b. Year: Calendar year of adoption;  
   c. Type: Legal nature per Article 5;  
   d. Sequence: Sequential allocation within each (Sector, Year, Type) triplet.  
2. The sequence space (32^6 combinations per triplet) shall be monitored; overflow triggers Article 4(2).  

Article 13  
Lifecycle Management  

1. Instrument lifecycle stages:  
   a. Drafting: Internal authoring (Sector 9, status "Drafting");  
   b. Consultation: Stakeholder review (metadata field "Consultation Period");  
   c. Adoption: Formal approval by competent organ (status "Adopted");  
   d. Publication: Assignment to Journal series and inclusion in the Registry (status updated per timeline);  
   e. Archiving: Status "Repealed"/"Expired" with preserved metadata in the Registry.  
2. Corrections shall be issued exclusively via corrigenda instruments--never by modifying original texts in the Registry.  

Article 14  
Citation Standard  

1. Human-readable citations shall follow the format [Type Name] [Citation Prefix][Sequence]/[Year] where:  
   a. Citation Prefix = Journal series code (L/C/T) + Sector code (0-9), derived per Table 1;  
   b. Sequence = First six characters of the sequence field in the IOID ID.  
2. Table 1: Citation Prefix Derivation  
   a. Sectors 0,1,4 with Journal L: Prefixes L0, L1, L4;  
   b. Sectors 2,3 with Journal L: Prefixes L2, L3;  
   c. Sectors 5,7 with Journal C: Prefixes C5, C7;  
   d. Sector 6 with Journal C: Prefix C6;  
   e. Sector 8 with Journal T: Prefix T8;  
   f. Sector 9: Not applicable.  
3. Examples:  
   a. IOID ID 82026TK3M2AB: Technical Standard T8K3M2AB/2026;  
   b. IOID ID 42026RL1B7CD: Regulation L4L1B7CD/2026;  
   c. IOID ID 52025DC9X3Y2: Decision C5C9X3Y2/2025.  
4. Machine reference: The full IOID ID shall be appended in parentheses where precision is required, e.g., "Pursuant to Technical Standard T8K3M2AB/2026 (82026TK3M2AB)".  

Article 15  
System Integrity  

1. Immutability:  
   a. IOID IDs shall never be reused or reassigned;  
   b. Authentic text shall be verified via SHA-256 hash stored in the Registry metadata;  
   c. All amendments shall preserve original instrument integrity.  
2. Archiving:  
   a. Repealed/expired instruments shall remain publicly accessible in the Registry;  
   b. Full version history shall be retained for 50 years post-expiry.  

CHAPTER 5  
FINAL PROVISIONS  

Article 16  
Entry into Force  

1. This Framework enters into force on 1 March 2026.  
2. The Office of Legal Affairs shall publish implementation guidelines for the Registry by 15 February 2026.  

ADOPTED on 23 January 2026  
By the OIDI Secretariat  

PUBLICATION: This instrument is published in the Official Journal as L1C00001A/2026 (12026C00001A).  
STATUS: In Force from 1 February 2026.  
```
