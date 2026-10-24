# Milestone 2 Step 1 Design Requirements

## Project direction

The project will explore a role-aware smart-home mobile interface for households in which people have different technical abilities and access needs. The initial prototype will support three roles: an administrator, an older adult represented by 60-year-old participant Murium, and a child represented by 10-year-old participant Ayun. The design goal is to reduce unnecessary interface complexity while keeping restricted actions safe and understandable.

This is a working Phase 2 document. It separates findings supported by the current interviews from design hypotheses that still need validation.

## Evidence available from Milestone 1

- Ramz is a technically comfortable user who reported that he does not struggle with IoT controls.
- Murium is 60 years old, was directly interviewed, is not very comfortable with technology, and has difficulty navigating smart-home controls.
- Ayun is 10 years old, was directly interviewed, and requires limits on the controls available to him. The exact interview question and his wording about restrictions are not yet documented.
- The participants use ordinary household devices including lights, air conditioning, televisions, and fans.
- A first formative review of the role-adaptive prototype produced generally improved comfort, although participants still needed time to become familiar with the changed layouts.
- After adding role-specific guidance and preserving stable control placement, participants showed faster learning, adaptation, and task completion. They responded positively to the icon-plus-label design, and one participant described it as a "convenient experience." Numerical task times, error counts, and participant attribution for the quotation were not recorded.
- The sample is exploratory and contains only three household participants. The interview date, recruitment details, parental consent procedure, interview questions, tasks, and direct quotations are not yet documented.

## Evidence to design chain

| ID | User problem or finding | Evidence status | Design requirement | HCI rationale | Design decision | Prototype feature |
|---|---|---|---|---|---|---|
| DR1 | Household members have different levels of technical confidence. | Supported by the contrast between Ramz and Murium. | The system shall present role-appropriate levels of interface complexity. | Flexibility and efficiency of use; cognitive load reduction. | Use the same underlying system with different views rather than one dense interface for everyone. | Administrator, older-adult, and child home views. |
| DR2 | Murium has difficulty navigating smart-home controls. | Supported by the interview summary, but specific navigation failures are not documented. | The older-adult view shall prioritize essential actions and minimize choices per screen. | Recognition rather than recall; minimalist design; reduced cognitive load. | Show a small set of common devices with familiar labels, clear status, and direct actions. | Simple home dashboard with Lights, Temperature, and TV cards. |
| DR3 | An older or less technical user may struggle with small or ambiguous controls. | Reasonable accessibility requirement; not directly measured in the interview. | Primary actions shall be visually clear, consistently placed, and easy to select. | Visibility, consistency, accessible interaction, and error prevention. | Use large touch targets, text labels with icons, strong contrast, and immediate state feedback. | Large on and off controls, readable device status, and confirmation feedback. |
| DR4 | Ayun requires limits on what he can control. | Supported by a direct interview with 10-year-old Ayun, although his exact wording is not documented. | The system shall restrict child access to selected devices and actions. | Error prevention and safe exploration. | Apply permissions by role and device rather than hiding the entire smart-home system. | Child dashboard with allowed devices and visibly unavailable restricted actions. |
| DR5 | A restricted user may not understand why an action is unavailable. | Design hypothesis; not yet supported by the current interviews. | When an action is restricted, the system should explain the restriction in plain language. | Visibility of system status; help users recognize and recover from problems. | Replace silent failure with a brief reason and the responsible role. | Restricted-action screen explaining why the control is unavailable. |
| DR6 | A restricted user may need a low-friction way to ask for a change. | Design hypothesis; not yet supported by the current interviews. | The system should let a restricted user request access without leaving the interface. | User control and freedom; clear feedback; reduced dependence on memory and outside communication. | Add a request action with a confirmation and visible request status. | Request Access button and Pending, Approved, or Declined status. |
| DR7 | The administrator needs to preserve safety while responding to household requests. | Derived from the proposed role model; requires validation with an administrator. | The administrator shall be able to review and resolve access requests with clear scope. | Error prevention, informed decision-making, and reversibility. | Show who requested what and allow narrowly scoped approval. | Admin request inbox with Allow once, Allow temporarily, Decline, and optional permanent permission controls. |
| DR8 | Users need to know whether a device command succeeded. | Baseline interaction requirement. | Every device action shall produce immediate and understandable feedback. | Visibility of system status and feedback. | Update the device state and show a brief result message after an action. | State change, progress indicator when needed, and success or failure message. |
| DR9 | Participants initially needed time to adjust, but the revised prototype produced faster learning, adaptation, and completion. | Supported by comparative qualitative feedback across two formative iterations; not yet quantified through recorded task times, error rates, or a usability scale. | The interface shall support gradual learning without changing the location or meaning of common controls between sessions. | Consistency and standards; recognition rather than recall; learnability. | Preserve stable device-card placement and provide brief first-use guidance for unfamiliar permission features. | Consistent dashboards, plain action labels, and short guidance for locked controls and requests. |
| DR10 | Participants responded positively to the use of recognizable device symbols. | Supported by Iteration 2 qualitative feedback. | Device controls shall pair recognizable icons with explicit text labels and state information. | Recognition rather than recall; visibility; accessible redundant coding. | Keep icons as supporting cues without requiring users to interpret an icon by itself. | Icon, device name, and current state presented together on each device control. |

