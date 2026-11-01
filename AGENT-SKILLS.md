# agent-skills pin

This branch (`agent-skills` in flexi767/superpowers, forked from obra/superpowers,
MIT, see LICENSE) is what flexi767/agent-skills pins. Seven skills are installed
from it, without the plugin namespace:

verification-before-completion, systematic-debugging, receiving-code-review,
finishing-a-development-branch, test-driven-development, requesting-code-review,
writing-skills

Adaptations on top of the upstream release (one commit):

- `superpowers:<name>` references between these seven skills use bare names.
- A "Host rules" note in five skills: the project's CLAUDE.md/AGENTS.md wins on
  verification scope and integration policy (test-driven-development,
  systematic-debugging, finishing-a-development-branch), and subagents are used
  only when the user asks for delegation (requesting-code-review, writing-skills).
- requesting-code-review defaults to reviewing the range yourself; the
  code-reviewer template example uses a scratch directory instead of /tmp.

Not installed: using-superpowers (its SessionStart hook), brainstorming,
writing-plans, executing-plans, subagent-driven-development,
dispatching-parallel-agents, using-git-worktrees, diagnosing-superpowers.

To re-pin: rebase this branch onto the new upstream release, review the diff of
the seven skill folders, push, and update the SHA in agent-skills/skills.txt.
