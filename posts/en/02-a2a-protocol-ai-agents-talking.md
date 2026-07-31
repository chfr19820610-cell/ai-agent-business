# A2A Is the Protocol for AI Agents Talking to Each Other

Two years ago this sentence would've been nonsense: your AI agents now have a standard way to talk to each other, and it's an open source project on GitHub.

The project is A2A, short for Agent-to-Agent. Google released it on April 9, 2025, with more than 50 founding partners, among them Atlassian, Box, Cohere, Intuit, MongoDB, PayPal, Salesforce, SAP, and ServiceNow (Google Developers Blog). It now sits under the Linux Foundation, and the code lives in the a2aproject/A2A repository.

What it does is simple to describe and hard to build. It lets one agent hand a task to another agent from a different vendor and get the result back. Different vendors, different models, still interoperable.

Before A2A, "AI agent" usually meant a chat window that could call a couple of tools. You asked, it answered. A2A changes the game: agent A discovers agent B, they agree on what gets done, agent A delegates, agent B does the work and hands it back. The closest mental model is a small team, except nobody is in the same office and one of them runs on a completely different stack.

Two terms keep getting mashed together, and the difference matters:
- MCP is how an agent reaches out and touches the outside world, the tools, data, and services outside the model. The agent grabbing a wrench.
- A2A is how two agents coordinate with each other. The agent handing the wrench to the next person.

You need both, and they do different jobs. MCP came first and became the standard for tool access. A2A sits on top and turns a single tool-calling bot into a working team.

For a developer, the practical takeaway is that agent interoperability is becoming a protocol, the way SMTP became the standard for email instead of a feature one company controlled. Once that happens, the integration cost drops and the ecosystem opens up, and anyone still building a walled garden ends up working against the standard instead of with it.

#A2A #AIAgents #MCP #AgentProtocol
