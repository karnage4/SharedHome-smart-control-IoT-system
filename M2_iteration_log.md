# SharedHome Prototype Iteration Log

## Purpose and evidence convention

This log records how SharedHome changed from the first low-fidelity concept through the current prototype. Each iteration links the relevant persona and scenario to the design decision, HCI purpose, available review evidence, remaining limitation, and reason for continuing to the next iteration.

The following evidence labels are used throughout:

- **Interview supported:** grounded in the direct interviews with Ramz, Murium, or Ayun.
- **Review supported:** observed or reported during a prototype review, subject to the stated recording limitations.
- **Design hypothesis:** a proposed solution that has not yet been established as a participant need.
- **Baseline usability requirement:** a conventional interaction or accessibility requirement that was not derived from a particular interview statement.

Wi-Fi and the front door remain hypothesis devices. Lights, air conditioning, television, and fans are grounded in the participants' reported household-device use.

## Personas and continuing scenarios

| Persona | Evidence-based characteristic | Continuing scenario | Design concern |
|---|---|---|---|
| Murium, age 60 | Low confidence with technology and difficulty navigating smart-home controls | Turn on a room fan or light and adjust comfort without entering settings | Complexity, learnability, readable controls, autonomy without stereotyping |
| Ayun, age 10 | Requires limits on the controls available to him | Use an allowed device, understand a restriction, and request temporary access | Safety, explanation, permission comprehension, meaningful next actions |
| Ramz, administrator | Technically comfortable and does not report difficulty with IoT controls | Review a request and grant only the intended access | Efficiency, decision clarity, least-privilege approval, low administrative burden |

## Iteration trail summary

| Iteration | Prototype | Main design question | Outcome | Reason to continue |
|---|---|---|---|---|
| 0 | `Iteration 0.html` | Can the three persona scenarios be represented as understandable task flows? | Established the low-fidelity information architecture and permission journey | Needed a more compact, realistic prototype that could demonstrate cross-role state changes |
| 1 | `Iteration 1.html` | Do role-specific layouts make the system more comfortable and manageable? | Participants felt somewhat more comfortable, but still needed time to adapt | Learnability and terminology needed improvement; task evidence was not measured |
| 2 | `Iteration 2.html` | Do contextual guidance, stable placement, and icon-plus-label controls improve adaptation? | Qualitatively faster learning, adaptation, and completion; positive response to icons and a "convenient experience" comment | Role-based layouts alone have limited novelty; adaptive autonomy and permission comprehension still require stronger design and evaluation |
| 3, planned | Next prototype | Can transparent adaptation balance accessibility, autonomy, safety, and learning? | Not yet implemented or evaluated | Will test the proposed PACE model and record measurable task evidence |

## Iteration 0 Low-Fidelity Task-Flow Baseline

### Prototype purpose

`Iteration 0.html` was the initial clickable grayscale wireframe. Its purpose was to translate the Milestone 1 interviews and conceptual design into testable navigation, device-control, restriction, request, and approval flows before applying visual branding.

The grayscale presentation deliberately directed attention toward hierarchy, labels, navigation, permissions, and feedback rather than appearance.

### Persona and scenario coverage

- **Murium:** A simplified dashboard with large labeled device cards and focused controls for lights, AC, fan, and television. Her primary scenario was adjusting the AC without navigating through settings.
- **Ayun:** An allowed-versus-restricted dashboard. His primary scenario was encountering a restricted television control, reading the explanation, confirming a temporary-access request, and seeing its status.
- **Ramz:** A complete device dashboard and request inbox. His primary scenario was reviewing Ayun's request and selecting Allow once, Allow for 1 hour, Always allow, or Decline.

### What was introduced and why

