# A2A Just Hit 22K Stars on GitHub. AI Agents Are Finally Talking to Each Other.


Here's a sentence that would've sounded insane two years ago: your AI agents now have a standard way to talk to each other, and the spec hit 22,000 stars on GitHub.

The thing is called A2A — Agent-to-Agent — and more than 150 organizations have gotten behind it. What it does is simple to describe and annoying to build: it lets one agent hand a task to another agent, from a different vendor, and get the result back. Not a fake integration bolted on by the same company. Different systems, different models, actually interoperable.

Up until now "AI agent" meant a chat window that could maybe call a couple of tools. You asked, it answered. A2A moves the game to: agent A discovers agent B, they negotiate what gets done, agent A delegates, agent B does the work and hands it back. The closest mental model is workers on a project, except nobody's in the office and one of them is running on a completely different stack.

Let me separate two terms that people keep smashing together, because it matters:

- MCP is how an agent reaches out and touches the outside world — tools, data, services. It's the agent grabbing a wrench.
- A2A is how two agents coordinate with each other. It's the agent handing the wrench to the next guy.

You need both, and they do different jobs. MCP got here first and became the de facto standard. A2A is the layer on top that turns a single tool-calling bot into an actual team.

If you're a developer, the practical takeaway is that "agentic" is no longer a feature one company controls. It's becoming a protocol, like HTTP or email. Once something is a protocol, the integration cost drops, the ecosystem opens up, and the pace picks up in a way that surprises everyone who was building a walled garden.

I've been digging into how to actually wire A2A into real projects rather than just reading the spec. I put together a starter walkthrough — MCP and A2A together, with templates — and it's on my Gumroad if you want to skip the trial and error. Or follow along; I'm breaking it down piece by piece on my site.

#A2A #AIAgents #MCP #AgentProtocol #DeveloperTools
