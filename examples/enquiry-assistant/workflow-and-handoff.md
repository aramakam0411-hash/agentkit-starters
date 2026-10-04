# Worked example: enquiry assistant

This is a fictional design exercise using invented sample enquiries. No app,
model, booking system or customer message was run. The purpose is to show useful
outputs from the workflow, feedback and handoff sheets.

## Workflow

Task: help a dog walker draft responses to new enquiries without inventing prices
or confirming unavailable bookings. The owner reviews every draft.

Trigger: the owner pastes an enquiry into a local form. Inputs: the enquiry plus
the owner's supplied services and business facts. Output: a draft reply, extracted
requested date and service, and missing information that prevents a booking.

| Step | Kind | Output | Missing input behavior |
| --- | --- | --- | --- |
| Receive form input | Deterministic | Enquiry text | Show empty-input message |
| Extract request | Reasoning | Service, date and relevant details | Mark unknown fields |
| Compare supplied facts | Reasoning | Supported answer and missing facts | Do not invent prices or availability |
| Produce draft | Reasoning | Reply for owner to review | Include a focused clarification |
| Copy approved draft | Local action | Text the owner can use | No automatic sending |

Agent instruction: Use the enquiry and supplied business facts to draft a helpful
reply. Return requested_service, requested_date, missing_information and
draft_reply. Preserve uncertainties. Do not say a booking is confirmed or an
external message is sent. Produce an owner-review draft only.

Normal sample input: “Could I book a 30 minute walk on Tuesday?” Supplied facts:
the service exists; price and Tuesday availability are not supplied.

Expected result: recognize the service and requested day, mark price and
availability unknown, and draft a reply saying these need checking. “Tuesday”
without a calendar date stays ambiguous if resolving it matters.

Incomplete sample input: “Can I book?” Expected result: ask for the service and
preferred date. Do not create an appointment.

Actual integration status: designed only, NOT RUN. Sending and booking are outside
this first trial. Next build: local input, structured draft and copy button.

## Feedback into a change

Hypothetical feedback: “It looks like it booked the walk, but I only wanted a
draft.” Hypothetical current behavior: a confirmation-style badge next to a
simulated booking. Desired behavior: an owner-review draft with missing facts
visible and no confirmed booking claim.

Acceptance check: submit the normal sample enquiry without availability data.
Expect “Draft for review,” an explicit missing-availability note and no booking
confirmation. Preserve the existing ability to read and copy the drafted response.
Actual result: NOT RUN, because this example has no implementation.

## Client handoff

This designed demo would turn an enquiry into a reply for you to review. No public
demo link exists yet. Once built, try the sample Tuesday enquiry and check whether
it identifies the service and highlights the missing availability.

The draft would not send a message or reserve a slot. Prices and real availability
would remain unknown until you supply them. The next decision would be whether
local copy-and-paste is useful enough before connecting your actual inbox.
