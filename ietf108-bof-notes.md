# ASDF BoF

## ASDF BOF AGENDA

TIME: Tue   2020-07-28	11:00UTC
https://www.timeanddate.com/worldclock/fixedtime.html?msg=IETF108+ASDF+BOF&iso=20200728T13&p1=141


materials:    https://datatracker.ietf.org/meeting/108/session/asdf
agenda:       https://www.ietf.org/proceedings/108/agenda/agenda-108-asdf-00
slides:       https://datatracker.ietf.org/meeting/108/materials/slides-108-asdf-consolidated-slides

meetecho URL: https://meetings.conf.meetecho.com/ietf108/?group=asdf
jabber:       xmpp:asdf@jabber.ietf.org?join
mailing list: https://www.ietf.org/mailman/listinfo/asdf
              https://mailarchive.ietf.org/arch/browse/asdf/

etherpad:     https://codimd.ietf.org/notes-ietf-108-asdf?edit

BLUE SHEET WILL BE TAKEN BY MEETECHO.


97 people in jabber room

Chairs: Niklas Widell and Michael Richardson

Notetakers: Ari Keränen and Jaime Jiminéz

Jabber scribe: Michael Richardson


## AGENDA:
1) Welcome and Note Well

### Niklas presenting Agenda.

2) hellos and mic check

3) Intro; brief introduction into OneDM, SDF (Proponents);
   (and clarifying questions) [30 minutes]

### Carsten Bormann (CB) presenting.
- We currently have lots of diversity in IoT systems that doesn't provide much value.
- Objective is to harmonize data models.
- No need for another wire format, rather harmonized data and interaction models. 
- Some components already in place (SenML, CDDL, W3C TD...) however they solve different problems. 
- Avoid creating another standard. (xkcd 927) Ecosystems should not see ASDF as a competitor.
- OneDM recently came out: https://onedm.org , started as a liason after ZigBee Hive meeting. SDOs operating under NDA, one liason per org is complex, came out in order to have a more open process.  
- Biggest achievement was legal agreement. Using open source license (BSD3) allows cooperation on common models without jumping through legal hoops. Second thing: common specification format SDF v1.0. Now getting data models published using SDF. SDF not a paper tiger: people have taken SDF and looked into how can convert models to SDF. Some also doing conversion to other direction.
- SDF as common format for collaboration (the "red star"). SDF is a domain specific language represented in JSON. SDF defines data models inspired by json-schema.org. SDF interaction is based on 3 types of affordances: property, action and event. 
- OneDM will be one of the users of SDF; others are the different ecosystems 
- YANG is not optimized for converting models from and to it. YANG is focus of people who want to define full-fledged models. Main user of YANG is the IETF itself. At high level may look similar, but if look how it's used, it's quite different.
- Proposal to standardize starting from draft-onedm-t2trg-sdf-00; after which gaps in functionality, references, usability will have to be identified. 
- The spec currently in many places needs to be still improved. Gaps in functionality, for example composition. Some things in SDF being used are not standardized yet; could copy in the doc or get the normative refs standardized. Work remains. 


Cullen Jennings (CJ): could you say a bit more about what those things are?
CB: JSON schema org the most daring. Using that to define the data schemas. Some others too, but will have to look
CJ: close enough, thanks!

- We can also still change SDF. It's not rubber stamping. OneDM is working on harmonizing things. Possible to work witht he contributing orgs to develop SDF. Right now things are still wide open. SDF will interact with tools. 

Andre Bondi (AB): Question on the inclusion of performance characteristics. It would be useful to know about performance and communication pattern requirements. If have centralized way to collect, we can understand what is the burden in the central controller. How stringent response time requirements. Other non-functional requirements?
CB: interesting idea, maybe not that easy to capture non-functional requirements. It could be useful if we manage to do it. 
AB: useful for capacity planning purpose
CB: can be only analyzed with protocol bindings. Will need to go further there before making useful statements. Agree, we should examine that.

- Why standardize this now? OneDM has completed a usable doc and happy to transfer change control to IETF.
- Why standardize at all? OneDM contributors and implementers need a stable, well-defined spec.
- Why IETF? Vendor-neutral process. Ecosystem SDOs already use IETF specs. IETF has some experience with domain-specific data modeling.
- What would ASDF WG do? Focus on delivering SDF spec in RFC form, ensure that normative refs are stable, work with other stakeholders. 

