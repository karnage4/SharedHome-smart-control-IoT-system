# Milestone 2 Step 2A Conceptual Design

## Purpose

This document translates the confirmed Milestone 1 findings and Step 1 requirements into provisional personas, scenarios, task flows, and information architecture. It does not invent participant quotations or behaviors that were not recorded. Features involving restriction explanations and access requests remain design hypotheses to be validated.

## Provisional personas

These are evidence-bounded personas based on the three directly interviewed participants. They can be expanded after the interview questions, observations, and quotations are documented.

### Persona 1 Murium the low-confidence household user

- **Age:** 60
- **Technology confidence:** Low
- **Context:** Uses household devices such as lights, AC, TV, and fans.
- **Known behavior:** Has difficulty navigating smart-home controls.
- **Primary goal:** Complete common household-control tasks without navigating a complicated interface.
- **Evidence-based need:** A small number of clearly labeled actions, visible device state, and predictable navigation.
- **Current evidence gap:** The precise controls, labels, or navigation steps that caused difficulty have not been recorded.

### Persona 2 Ayun the restricted child user

- **Age:** 10
- **Technology context:** Uses or encounters common household devices such as lights, AC, TV, and fans.
- **Known requirement:** Needs limits on which devices or actions he can control.
- **Primary goal:** Use allowed household controls safely and understand what is available.
- **Evidence-based need:** Role-based permissions that prevent disallowed actions without making allowed actions difficult to find.
- **Design hypothesis:** A plain-language explanation and an in-app access request may make restrictions easier to understand.
- **Research note:** The project record should state how parental consent or guardian permission was obtained for the direct child interview.

### Persona 3 Ramz the technically comfortable administrator

- **Technology confidence:** High
- **Context:** Does not report difficulty using IoT controls.
- **Primary goal:** Access complete device controls and manage household permissions efficiently.
- **Evidence-based need:** The full interface must remain efficient for a capable user rather than simplifying every role equally.
- **Design hypothesis:** A request inbox and narrowly scoped approval options may help the administrator manage other users' access.
- **Current evidence gap:** No administrator workload, permission-management problem, or response preference has yet been documented.

## Scenarios

### Scenario A Murium adjusts room comfort

Murium enters the smart-home interface to make the room more comfortable. The dashboard immediately shows the living-room AC and fan with their current states. She opens the AC control, changes the temperature, receives visible confirmation, and returns to the dashboard without navigating through settings or technical device information.

This scenario is grounded in Murium's navigation difficulty and the household's use of AC and fans. The exact temperature and room are illustrative prototype details, not interview findings.

### Scenario B Ayun encounters a restriction

Ayun opens the child dashboard and uses an allowed light control. He then attempts to open the restricted Wi-Fi settings. The interface prevents the action. In the proposed hypothesis flow, it also explains that the administrator manages Wi-Fi and offers a Request Access action.

The restriction is evidence-based. The explanation and request interaction must be tested in a follow-up interview before being described as participant needs.

### Scenario C Ramz reviews a request

The administrator receives a request showing the requester, Wi-Fi control, requested action, and time. The administrator approves it once, temporarily, permanently, or declines it. The system confirms the decision and updates Ayun's request status.

This is a proposed administrative workflow rather than a behavior established by the current interviews.

## Primary task flows

### Flow 1 Common device control for Murium

1. Open the app.
2. Enter the older-adult profile.
3. View the simplified dashboard.
4. Select AC, fan, light, or TV.
5. View the current device state.
6. Perform the primary action.
7. Receive immediate confirmation.
8. Return to the dashboard.

**Success condition:** Murium completes the action without entering settings, encountering an unclear icon, or needing help.

### Flow 2 Restricted action for Ayun

1. Open the app.
2. Enter the child profile.
3. View allowed and restricted device controls.
4. Select a restricted action.
5. See that the action is unavailable.
6. Read the proposed plain-language explanation.
7. Choose Request Access or return to the dashboard.
8. If requested, see a Pending status.

**Success condition:** Ayun does not complete the restricted action and can correctly explain what happened and what he can do next.

### Flow 3 Request resolution for Ramz

1. Open the administrator dashboard.
2. Notice a pending request indicator.
3. Open the request inbox.
4. Review who requested which device action.
5. Select an approval scope or decline the request.
6. Confirm the decision.
7. See the updated request state.

**Success condition:** Ramz resolves the intended request without accidentally granting broader or longer access than intended.

## Information architecture