| Change or feature | Evidence status | Why it was introduced | HCI purpose fulfilled |
|---|---|---|---|
| Three persona-specific entry points | Interview supported | The participants differed in confidence and permitted actions | Flexibility and efficiency; reduced cognitive load |
| Large, labeled cards with visible state | Interview supported plus accessibility baseline | Murium needed a less complicated route to common devices | Recognition over recall; visibility; accessible target sizing |
| One focused device-control screen | Design response | Avoid settings-heavy navigation for common actions | Minimalist design; match with the real world |
| Visible restricted controls for Ayun | Interview supported restriction; presentation was a hypothesis | Prevent unsafe action without making the boundary invisible | Error prevention; visibility of system status |
| Plain-language restriction explanation and Request access | Design hypothesis | Provide a next action rather than a dead end | Help with recognition and recovery; user control |
| Request confirmation and status | Design hypothesis | Prevent ambiguous requests and repeated submissions | Error prevention; feedback |
| Scoped administrator approval | Design hypothesis | Avoid granting broader or longer access than intended | Informed decision-making; reversibility; least privilege |

### What Iteration 0 fulfilled

- Demonstrated all three end-to-end scenarios in one prototype.
- Made device state and action feedback visible.
- Distinguished interview-grounded devices from the proposed permission interaction.
- Established the information architecture later reused by the higher-fidelity prototypes.
- Provided review prompts for next-action clarity, state visibility, restriction comprehension, and approval scope.

### What Iteration 0 could not establish

- It did not show whether the participants preferred explanations, requests, or approval scopes; those remained hypotheses.
- It used separate multi-screen flows and did not clearly demonstrate a shared live state across personas.
- Its grayscale wireframe format limited conclusions about icon recognition, visual comfort, or the realism of everyday use.
- It did not record participant task times, errors, assistance, hesitations, or standardized usability ratings.
- It used personal names in system messages, which later created ambiguity between the participant, project member, and administrator role.

### Reason for Iteration 1

Iteration 1 was needed to turn the task-flow proof of concept into a more compact and realistic mobile interaction. It retained the three scenarios while allowing the team to demonstrate that a request created in the Child view appears in the Administrator view and that an approval changes the Child view.

## Iteration 1 Role Adaptive Prototype Review

### Prototype reviewed

The first formative review used the SharedHome clickable web prototype. It presented three role-adaptive views:

- An Elder view with fewer choices, larger controls, and optional progressive disclosure.
- A Child view with allowed devices and visibly locked higher-consequence controls.
- An Administrator view with complete device controls, access settings, and a request inbox.

### Changes from Iteration 0

1. Replaced the separate role-selection and multi-screen wireframe journey with a compact role switcher for classroom demonstration and rapid testing.
2. Introduced shared prototype state so device changes, requests, approvals, and one-time access could be observed across roles.
3. Changed Murium's view to a small set of immediate room controls with optional More controls progressive disclosure.
4. Presented Ayun's allowed and locked devices together as recognizable tiles with text state.
5. Added Wi-Fi and the front door as explicit higher-consequence hypothesis devices for permission and safety scenarios.
6. Brought requests, device state, Ayun's access, and Murium's view settings into the Administrator dashboard.
7. Moved from grayscale wireframes to a visually clearer phone-like interface with icons, state styling, and larger controls.

These changes tested whether role adaptation could operate as one household system rather than three disconnected mock-ups. They supported visibility of system status, progressive disclosure, recognition over recall, and flexibility for novice and experienced users.

### Evidence status of prototype devices

Lights, AC, TV, and fans are grounded in the participants' reported household-device use.

Wi-Fi and the front door are intentional hypothesis devices. They were added because they create understandable, higher-consequence permission scenarios. They allow the team to test whether users notice a restriction, understand who controls it, request access successfully, and distinguish temporary from permanent approval. They must not be described as devices identified through the initial interviews.

### Participants and procedure

The project participants reviewed the prototype after the role-specific layouts were introduced. The available record does not yet state which tasks each participant completed, the session date, session duration, whether assistance was needed, or whether parental consent was documented for Ayun's participation.

### Feedback received

Participants felt somewhat more comfortable with the revised interface. However, they still needed time to adapt to the new layouts and interactions.

No exact quotation, numerical rating, task-completion time, error count, or hesitation count was recorded. The finding should therefore be reported as preliminary qualitative feedback rather than proof of improved usability.

### Interpretation

The improved comfort suggests that tailoring information density and control size by role is a promising design direction. The continued adaptation time indicates a learnability issue: changing the interface can initially slow users even when the resulting layout is simpler.

This feedback does not independently validate every hypothesis feature. In particular, it does not yet show whether users understood the locked-control explanation, preferred an in-app request, or correctly interpreted approval scopes.

