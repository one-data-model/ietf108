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

## ASDF

  The objective of the ASDF WG is to develop SDF to an IETF-quality
  specification for Thing Interaction and Data Modelling, working with
  experts from OneDM and its contributing organizations.  On the way
  to that specification, further functionality requirements will be
  addressed that emerge in the usage of SDF for model harmonization.

  In the process, some smaller pieces may become usable independently
  from SDF itself and its applications.  JSON Path (similar to, but
  different in scope from JSON Pointer documented in RFC6901) might be
  an example for such a spin-off specification -- it is currently
  defined on a website and would benefit from a more formal definition
  so it can be used in discovery processes involving SDF models.

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