```text
Prototype entry
|-- Select profile
|   |-- Administrator
|   |-- Older adult
|   `-- Child
|
|-- Role dashboard
|   |-- Lights
|   |-- AC
|   |-- Fans
|   |-- TV
|   |-- Wi-Fi hypothesis device
|   `-- Front door hypothesis device
|
|-- Device control
|   |-- Current state
|   |-- Primary control
|   `-- Result feedback
|
|-- Restricted action
|   |-- Restriction explanation
|   |-- Request access
|   `-- Request status
|
`-- Administrator requests
    |-- Request list
    |-- Request details
    |-- Allow once
    |-- Allow temporarily
    |-- Allow permanently
    `-- Decline
```

The profile selector exists to make the student prototype testable. A deployed household system could use accounts, device recognition, or another authentication method, but authentication is outside the current prototype scope.

## Navigation model

- Use a role-specific dashboard as the home screen.
- Let each device card open one focused control screen.
- Keep a persistent, clearly labeled Home action.
- For the simplified view, avoid deep navigation and advanced settings.
- For the child view, keep allowed controls visible and show restricted controls only when doing so helps explain the boundary.
- For the administrator, place pending requests directly on the dashboard rather than inside general settings.

## Screen inventory for wireframing

### Shared prototype screens

1. Profile selection
2. Role-specific dashboard
3. Light control and feedback
4. AC control and feedback
5. Fan control and feedback
6. TV control and feedback

### Hypothesis-flow screens

7. Restricted Wi-Fi and front-door controls
8. Restricted-action explanation
9. Request confirmation
10. Request status
11. Administrator request inbox
12. Administrator request details and decision
13. Decision confirmation

## Prototype states that must be represented

- Device on and off
- AC temperature before and after adjustment
- Fan speed before and after adjustment
- Wi-Fi and front-door controls restricted
- Action successful
- Action unavailable
- Request not sent, pending, approved, and declined
- Administrator request unread and resolved

## HCI principles guiding the wireframes

| Principle | Application in the conceptual design |
|---|---|
| Visibility of system status | Always show device state, command outcome, and request status. |
| Match with the real world | Use familiar device names and plain actions such as Turn on and Set temperature. |
| User control and freedom | Provide a clear Home or Back action and allow reversible changes where practical. |
| Consistency and standards | Keep device cards, labels, navigation, and feedback patterns consistent. |
| Error prevention | Disable or intercept restricted and unsafe actions before they change a device. |
| Recognition rather than recall | Keep common devices visible and label icons with text. |
| Flexibility and efficiency | Give the administrator fuller controls while keeping Murium's view focused. |
| Minimalist design | Remove nonessential settings and technical information from the simplified view. |

## Step 2B low-fidelity wireframe

The clickable low-fidelity mobile wireframe is implemented in `M2_wireframes.html`. It includes:

- Murium's simplified dashboard and device-control flow.
- Ayun's allowed controls, restricted-action explanation, request confirmation, and request-status flow.
- Ramz's administrator dashboard, request inbox, approval scope, and decision-feedback flow.
- Lights, AC, fans, and TV controls grounded in the participants' household device use.
- Wi-Fi and front-door controls included as explicit hypotheses for testing permission comprehension and safety boundaries.
- Visible device state, action feedback, consistent navigation, and large labeled controls.
- A review panel that identifies the purpose of each screen and provides direct entry to the three evaluation flows.

The wireframe intentionally uses grayscale styling so evaluation focuses on hierarchy, navigation, permissions, labels, and feedback before visual branding is introduced.

## Initial formative feedback

The role-adaptive prototype was reviewed with the project participants. They reported feeling somewhat more comfortable with the revised layouts, while also indicating that they still needed time to adapt. This is preliminary qualitative feedback rather than a completed usability evaluation because task completion, hesitation points, assistance, errors, timing, and exact quotations were not recorded.

The feedback provisionally supports retaining the distinct Administrator, Elder, and Child layouts. It also introduces a learnability requirement: future iterations should preserve stable control placement and use brief, plain-language guidance for unfamiliar permission and request features.

## Iteration 2 formative feedback

After role-specific Quick guides and clearer terminology were added, participants demonstrated faster learning and adaptation and completed tasks more quickly than in the first review. They also responded positively to the recognizable icons used with text labels. One participant characterized the prototype as a "convenient experience."

These are comparative qualitative findings because no numerical task times, participant-level outcomes, errors, or quotation attribution were recorded. They support retaining the role-adaptive layouts, stable device placement, brief contextual guidance, and icon-plus-label controls. They do not replace the quantitative and task-based evaluation required in Phase 3.

## Step 2 completion condition

Step 2 is ready for an initial design review when the three persona summaries, task flows, information architecture, and clickable wireframes reflect the interviews accurately. Findings from that review should be recorded as the first design iteration before moving to higher-fidelity prototyping.
