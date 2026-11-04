# Part 4 of 6: The Risk: Plugins as a Supply Chain

*Series: Skills, Plugins, and Governance in the Enterprise*

## Brief

Plugins carry the same risks as software dependencies, with more direct access. Walk through what a plugin can actually do (hooks running as the user, MCP servers, executables, scripts bundled in skills, silent auto-updates) and pair each with its abuse case. Bring in the evidence: malicious skills found in public registries, scanners evaded, pinning bypassed. End on the trust gap: what people assume about marketplaces, permissions, and reviewed code versus what's actually true.

## Thesis

Installing a plugin is closer to adding a dependency with shell access than downloading a template, and most people don't treat it that way.

## Outline

1. **Hook**
   - A concrete scenario: a useful plugin whose hook quietly sends data somewhere, or whose skill nudges Claude to do something the user never asked for.

2. **Short recap**
   - Two sentences pointing back to Parts 2 and 3. The capabilities that make plugins powerful are the subject of this post.

3. **What a plugin can do, and the abuse case for each**
   - **Hooks:** run shell commands at lifecycle points, with the user's full permissions and outside the sandbox.
   - **MCP servers:** local processes started on the user's machine, also outside the sandbox.
   - **`bin/` executables:** callable by Claude through its shell.
   - **Skills, commands, and agents:** enter Claude's context as instructions, so they can steer behavior (prompt injection by design).
   - **Auto-update:** the files you reviewed can change after you reviewed them.

4. **Scripts are the payload**
   - Config files show *that* something runs, not *what* it does.
   - Hooks often call bundled Python or shell scripts; MCP servers are often Python processes; skills frequently ship a `scripts/` folder Claude is told to run.
   - Runtime `pip install` or `npm install` steps extend the supply chain one more hop.
   - Reviewing a plugin means reading the scripts the manifests point to.

5. **This isn't hypothetical**
   - Koi Security: 341 malicious skills among 2,857 on one public registry (Feb 2026, cited by the Cloud Security Alliance).
   - Cloud Security Alliance research note on malicious skills evading marketplace scanners (July 2026).
   - Air Security research on a marketplace version-pin bypass across four coding-agent CLIs, including Claude Code, fixed before publication (Sept 2026).
   - Keep this section short and factual.

6. **The trust gap**
   - Assumption: a known marketplace name means vetted. Reality: the name says who publishes the catalog, not what each plugin does.
   - Assumption: permissions and sandboxing cover everything. Reality: hooks and MCP servers run outside them.
   - Assumption: what I reviewed is what runs. Reality: auto-update can change it.
   - Assumption: I can see what it does from its config. Reality: the behavior lives in the scripts.

7. **Bridge to Part 5**
   - None of this means avoiding plugins. It means governing them, and no single control is enough.

## Personal angle to fill in

- [ ] A plugin you reviewed and what you found (even if benign)
- [ ] An assumption you or your team held that turned out wrong

## Sources to cite

- Claude Code Docs, *Plugin security and trust*: https://code.claude.com/docs/en/plugins/security.md
- Qodo, *What Are Claude Code Plugins?* (summarizes the Koi Security, CSA, and Air Security findings): https://www.qodo.ai/?p=22616
- Verify and link the original Koi Security, Cloud Security Alliance, and Air Security publications before publishing.

## LinkedIn hook ideas

- "Every plugin you install runs as you."
- "We spent a decade learning to vet npm packages. AI plugins need the same scrutiny."