Bron Gondwana (BG): Given the timeline which is of few months, it seems incompatible with not forming a WG. Which is the timeframe?
CB: not something like January CES but getting started in months would be useful. Getting stable SDF 1.1 or 2.0 out of WG end of next year would be very important.
BG: So it sounds that it is a WG forming group in all but name. 
Charles Eckel (CE): how see translation happening, and models defined in SDOs. If IETF would make changes. How to make sure translations stay valid.
CB: It is the job of OneDM to actually get the harmonization process defined. We are discussing a document on how the process should work in detail. Some of your questions will be answered by that document. 
Actual tools will be written by ecosystems and vendors there. Need to keep up relationships there. They will be important voice on what changes can be made. Need to keep them at the table.
CE: Tooling was indeed very important for YANG and we have also seen it to be very important for Open Source. 
CB: some of these tools have been made at IETF/WISHI hackathons. We have built components that went into those tools.

4) Views of contributing ecosystems (Bluetooth, OCF, OMA [LwM2M], Zigbee) and
   a few interested vendors (…); clarifying questions [20 minutes]

- Alan Soloway (AS) presenting the OMA BoD pov. Overview of the orgs (DM and IPSO) and Liason Statement signataries that support to the OneDM work. BSD-3 clause license is also already. Presenting a tool that translates from SDF to LwM2M. 
- Michael Koster (MK) presenting the pov of Zigbee alliance (BoD) and Project CHIP (Steering committe). Zigbee Use Cases; need to provide a friendlier entry point than XML for the Cluster libraries and SDF would be a good match. 
- Wouter van der Beek (WB) presenting OCFs pov. BSD-3 clause license is also already. Created a conversion tool between OCF and SDF. Liason endorsing the work on public website.
- Szymon Slupik (SS) precenting bluetooth pov (chair of Bluetooth SIG mesh WG). A focus area on smart buildings, which they believe that it is good match for SDF work. Bluetooth SIG endorses this work. They are alooking into using SDF as the native environment to represent data models. 
- MK presenting uses cases from the SmartThings pov. Objective is to use SDF for device integration, capability model, 3rd party API integration; using swagger and WoT for it.
- Ari Keranen (AK) from Ericsson pov. Ericsson uses SDF, see it as a valuable tool to reduce integration costs. Having a common language that would reduce the cost. Another use is to using SDF together with LwM2M/IPSO. Already have contributions with tools for model development and translation.

5) Discussion (beyond clarifying questions) [30 minutes]

Questions to come: 
Do we agree on the plan?
Do we have energy to do this?
Should it be done in IETF?


CJ: Regarding change control. How much are we open to significantly change SDF? Or people want to give it largely as is. Is this starting point or close to done?
CB: This spec is actually and unusually open-to-change specification. People usually don't directly write SDF but use tools to translate to/from. We did sweeping changes leading to 1.0 and was relatively painless. Not free to do, but certainly possible.
AS: The answer is actually "both". It is a well-stablished floor in which we can start evolution. We have a great foundation but we need to work on it to evolve.
Michael Richardson (MR): Kinda inheritance (?)
CJ: didn't argue for that model, just example of a significant change
WB: We have a working situation in which SDF fits multiple ecosystems, at some point we need to draw a line in order to get started. Is this enough? No. But this kind of work will never stop. 

Andre Bondi (AB): Worked for a long time on performance and found that it is often a problem, it would be good to embed performance characteristics information early on. Maybe something needs to be communicated at some point of time. Seems this could be right place to capture that.

NW: interesting topic. Not right now focus of group but could be extension.
AB: happy to take issue off-line
CB: we have asdf mailing list where could discuss this and have other people participate


6) Calling the questions [10 minutes]

NW (as chair): was  also asked in Jabber why not WG forming BoF. There was wish to see more industry support for this. That's why had lined up industry folks here. This work has been progressing and is reasonably mature. Don't hear any disagreement -- Barry to comment as AD?
Barry Leiba (BL): going well. Let's get sense whether people think IETF is the right place to do this

HUM: IF YOU WILL PARTICIPATE IN THIS WORK, please HUM
(in jabber: a few. Plus FORTISSIMO result)


Steps: 
1.- Draw up a charter and capture what was discussed in the meeting. Any comments against?
No comments.
2.- Do we have energy to do this? User industry seems to have energy; have expressed strong interest in this. Is there enough IETF'er to do work on this? Bunch of highly-engaged IETFers in IoT space on this. 

BL: could take a hum for "if you would be participating in this work, hum"

NW: first question: if this work starts, would you participate (use the hum tool -- to the left of the chat icon)

