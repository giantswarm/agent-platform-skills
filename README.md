# Agent Platform skills

Giant Swarm's curated skills for agents on customer installations of the
[Giant Swarm Agent Platform](https://docs.giantswarm.io/overview/agent-platform/), written to the
[agentskills.io](https://agentskills.io/specification) format.

## Layout

One directory per skill at the repository root, each with a `SKILL.md` and optional `references/`,
`scripts/` or `assets/`. `scripts/validate_skills.py` checks every `SKILL.md` on each pull request.

## Use on an installation

List the repository in agent-manager's `skills.repositories` (Helm values); the portal's create flow
and agent-manager then offer every skill in it:

```yaml
skills:
  repositories:
    - https://github.com/giantswarm/agent-platform-skills
```

An agent pins each skill to a full commit SHA. A new commit here changes no agent until it is re-pinned.
