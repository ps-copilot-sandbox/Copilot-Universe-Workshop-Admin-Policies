# Exercise 3: Security

Review how Copilot access is configured, which features are available to the organization, and how administrators can trace policy and access changes.

For the presenter, start at the [GitHub Universe enterprise](https://github.com/enterprises/ghuniverse1824-ea31). Participants should use their own organization and review settings without changing them.

## 1. Copilot access

1. Open your organization and select **Settings**.
2. Select **Copilot**, then **Access**.
3. Open the **Filter** dropdown and review the available options.
4. Open the **Get usage report** dropdown and review the options available to administrators.
5. Find the **Copilot Enterprise is active in your organization** setting and open its dropdown. Review **Disabled**, **All members**, and **Selected members**.
6. If access is active for **All members**, explain that everyone in the organization has Copilot access. The access management list below does not restrict access while all members are included.

## 2. Policies and features

1. In your organization settings, select **Copilot**, then **Policies**.
2. Scroll to **Features** and review the available settings and inherited permissions.
3. Review the policies for **Features**, **Clients**, **Agents**, and **MCP**, along with any other preview features available in your organization.
4. For each area, note which permissions are inherited and which can be set for the organization. Discuss which features your team can use and which controls an administrator can manage.

## 3. Audit log

1. In your organization settings, find **Logs** under **Archive**, then select **Audit Log**.
2. Set the date filter to `created:2026-10-07` for this review.
3. Search each action below to review the corresponding administrative changes:
   - `action:copilot` for Copilot policy and settings changes.
   - `action:business` for enterprise administrator changes.
   - `action:org` for organization administrator changes.
4. In the same audit log, search for access and membership events:
   - `action:copilot.cfb_seat_assignment_created` for new Copilot seat grants.
   - `action:copilot.cfb_seat_cancelled` for Copilot seat removals.
   - `action:team` for team membership changes that can drive seat assignment.
5. For each result, identify the **actor** who made the change and the **user** affected, when those fields are available.

## What to explain to Security

- **Access:** "I can review whether Copilot is disabled, available to all members, or limited to selected members. When all members have access, the access management list below is not limiting who can use Copilot."
- **Policies:** "I can see which Copilot features and clients are available, what permissions are inherited, and where administrators can set organization policies."
- **Policy history:** "The audit log helps us identify who changed Copilot policies or administrative settings and when."
- **User access history:** "Seat-assignment records show Copilot grants and removals, while team membership events help explain access changes driven by teams. The actor and affected user help us understand who made each change and who was impacted."

---

[← Previous exercise: Finance](e2-Finance.md) · [Workshop overview](../README.md)