## Functional requirements for the first prototype

### Core requirements

1. The user can enter or switch between administrator, older-adult, and child profiles for demonstration purposes.
2. Each role sees a dashboard suited to its permissions and expected level of complexity.
3. The older-adult view provides direct control of a small number of common devices.
4. The child view prevents selected unsafe or disallowed actions.
5. The interface shows current device state and the outcome of every attempted action.

### Hypothesis features to validate before treating them as findings

1. A restricted action explains why it is blocked.
2. A restricted user can send an access request.
3. The administrator can approve once, approve temporarily, approve permanently, or decline.
4. The requester can see whether the request is pending, approved, or declined.

## Interaction and accessibility requirements

- Use plain, familiar device names and action labels.
- Pair icons with text rather than relying on icons alone.
- Keep primary actions consistent across device screens.
- Use readable text, strong contrast, and generous touch targets.
- Avoid placing essential information behind gestures or unlabeled controls.
- Prevent accidental high-impact actions and make reversible changes easy to undo.
- Do not use color as the only indicator of device state, permission, or request status.

## Recommended prototype scope

To keep the prototype feasible and evaluable, the first version should be a mobile interface using devices that the participants already encounter at home:

- Lights for a simple, low-risk control task.
- Temperature or air conditioning for a value-adjustment task.
- Fans for a simple speed-adjustment task using familiar household equipment.
- TV or media controls for a child-restriction scenario.

Security devices such as door locks should remain outside the first prototype unless the study specifically focuses on safety-critical interaction.

### Hypothesis devices for permission testing

Wi-Fi and the front door will be retained as intentional hypothesis devices. They were not listed among the household devices reported in the initial interviews, so they must not be presented as interview findings. They are included because they create clear, higher-consequence permission scenarios that can reveal whether users understand locked states, explanations, access requests, approval scope, and safety boundaries.

## Candidate evaluation tasks

These tasks will guide the prototype structure and later Phase 3 evaluation:

1. Older-adult task: turn on a room light and change the temperature.
2. Child task: attempt to open restricted Wi-Fi or front-door controls, understand the restriction, and request access.
3. Administrator task: review the request and grant limited access.

## Information needed to finalize Step 1

- The specific navigation problems Murium encountered.
- The exact interview questions and any participant wording that was recorded.
- The interview date and recruitment details.
- Confirmation that parental consent or guardian permission was obtained for Ayun's direct participation.
- Whether participants said they wanted explanations or an in-app request process when blocked.
- Which participants completed each prototype task, where they hesitated, and whether they required assistance.
- Any task-completion times, errors, preference ratings, or exact feedback wording from the formative review.

## Step 1 completion condition

Step 1 is complete when the team confirms the prototype platform, device scope, role definitions, and which hypothesis features will be tested in a short follow-up interview. The next step is the conceptual design: personas, scenarios, task flows, information architecture, and low-fidelity wireframes.
