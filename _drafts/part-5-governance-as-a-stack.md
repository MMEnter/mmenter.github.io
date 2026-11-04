# Part 5 of 6: Governance as a Stack

*Series: Skills, Plugins, and Governance in the Enterprise*

## Brief

No single control solves plugin risk, so this post lays out governance in layers: review at install time, control at the source, policy through managed settings, and visibility through telemetry and inventory. The "ground level" case: governance that only exists in admin policy misses the moment a person decides to install something, which is where automated review tools, including plugins built to review other plugins, earn their place. Address the obvious question of who governs the governor. Include a checklist split by enterprise and personal use.

## Thesis

Plugin governance is a stack, not a product, and it starts at the point of install.

## Outline

1. **Hook**
   - Recap the trust gap from Part 4 in one or two lines. The question now is what to do about it.

2. **Why one control isn't enough**
   - Scanners can be evaded.
   - Policies don't see what a plugin actually does.
   - Review without pinning is undone by the next update.

3. **The four layers**
   - **At install (ground level):** inventory what the plugin contains, read hooks, MCP configs, `bin/`, and the scripts they reference, check skills for injected instructions. Automated reviewers, including plugins built for this, make this fast and repeatable. Their output is a gate for human judgment, not a verdict.
   - **At the source:** curated private marketplace, version pinning (commit SHA or archive digest), updates treated as new reviews.
   - **At the policy layer:** managed settings to allowlist marketplace sources, restrict hooks to approved plugins, and disable side-loading flags.
   - **After the fact:** telemetry and plugin inventory, so you know what's installed when something goes wrong. Enable detailed plugin names in telemetry, since non-official plugins are otherwise reported generically.

4. **Why ground level matters**
   - Policy is set once by admins; install decisions happen every day by individuals.
   - A review step at install puts governance where the decision is made.

5. **Who governs the governor?**
   - A review plugin has the same privileges as what it reviews.
   - Keep it small and auditable, pin it, source it from your own marketplace, and treat its output as advisory.

6. **Scaling it**
   - **Enterprise:** all four layers, a named owner for each, a documented review process for new plugins and updates.
   - **Personal:** the same habits, lighter weight.

7. **Checklist**
   - **Enterprise**
     - [ ] Restrict installs to an approved private marketplace
     - [ ] Pin every plugin version
     - [ ] Require review for new plugins and every update
     - [ ] Restrict hooks to managed or force-enabled plugins
     - [ ] Turn on detailed plugin telemetry
     - [ ] Assign an owner to every listed plugin
   - **Personal**
     - [ ] Prefer Anthropic's official and community marketplaces
     - [ ] Read `hooks/hooks.json`, `.mcp.json`, `bin/`, and referenced scripts before installing
     - [ ] Turn off auto-update for third-party marketplaces
     - [ ] Uninstall what you don't use, and clear its cached files

8. **Bridge to Part 6**
   - The framework is the easy part. Next: what it looks like to run this day to day.

## Personal angle to fill in

- [ ] Which layer your organization had first, and which it was missing
- [ ] How install-time review fits into your workflow
- [ ] How you handle updates to approved plugins

## Sources to cite

- Claude Code Docs, *Plugin security and trust*: https://code.claude.com/docs/en/plugins/security.md
- Claude Code Docs, *Manage plugins for your organization*: https://code.claude.com/docs/en/plugins/org

## LinkedIn hook ideas

- "Plugin governance isn't a tool you buy. It's four layers you build."
- "Your admin policy can't see the moment someone clicks install."