### Decisions retained

1. Keep distinct Administrator, Elder, and Child layouts.
2. Keep the Elder view focused on a small set of room-level controls.
3. Keep large, labeled device controls and visible device state.
4. Keep restricted Child controls visible and clearly labeled rather than silently hiding them.
5. Keep Wi-Fi and the front door as hypothesis devices for permission and safety testing.
6. Keep the request inbox with Once, 1 hour, Always, and Deny decisions.

### Changes proposed for Iteration 2

1. Preserve device-card positions between sessions so participants can build familiarity.
2. Add brief first-use guidance explaining that locked items can be selected to see why they are restricted.
3. Keep permission explanations short and name the responsible role.
4. Make the result of a request or approval visible in both the Child and Administrator views.
5. Record task-level observations instead of relying only on overall impressions.

### Next review tasks

1. Murium turns on her room fan without assistance.
2. Murium reveals More controls and adjusts the room temperature.
3. Ayun selects Wi-Fi, explains why it is locked, and sends a request.
4. The administrator identifies the request and grants access for one hour.
5. Ayun returns to Wi-Fi and identifies the updated access state.

For every task, record completion, assistance, errors, hesitation points, completion time, and one short follow-up response about what felt clear or confusing.

### Iteration 1 conclusion

Iteration 1 supports continuing with role-adaptive layouts, but it does not yet establish that the prototype is easy to learn. Iteration 2 should focus on learnability, permission comprehension, and observable task performance.

## Iteration 2 Learnability Improvements

### Changes implemented

1. Added a short, dismissible Quick guide tailored to the Administrator, Elder, and Child views.
2. Explained the main action and unfamiliar permission behavior without presenting a long tutorial.
3. Replaced the inconsistent personal administrator name with the generic household administrator role throughout requests and help messages.
4. Added modal semantics and keyboard focus when a locked-control explanation opens.
5. Added Escape-key dismissal for the locked-control dialog.
6. Preserved the location, size, and meaning of the existing device controls so returning users can build familiarity.

### HCI justification

- The Quick guide supports learnability while keeping information close to the relevant role context.
- Dismissible guidance applies progressive disclosure and user control instead of forcing repeated instructions.
- Stable device placement supports recognition and spatial learning.
- Consistent administrator terminology reduces ambiguity between a project-team member and the administrator persona.
- Dialog focus and keyboard dismissal strengthen accessibility and user control.

### Validation needed

Iteration 2 should be tested with the same five tasks listed above. Compare assistance, errors, hesitation, and completion time with the first review where possible. Ask each participant whether the Quick guide was useful, unnecessary, or unclear, and record their exact wording.

### Iteration 2 feedback received

Participants showed faster learning and adaptation when using the revised prototype. Task completion was also faster than in the previous review. The use of recognizable icons alongside text labels was received positively, and one participant described the result as a "convenient experience."

No numerical completion times, participant-level results, error counts, or speaker attribution for the quotation were provided. The results therefore support a qualitative comparison with Iteration 1 but should not be reported as a measured performance improvement.

### Interpretation of Iteration 2

- Faster adaptation provisionally supports the short, contextual Quick guides and stable control placement.
- Faster completion provisionally supports the simplified role-specific information architecture.
- Positive feedback on icons supports recognition over recall because users can combine a familiar symbol with a written label.
- The phrase "convenient experience" indicates positive perceived usability, although it is not a standardized usability score.

### Iteration 2 conclusion

The second iteration improved perceived learnability, efficiency, and convenience compared with the first review. The role-adaptive design, icon-plus-label presentation, and brief first-use guidance should be retained in the higher-fidelity prototype. A later formal evaluation should collect task times, success rates, errors, assistance, and a standardized usability measure to test these observations quantitatively.

## Novelty Review After Iteration 2

### Review question

The mandatory review question was: **What is novel about SharedHome, and how would it remain meaningfully different if an existing smart-home application added role-specific interfaces?**

### Current novelty limitation

Role-based permissions, simplified dashboards, device icons, and time-limited access are not individually strong novelty claims. Current commercial systems already contain some related capabilities:

- [Google Home household permissions](https://support.google.com/assistant/answer/9155535?hl=en) distinguish Administrator and Member access and apply additional limits to child accounts.
- [Apple Home guest access](https://support.apple.com/en-gw/guide/iphone/iphcbaf7e8f3/27/ios/27) can restrict guests to selected security accessories and scheduled times.

Therefore, SharedHome should not claim that profiles, parental restrictions, or temporary permissions were invented by this project. Its proposed contribution is the integration of interface complexity, action authority, explanation, and learning support for a multigenerational household.

The current prototype still treats Administrator, Elder, and Child as mostly fixed categories. This can overgeneralize age and role, especially if every older adult is assumed to require the same simplified interface. It also cannot yet demonstrate that the interface adapts to changing confidence, context, or risk.

### Reframed contribution

The proposed novelty for Iteration 3 is a **transparent capability- and context-adaptive interaction model**:

> SharedHome changes both what a household member may control and how that control is presented, based on the person, action risk, context, and experience. Restrictions and adaptations remain visible, understandable, and user-controlled.

This is recorded as a design direction and research hypothesis, not as a proven novelty or participant requirement.

### Proposed PACE adaptation model

| Dimension | Question | Example in SharedHome |
|---|---|---|
| Person | What are this person's preferences, accessibility needs, and authority? | Murium prefers Guided mode; Ayun has limited authority; Ramz manages permissions |
| Action risk | What could happen if this action is performed incorrectly? | A light is low risk; Wi-Fi is moderate risk; unlocking the front door is high risk |
| Context | When, where, and under what conditions is the action requested? | Wi-Fi for one hour during homework; door access only when an adult is present |
| Experience | How familiar and successful is the person with this task? | First use receives guidance; repeated successful use can trigger an optional shortcut suggestion |

PACE would determine:

- The controls and information presented.
- The amount of guidance provided.
- Whether confirmation or administrator approval is required.
- The permitted action and its duration.
- The feedback, explanation, and expiry information shown afterward.

### Why this is different from automatic interface change

SharedHome should not rearrange itself silently. An adaptive system that unexpectedly moves controls can damage spatial learning and user trust. The proposed model is therefore **mixed initiative**:

1. The system may recommend an adaptation.
2. It explains why the recommendation appeared.
3. The user accepts, rejects, or reverses it.
4. Essential controls retain stable placement.

The contribution is the transparent interaction loop and its evaluation with the three household personas, rather than a claim that no other application can ever reproduce an individual feature.

## Iteration 3 Research and Design Backlog

All entries below are proposed hypotheses until they are implemented and evaluated.

### Priority 1 User-controlled complexity modes

Replace the age-labeled Elder mode with user-selectable interface levels such as:

- **Basic:** Essential controls with minimal information.
- **Guided:** Essential controls plus contextual help and explanations.
- **Full:** Complete device controls and settings permitted for that user.

The system may recommend a different mode after repeated use, but the user must approve the change. This supports user control and freedom, progressive disclosure, flexibility and efficiency, consistency, and recognition over recall. It also reduces the risk of age-based stereotyping.

**Murium scenario:** After she completes the fan task successfully several times, SharedHome offers to add fan speed to her home screen. The existing fan tile does not move, and she can decline or undo the suggestion.

### Priority 2 Explainable permission card

Every locked action should answer:

1. Why is this restricted?
2. Who manages the restriction?
3. What can the user do next?
4. If access is approved, when will it expire?

This extends the existing locked-control dialog with clearer policy information. It supports visibility of system status, match with the real world, help and recovery, and trust through transparency.

**Ayun scenario:** Wi-Fi explains that the household administrator manages it, offers a homework access request, and shows the remaining time after approval.

### Priority 3 Person-device-action-time permissions

Approval should describe the smallest usable scope rather than only a general role:

- Ayun may control his room light at any time.
- Ayun may use Wi-Fi for one hour.
- Ayun may view the front-door state but may not unlock it.
- A front-door unlock request requires an adult confirmation.

The administrator should see the person, device, requested action, duration, risk level, and result before confirming. This supports error prevention, informed decision-making, reversibility, and least-privilege access.

**Ramz scenario:** When reviewing a front-door request, SharedHome recommends a narrower alternative and clearly distinguishes View status from Unlock door.

### Priority 4 Guidance that responds to learning

Guidance should change gradually rather than appearing once for every user:

- First attempt: step-by-step help.
- Developing familiarity: short contextual hint.
- Repeated success: help remains available but is not shown automatically.

Success thresholds must be explicit in the prototype and should not be described as intelligent learning unless actual behavior data are recorded. This supports learnability, minimalist design, recognition, and flexibility for novice and experienced use.

### Priority 5 Multimodal and language preferences

Future versions may offer English or Urdu, scalable text, stronger contrast, audio confirmation, and optional voice input. Important security actions should still require an explicit confirmation. These features require direct validation with the participants and should not be added merely on the assumption that a particular age group or language preference needs them.

Relevant older-adult smart-home research emphasizes customization, meaningful presentation, participant co-design, and avoiding ageist assumptions. See the open-access [smart-home interface co-design study](https://pmc.ncbi.nlm.nih.gov/articles/PMC10334717/).

## Proposed Iteration 3 Scope

To keep the next prototype feasible and evaluable, Iteration 3 should implement the first three priorities and a small simulation of the fourth:

1. Rename the fixed Elder view to a user-selected Basic, Guided, or Full experience while retaining Murium as the evaluation persona.
2. Add an adaptation suggestion with an explanation, Accept, Not now, and Undo.
3. Expand locked-control explanations to include reason, decision owner, available next action, and access expiry.
4. Replace broad approvals with person-device-action-time summaries and a visible risk level.
5. Simulate first-use, developing, and familiar guidance states without claiming that machine learning is operating.
6. Keep icons with labels, stable device placement, visible state, role-aware access, and keyboard-accessible dialogs from Iteration 2.

English/Urdu switching, voice interaction, audio confirmation, and automatic behavior inference should remain stretch goals until the core PACE interaction has been tested.

## Iteration 3 Research Questions

### Primary question

Does transparent adaptation based on person, action risk, context, and experience improve task performance and permission understanding without reducing user autonomy?

### Supporting questions

- Can Murium choose and change an appropriate complexity level without assistance?
- Does the adaptation suggestion feel helpful rather than patronizing or unpredictable?
- Can Ayun explain why an action is restricted, who controls it, what he can request, and when approved access expires?
- Can Ramz distinguish the requested action from broader device access and grant the intended duration?
- Do users notice and understand the risk difference between lights, Wi-Fi, and the front door?
- Can every user reverse an interface adaptation or permission decision where reversal is safe?

## Iteration 3 Evaluation Plan

| Persona and task | Success evidence | Experience question |
|---|---|---|
| Murium selects Guided mode, turns on the fan, responds to a suggested shortcut, and reverses it | Task success, time, errors, assistance, correct use of Accept or Not now and Undo | Did the adaptation feel helpful, understandable, and under her control? |
| Ayun selects Wi-Fi, explains the restriction, requests one hour, and identifies the expiry | Correct explanation of why, who, next action, and duration; no unsafe action | Did the restriction feel understandable and fair rather than like a dead end? |
| Ramz reviews Wi-Fi and front-door requests and grants the narrowest intended permission | Correct person, device, action, duration, and risk recognized before approval | Was the recommendation useful, and did it reduce or add administrative effort? |

For each task, record the session date, participant, completion result, time, errors, assistance, hesitation points, chosen mode or permission, and one attributed quotation. Use a standardized usability instrument only if permitted by the course methodology, and keep its result separate from qualitative comments.

## Known Limitations Carried Into Iteration 3

- The participant sample remains limited to three people in one household context.
- Ramz is both a team member and participant, which may introduce response bias.
- The earlier reviews lack numerical baseline task times, errors, and participant-level outcomes.
- The exact speaker of "convenient experience" was not recorded.
- The record still needs the interview date, exact questions, recruitment details, and documentation of guardian consent for Ayun.
- PACE is currently a proposed framework created for this course project; it has not been established as a validated general smart-home model.
- Wi-Fi and the front door remain test scenarios, not devices identified in the original interviews.
- Adaptation based on repeated success will initially be simulated and must not be presented as a deployed AI system.