(result: Fortissimo)

BL: already asked objections, wasn't any. Fortissimo for "i would work on this" is promising

Eve Schooler (EV): can we have some discussion about where other than the ietf would this work get done?

QUESTION: IS THE IETF THE RIGHT PLACE TO DO THIS?

CJ: since no objections, this hum may not give that much info
BL: we could discuss what are the alternatices

NW: OneDM folks, as Carsten stated, think IETF is the right place. If we want to tell SDF folks to go elsewhere there should be objections to not do it here. If have objections please come to mic line.

{mic line empty on alternatives}

NW: still needs charter etc, but as I see it there's no enthusiasm  to discuss alternative places to do this.

CJ: has been really well run bof and  convincing. Why not have the charter discussion here and now?

BL: this came from BoF approval call; perhaps remember there were some concerns about industry pick-up on this. If there's broad interest. Approved as non-WG forming BoF with that in mind. Sounds to me it's pretty clear we should send charte to list, finalize that, and get it to me.

CJ: agree with the plan!

Pete Resnick (PR): seems there's charter in back pocket to work on.  Anything controversial there? Any particular issues where need input? 

CB: maybe we should show the charter (even if against protocol). 

https://github.com/one-data-model/ietf108/blob/master/charter.md

PR: no need for details; anything you think need group input? Anything in particular need help with?

CB: interesting thing in this work -- Last 3 paragraphs. Interesting thing of SDF: stew of different technologies. Input coming from various places. Some can be handled separately, like JSON path. Don't know yet if need it beyond discovery. Things like how we do data modeling and interaction modeling parts. Hope we can handle all the questions in the WG. Sometimes IESG wants decisions made before WG is formed so that WG doesn't get blocked by bike shed discussions but don't see that as problem here. Way we got to SDF 1.0 was very constructive process. Some WG and RG relationships, like CBOR for CDDL specs, formal description languages RG, etc.

BL: only thing  that strikes is to  "work with OneDM and contributing orgs" will get questions  from IESG. Also concerns about there being representatives that say "OneDM says this" rather than individuals working on this.  Re-spinning that might be useful cosidering how  IETF works. PRefer to have people who care to be in the  WG doing the work.

CB: yes, don't want to do this based on liaison statements. Limited usefulness with LSs. That text should be changed, agree.

NW: Please sign up for the ASDF list (asdf@ietf.org) and for the charter discussions if you have interest on this. So at this point we have a plan forward. 

CB: if you are interested in SDF there are various  tutorial resources you  can use. One in my youtube channel. There's onedm.org as landing page for info about OneDM. Also find github repos for various models. All work in progress, not finished. Needs lots of work but a good way to get familiarized with this.

Georgios Karagiannis (GK): I'd like to know whether we have looked into other SDOs like OneM2M and W3C. Have looked at what has been done there?
CB: Yes. Have even slide about W3C at the backup materials.

MK: as individuals and also as org have worked with the W3C WoT group. We are focusing on the domain specific vocabularies that are explicitly excluded from WoT. Metamodel very much aligned. W3C plugfest has been using OneDM definitions in thing descriptions. TD applies descriptions to over the wire data formats.

GK: agreement between W3C and OneDM?
MK: yes, currently working on concept called TD templates that can make TDs composable together with OneDM definitions. Also other intersections like discovery: the terminology used can be OneDM URIs. Also other vocabulariess like iotschema can be used. 
GK: and OneM2M
MK: OneM2M was involved early on but had to partition the work due to Huawei issue. But now not issue. OneM2M is potentially part of this. Also modeling part of OneM2M and OneDM has another potential intersection.
GK: also agreement here?
MK: was early on but has not been lot of participation. Now being open and everyone can participate we need to get OneM2M back to participating.
CB: T2TRG has been  organizing number of informal events where we bring people from SDOs and orgs together. Have had lots of common events with W3C WoT. WoT is bit of sister org of T2TRG. Next WISHI call day after tomorrow where we talk with MSFT about DTDL. Another language we want to take with SDF. Will have discussion there. Coordinates in T2TRG mailing list; can send invite to ASDF list too. 

https://github.com/t2trg/wishi/wiki/Agenda-items#wishi-online-meeting

NW: OneDM coming out as visible org, there are many reasons, one was to be able to address more orgs than in the original liaison. This is about reaching out to other orgs and incorporating their requirements.

NW: Seems we are done. Any last thoughts?

BL: thanks for the chairs -- very well run BoF!

NW: Thanks!
