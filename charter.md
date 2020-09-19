# Charter proposal for an ASDF WG

- Name: A Semantic Definition Format for Data and Interactions of Things (ASDF)
- Revision: 0.1.0

## Background

  Data and interaction models of IoT devices today exhibit unneeded
  diversity between different industry ecosystem standards development
  organizations (SDOs), hindering interoperability across these
  ecosystems with little discernible benefit from the diversity.
  Early 2019, [One Data Model (OneDM)][2] was started to bring several
  IoT SDOs and IoT device and platform vendors together under a broad,
  multi-party liaison agreement, with a goal of arriving at a common
  set of data and interaction models that describe IoT
  devices. Ideally, for every class of IoT device, there is just a
  single model selected/created by the participating organizations,
  which everyone can adopt.

  As a common language for writing down these models, the Semantic
  Definition Format (SDF) was created, which can represent IoT Things,
  their composition from reusable Objects, their Interaction
  Affordances (Properties, Actions, Events), and the data models
  relevant to describe these Affordances.  SDF is representing these
  models in JSON, enabling re-use of specification formats such as
  CDDL (RFC8610) and the formats proposed at json-schema.org and their
  tooling, for describing both the SDF format itself and the structure
  of the data to be modelled in SDF.

  Some 200 models in SDF format have been contributed by participating
  ecosystems; new models are being submitted continually.  Version 1.0
  of the SDF specification was published on the OneDM github
  repository and as an [Internet-Draft][1].  OneDM is now focusing on
  [consolidating the body of submitted models][3] and developing processes
  for arriving at harmonized models that span different industry
  ecosystems in a common way; they look towards the IETF for
  developing SDF 1.0 further into a high-quality specification.

  The IETF also defines the YANG data modelling language (RFC 7950).
  YANG has a strong focus on modelling the management interface for network devices,
  using a fairly small set of network management protocols,
  whereas SDF is designed to span (and transitively unify) many existing interaction models already present.
    While data associated with a YANG schema can be serialized to a variety
   of wire formats (e.g., XML, JSON, CBOR, and others), the serialization is
   driven directly by the structure of the data models defined in YANG; there is no separate "protocol binding" step as in the use of SDF.

   Conversely, SDF does not deal directly with serialization at all,
   modelling only the structure and semantics of the data being interchanged, hence leaving data
   serialization (and RPC semantics) to other standards, most likely defined
   by existing IoT SDOs.

## ASDF

  The objective of the ASDF WG is to develop SDF to an IETF-quality
  specification for Thing Interaction and Data Modelling, working with
  experts from OneDM and its contributing organizations.  On the way
  to that specification, further functionality requirements will be
  addressed that emerge in the usage of SDF for model harmonization.

  The ASDF WG will work closely with the CBOR WG, home of the CDDL
  specification.  It will also engage the still active mailing list of
  the dormant JSON WG.  Recent proposals to form an IRTF formal
  description techniques (FDT) Research Group may lead to another
  collaboration partner.  The Thing-to-Thing Research Group (T2TRG)
  and its WISHI program can be instrumental in engaging researchers
  and other SDOs in this space, for instance W3C WoT, which is working
  on Thing Description Templates and related specifications.


[1]: https://www.ietf.org/id/draft-onedm-t2trg-sdf-00.html
[2]: https://onedm.org
[3]: https://onedm.org/faq


## Initial Milestones

There is only one deliverable, the SDF specification.
It is not currently foreseen that this will be split into multiple
documents, but that is also not excluded.
The plan is to evolve the specification in a regular rhythm, with a
new Implementation Draft available about bi-monthly.

* SDF specification ("SDF 1.0"), WG document adopted, September 2020
* SDF specification ("SDF 1.1"), Implementation Draft, November 2020
* SDF specification ("SDF 1.2"), Implementation Draft, February 2020
* (continuing in the rhythm...)
* SDF specification ("SDF 1.n"), PS to IESG, September 2021
