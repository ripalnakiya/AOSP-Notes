# SELinux

SELinux, which stands for Security-Enhanced Linux, is a set of security extensions implemented in the Linux kernel to enhance the overall security of the operating system.

SELinux is a security framework integrated into the Linux kernel. It provides a set of access control policies and mechanisms that go beyond traditional Linux permissions.

It is a MAC(Mandatory Access Control) security mechanism in android.

It is a set of rules that are enforced by the kernel.

It restricts the actions that processes and users can perform on the system.

> SELinux uses a policy language that specifies rules for how processes and users interact with various system resources.

This enhances overall system security by mitigating the impact of potential security vulnerabilities and unauthorized access.

---

SELinux depends on lables to enforce access control.

> Labels are used to identify the type of a process, match actions and policies.

---

SELinux operates on the priciple of Default Denial. That is, everything is denied unless explicitly allowed.

## Global Modes

SELinux can operare on two global modes:

- Permissive Mode
  - Permission denials are logged but are not enforced.
- Enforcing Mode
  - Permission denials are logged and are enforced.

Android includes SELinux in enforcing mode.

> In Enforcing mode, disallowed actions are logged and denied.

## Types of Access Control Models

- MAC (Mandatory Access Control)

  - The system determines which subjects(android processes) can access which objects(files, sockets, ports, etc.).

- DAC (Discretionary Access Control)
  - The owner of an object specifies which subjects can access the object.

---

Rules are defined in `*.te` files
