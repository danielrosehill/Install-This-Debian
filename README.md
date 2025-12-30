# Install This Debian, Please!

I have become a huge proponent of using agentic AI tools and command-line interfaces for a pattern of use that can be termed computer operation, desktop administration, or, a little more ambitiously, sysadmin. 

It can be used both on local machines as well as on remotes. 

Simply put, it involves using the agent's ability to execute Linux bash commands to operate computers.

This use case has seen very little direct interest and attention from vendors (and a lack of fine-tunes targeting this use-case!), as most agentic tools remain wedded to the assumption that they will be operated within a repository and subject to understandable but highly restrictive sandboxing which proves a huge impediment to the fluid operation of this pattern.

Many advanced benchmarks exist, providing data on the abilities of various frontier models to engage in complex problem-solving and solve pull requests on GitHub (SWE Bench etc) These are very useful. But I wanted to create a simple proxy to be used for back-of-the-envelope tests to see if something can work or not.

## The Simple Test Task

The extremely simple task provided is asking the CLI to install a Debian package on the desktop. 

You can add a misspelling to the prompt and deliberately loosen up your punctuation. Download any Debian (or .exe etc) to your desktop and ask the agentic CLI/TUI to install it. The instruction should be unambiguous with basic reasoning.

While this may seem like an incredibly simple test, the variance in how agentic AI tools handle this request is quite substantial. 

Limitations like very strict sandboxing or refusal to escalate to `sudo` will be immediately apparent.

This is also an easy way to gauge how flexible a front-end interface, like a wrapper over a CLI, is for this intended purpose. Launched from any directory, you can assess whether the agent is able to move freely across directories (or not).

## Success Criteria

The success criteria is for a model that defies best practices in the code generation and code editing use case: specifically, don't bother the user with permission for an obvious request!

Instead, execute the task and complete it as speedily as possible. Reasoning demonstrated during this task can include disambiguation, inference, and other intermediate steps.
