# OS-A SEE TG Meeting Minutes

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

