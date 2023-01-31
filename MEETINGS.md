# OS-A SEE TG Meeting Minutes

## 2023/01/31
- [Meeting Presentation](https://docs.google.com/presentation/d/1IMDUkH7IyxKEuKHJbjLBIWj81ERrAk-PSRS_xf9uGQw/edit#slide=id.p1)
- Went over naming of spec since was contentious in the past. Seemed to get some consensus on BRS - Boot & Runtime Services.
- Went over Platform interaction with BRS. Drew a picture and collaborated on changes. Group decided to have a base hardware requirement spec. That needs to be worked on/created.

## 2023/01/24

- [Meeting Presentation](https://docs.google.com/presentation/d/14s74R9TMw3J6L50x9dgvlieRv7GkOjT_hb93w1r135w/edit#slide=id.p1)
- Strawman Charter change led to discussion of naming. Large desire is to change the name but also include modifications that more closely cover the expected result.
- OS-A SEE Name brought up again. People would like to see a name change. Possibly SEEI. "Common Boot Services" was also brought up. Mark Himelstein indicated we should at least reference and/or coordinate with existing specs in RISC-V.
- Glossary of terms and definitions needed.
- Platform vs OS-A SEE spec distinction came up again. People looking for definitive explanation of what type of requirements fall into Platform. OS-A SEE needs some hardware requirements to set expectatiosn, but much of the system (peripherals, etc) can be punted to the Platform.
  - Paul W mentioned some hardware requirements are in the current proposal. Need to find and be precise in language.
- Andrei asked in chat: Will there be a common SEE? Will an SEE for IoT differ from SEE for laptop or sensor? Did not touch on this during the meeting, but we should conclude on that.
- Went over overview of proposals about the two receipes (HI and VI)
  - Horizontally-Integrated and Vertially-Integrated names: Mark Himelstein does not like them.
- Discussed requirements of spec organization. e.g. Unique identifiers given to each requirement so one can compose and drive tests against each item.
- Concept of LBBR punted out until a need is there.
- Briefly talked about ratifiction plan and requirements for testing as well as a proof of concept.

## 2023/01/10

- [Meeting Presentation](https://docs.google.com/presentation/d/1RDaw280y-5BX3dE4dmIUBlWI9yQptsSG9NDs2jiLXRw/edit#slide=id.p1)
- Quickly went over potential changes to OS-A SEE Charter as discussed at Members' Day at RISC-V summit. Aaron to propose a new charter and send out to list.
- Mark Himelstein requests OS-A SEE Ratification Plan to be presented to Chairs meeting in early Feb. Include proposed charter change as well.
- Need a plan/description of how other specs compose into building a system. This can be a separate doc explaining how that fits/works together. e.g. Platforms
  - Platform needs to be scoped and qualified. Need to start that discussion with broader community.
- Andrei walked through his [proposal](https://docs.google.com/document/d/1X0TSbheEJjRGWhG2nzUnfIl_QcHWSuvd/edit?rtpof=true).
  - Thinking is that this is equivalent to BBR as a base.
  - Comprised of recipes.
  - Plan to move to asciidoc. Aaron to put together a format to start filling things in. Will then use pull requests for changes.
  - FFH ACPI bindings for RISC-V SBI. Proposal from Andrew is mid Feb.
  - IOMMU ACPI [proposal](https://github.com/vlsunil/riscv-acpi/blob/iommu/rimt.adoc). Not sure if latest.
- Meeting cadence to increase starting week of Jan 23.

## 2022/11/30

- [Meeting Presentation](https://docs.google.com/presentation/d/1nEMoR44drgV89j8fhUyhaaMzQb4yWNMYkuzHyeod8Ak)
- Intended to have Andrei talk through his [proposal](https://docs.google.com/document/d/1X0TSbheEJjRGWhG2nzUnfIl_QcHWSuvd). However, something came up at last minute where Andrei could not attend. Meeting adjourned early.

## 2022/11/15

- [Meeting Presentation](https://docs.google.com/presentation/d/1bEA4mtRICCHNcEng2_9AJ-iV30Q0cCq9xk-xUHX_6MM)
- Wanted explain how the OS-A SEE was originally envisioned depending on Profile in the underlying dependency chain.
- Goals are:
  - Targeting binary compatibility
  - Rich OSes
  - Focus on SW interface for booting along with runtime services
  - Utilizes industry standards
- How will future Platform specs utilize the other RISC-V specs?
- Should incorporate existing HW in marketplace -- problematic if only future looking and wanting to align with Profile. Allow market to decide pairing of Profile with OS-A SEE? By way of Platform?
- Andrei: remove hw dependencies. e.g. Profile dependency. Let Platform bring things together.
- Paul: OS-A SEE wasn't originally intended to target IOT devices.
- Andrei: wants to make it exteremely generic and applicable. Pyramid narrowing at top. Being ahead of HW not helpful in ARM land from past experience.

## 2022/11/01

- [Meeting Presentation](https://docs.google.com/presentation/d/1zrkMhqvDaZbaYSsG1PI8Dsvjxr0K0EwaOFzbmJwv2zM/)
- ACPI vs DT - Andrei had a [thread](https://lists.riscv.org/g/tech-os-a-see/message/131) on the mailing list.
  - Discussion and conclusions of the thread is have both ACPI and DT as options.
  - Be agnostic. Let ecosystem decide based on system vendors’ products to drive ecosystem support.
- EBBR vs Full UEFI
  - Andrei: UEFI is BBR (Arm's Base Boot Requirements).
  - EBBR relaxations/minimums but not allowed today in UEFI spec. AR: Understand the overlap and figure out how to separate out requirements in OS-A SEE spec.
  - Sunil: in order to reduce UEFI concern -> if HW feature exists then protocol must be there. Can always fix UEFI spec, if needed.
  - Andrei: focus on booting spec. Allow for "industry norms" using body of existing tests.
- SEE prescriptive language for certain SBI extensions? Andrei suggest as you go up the composition stack one can't relax. One can only refine or restrict. Funnel mouth is big @ SEE level
- Don't be in business of adding restrictions of areas of concern
- Dependent spec versions would be indicated as >= version


## 2022/10/18

- [Meeting Presentation](https://docs.google.com/presentation/d/1utzR6UG6bAW8MZrgIuj42HVgvl87ll-cUKK0xnXdC1c/)
- Rehashed premise of OS-A SEE trying to incoproate SW & HW requirements, if any. How to decide what is mandatory in OS-A SEE spec? HW and SW requirements exist in many existing and future RISC-V specs (Profiles and Platforms).
- How are the RISC-V specifications composed? OS-A SEE on its own or part of a stack?
- Greg brought up AiA - optional or required?
  - Ramifications of big tent -- Optional requirements would lead to SW must support both. i.e. Imposing constraints on SW. Can it be a choice of the OS?
  - Should be focusing on standard SW & distros.
- Darius reiterated use of constant and transparent language
- Ved said OS-A SEE must be useful. If OS vendors bypass it -> not useful.
- Philipp indicated may be useful to punt out strict HW requirements to future Platform docs
- Ved reminded need of HW discovery. Should be fine with ACPI or DT.
- Future versions of OS-A SEE? Likely multiple future versions & releases to keep up with changes in dependent specs.
- Greg suggests adapting philosophical approach: wants more prescriptive and limiting optionality
- Key optionality question: interrupt solutions?

## 2022/10/04

- [Meeting Presentation](https://docs.google.com/presentation/d/1FPm5COOnTglsqOhWLFhQZD2onDmrxceyZPtIkKpTsqE/)
- Attempted to go through SBI spec to determine what should be required or not for the SBI extensions. Good discussion ensued. Arrived at deferring to the SBI spec itself as it has mandatory vs optional. SBI spec also has extensions specific hypervisors vs regular booting. In the end may have to call out specific extensions being mandatory, but 1st pass is to defer to SBI spec.

##  2022/09/12

- [Meeting Presentation](https://docs.google.com/presentation/d/1uW9OB3ocltpWJj8fYdfMOnNWHIAuTY-yxRH5MUYi6p8/edit)
- Went over the [Charter](https://github.com/riscv-admin/os-a-see/blob/main/CHARTER.md)
  - Discussed what is in scope for OS-A SEE
  - Paul W. asked about hardware requirements. In alignment with the Charter, we should be focusing on compatibility across RISC-V systems for loading and running operating systems.  Hardware requirements should fall under the Platform specifications.
  - Additionally Kumar indicated SW view of the world should be the focus.
- Paul brought up a distinction of feature / device binding required in both early and later stages of kernel startup.
- Target Audience of OS-A SEE? Ideally would be standar operating system distributions to further expand the ecosystem. Users of the RISC-V systems would benefit, but it's important to allow operating system distributions to target a conformant spec.
  - [RISC-V Platform Spec Review Comments](https://docs.google.com/document/d/1PfvLw3f-tPTRjl6Rw614O_RaA62oKeHlTfu7g6KZ4Vs/edit) would collected in 2021. Need to incorporate this feedback into the spec for the parts that align with the OS-A SEE Charter.
- psABI would not fall into the purview of the OS-A SEE spec. Reason: Kumar syas focus should be on ability to run same OS on multiple implementations.
- ACPI vs DT. Acknowledge we need to support both. May want to allow an OS to choose which one to support (or both) instead of mandating both. Allows for OS vendors to define their own product. Topic to still be discussed.
- Need to start framework of document and start seeding content.

