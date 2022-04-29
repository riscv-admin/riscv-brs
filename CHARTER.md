# RISC-V OS-A SEE Charter

The OS-A SEE (Supervisor Execution Environment) TG will write a specification targeting binary compatibility for rich operating systems (OS) so that many specific implementations can be built that adhere to OS-A SEE for the purposes of booting the OS. With the OS-A SEE defined, it is expected OS distributions can build compliant binary compatible images that target multiple vendors’ implementations. The use of a common foundation and dynamically detected value-adds will allow off-the-shelf compatibility for users as well as enable differentiation for the vendors.

The focus will be on the interfaces between the operating system and its SEE (through which the operating system may, for example, access services provided by the firmware or otherwise). The specification will require RISC-V implementations adhere to a dependent [RISC-V Profile][1]. The dependent interfaces will include both boot time and runtime components for conveying information to the operating system for managing the system. Industry and RISC-V standards will be leveraged for those interfaces.


[1]: https://github.com/riscv/riscv-profiles/blob/main/profiles.adoc
