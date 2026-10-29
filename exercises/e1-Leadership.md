# Exercise 1: Leadership

Use the settings below as a starting point for your enterprise and organization. Make each choice in the admin settings, then be ready to explain why it fits your team’s needs.

## 1. Repository rulesets

1. Go to your **Enterprise**.
2. Select **AI controls**.
3. Select **Agents**.
4. Scroll to **Repository ruleset** and choose the agent controls your organization wants enforced through its ruleset.

## 2. Custom instructions and content exclusions

1. Go to the **Organizations** tab.
2. Select your organization in the list.
3. Once you are in your organization, select "Settings" then **Copilot**.
4. Add or update **Custom instructions** with guidance your organization expects Copilot to follow.

For example:

> Use clear, concise language. When suggesting or changing code, favor secure, maintainable approaches and follow the conventions in the repository. Don’t invent facts or hide uncertainty; state assumptions when relevant. Never include secrets or credentials in responses. For changes with security or data-loss implications, explain the risk clearly.

5. Add content exclusions for files Copilot should not access. For example:

```yaml
"*":
  - "**/.env"
  - "**/secrets/**"
  - "**/*.pem"
```

## 3. Cloud and Code review

### Cloud settings  

1. In the same **Copilot** settings page, select **Cloud**.
2. Select **Copilot**, then **Cloud agent**.
3. Enable **Allow shared automations** so teams can use organization-approved shared automations.
4. Enable **Require write access to trigger automations** so only users with write access can trigger them.
5. Enable **Claude** and **Codex** partner agents if your organization has approved them. If not, leave them disabled and explain what approval is needed.

### Code review settings

1. In the same **Copilot** settings page, select **Code review**.
2. Set the default review effort to **Lite** for faster reviews on routine changes.
3. Set the maximum review effort to **Balanced** to allow more thorough reviews when needed while keeping review effort bounded.
4. In the approvals section, choose whether Copilot can approve pull requests **Everywhere**. Enable this only if it matches your review policy, and be ready to explain who remains accountable for approval.
5. Block reviews requested with an external Copilot license if your policy requires reviews to use organization-managed licenses.

## 4. Internet access

1. In the same **Copilot** settings page, select **Internet access**.
2. Review **Copilot in the cloud** and **Copilot code review** separately.
3. Set **Enable firewall** to **Enabled** to restrict outbound connections and reduce data exposure risk.
4. Set **Recommended allowlist** to **Enabled** to allow common dependency sources while keeping other destinations restricted.
5. Decide whether to enable **Allow repository custom rules**. Enable it when repository admins should be able to add project-specific hosts; disable it when all exceptions must be managed centrally.
6. If a required host is blocked, select **Organization custom allowlist** and add only the domain or URL your organization needs. For example, `packages.example.com` allows that domain and its subdomains.

## What to explain to leadership

- **Rulesets:** "I can set organization-wide rules for which agents are available, so users work with agents that meet our requirements."
- **Custom instructions:** "I can give Copilot shared guidance about our conventions and priorities, so teams have a consistent starting point for how it should approach their work."
- **Content exclusions:** "I can identify files or paths Copilot should not access, helping protect sensitive content."
- **Cloud agent and code review:** "I can control which cloud agents, automations, and review capabilities are available, and set boundaries for how they are used."
- **Internet access:** "I can limit where Copilot connects, while allowing trusted hosts that our teams need."

---

[Next exercise: Finance →](e2-Finance.md)
