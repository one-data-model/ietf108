==== ASDF (proposal) ====

- Name: A Semantic Definition Format for Data and Interactions of Things (ASDF)
- Description:

  In a 2018 event about IoT futures hosted by ZigBee, by far the most
  frequently cited challenge was the inconsistency and lack of
  interoperability across the field of IoT data models; specifically
  the lack of a common data model.

  Based on this observation, One Data Model (OneDM) was started in
  early 2019, bringing several IoT SDOs (Standards Development
  Organizations) and IoT device and platform vendors together under a
  broad, multi-party liaison agreement.

  The goal of OneDM is to arrive at a common set of data and
  interaction models that describe IoT devices. This will enable an
  application to work with IoT devices from different ecosystems,
  without a need for converting data and interactions from the model
  of one organization to that of the other. Ideally, for every class
  of IoT device, there is just a single model selected/created by the
  participating organisations, which everyone can adopt.

  The first step towards this goal was to have a common way how to
  write down a model. Since all participating organizations are
  currently doing this in their own ways, it made sense to develop a
  single way to describe models.  Over a little more than a year, the
  Semantic Definition Format (SDF) was created, which can represent
  IoT Things, their composition from reusable Objects, their
  Interaction Affordances (Properties, Actions, Events), and the data
  models relevant to describe these Affordances.  SDF is representing
  these models in JSON.  This allows re-use of specification formats
  such as CDDL (RFC8610) and the formats proposed at json-schema.org
  for both the description of the SDF format itself and the structure
  of the data to be modelled in SDF.  Abundant tools and libraries are
  available to produce/consume JSON, so tooling to work with SDF
  models can be created efficiently.

  Some 200 models in SDF format have been contributed by participating
  ecosystems; new models are being submitted continually.  Version 1.0
  of the SDF specification was published on the OneDM github
  repository and as an Internet-Draft.  OneDM is now focusing on
  consolidating the body of submitted models and developing processes
  for arriving at harmonized models that span different industry
  ecosystems in a common way.

  Further development is needed on SDF, both with respect to
  functionality and editorial quality.  OneDM is looking towards IETF
  as the standards development organization that is both providing the
  technical quality sought after and fits into the open collaboration
  model of OneDM itself.

  The objective of the ASDF WG will be to work with OneDM and its
  contributing organizations and develop SDF to an IETF-quality
  specification.

  In the process, some smaller pieces may become usable independently
  from SDF itself and its applications.  JSON Path (similar to, but
  different in scope from JSON Pointer documented in RFC6901) might be
  an example for such a spin-off specification -- it is currently
  defined on a website and would benefit from a more formal definition
  so it can be used in discovery processes involving SDF models.

- Status: WG Forming
- Responsible AD: TBD
- BoF proponents: Michael Koster <michael.koster@smartthings.com>, Carsten Bormann <cabo@tzi.org>
- BoF chairs: TBD
- Number of people expected to attend: 50
- Length of session (1, 1.5, 2, or 2.5 hours): 100 minutes
- Conflicts to avoid (whole Areas and/or WGs): CORE, CBOR, COSE [fill in!]

- Agenda
   - Brief introduction into OneDM, SDF (Proponents)
   - Views of contributing ecosystems (e.g., OCF, OMA LwM2M, ...)
   - Charter presentation
   - Discussion
   - Calling the questions
- Links to the mailing list, draft charter if any, relevant Internet-Drafts, etc.
   - Mailing List: (not yet)
   - Draft charter: https://github.com/one-data-model/ietf108/blob/master/charter.md
   - Relevant drafts:
      - Use Cases:
         - (no draft, see https://onedm.org and https://onedm.org/faq for info)
      - Solutions
         - https://www.ietf.org/id/draft-onedm-t2trg-sdf-00.html
