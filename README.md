# Amplitude Product Analytics Implementation

## Overview
This project is an end-to-end product analytics implementation built in a live environment. I created a responsive landing page, published it on Netlify, connected it to Amplitude, tracked key CTA interactions, validated the data, built a conversion funnel, and created a dynamic behavioural cohort.

- **Live site:** https://admirable-mochi-cb8665.netlify.app/
- **Loom walkthrough:** https://www.loom.com/share/c7de2c42e627415abe56a28e17b3d6de

## Tools
- HTML
- CSS
- JavaScript
- Amplitude Browser SDK
- Amplitude Live Events
- Amplitude Funnel Analysis
- Amplitude Cohorts
- Netlify

## Events
| Event | Trigger | Selected properties |
|---|---|---|
| `Landing Page Viewed` | Page load | `page_name`, `traffic_source` |
| `Sign Up Clicked` | Sign Up CTA click | `button_text`, `button_location`, `page_name` |
| `Request Demo Clicked` | Request Demo CTA click | `button_text`, `button_location`, `page_name` |

Amplitude Autocapture also recorded supporting events such as page views, element clicks, session starts, and web vitals.

## Funnel
**Landing Page Viewed -> Sign Up Clicked**

Configuration used in the final walkthrough:
- Events in order
- One-day conversion window
- Counted by unique users
- Last seven days

Final snapshot:
- 33 unique landing-page viewers
- 16 users clicked Sign Up
- 48.5% CTA click conversion

This figure measures CTA engagement, not completed registration. The demo did not include a full sign-up flow.

## Behavioural Cohort
**Sign-Up CTA Users**

Dynamic cohort definition:
- Performed `Sign Up Clicked`
- Count = 1
- Last seven days

Final snapshot: 14 users.

## Validation
I confirmed that events were received in Amplitude Live Events and checked the event properties to verify that they came from the public Netlify domain.

## Limitations
This was an assessment dataset generated through test activity, including separate browser sessions and invited testers. It validates the implementation but should not be treated as a production benchmark.

## Recommended Next Steps
- Extend the funnel to Form Started, Form Submitted, Account Created, and Onboarding Completed.
- Compare Sign Up and Request Demo engagement.
- Segment results by traffic source and device.
- Review Session Replay for users who did not click the primary CTA.
- Test CTA copy, placement, and supporting messaging.

## Resume Summary
**Amplitude Product Analytics Implementation | HTML, CSS, JavaScript, Amplitude, Netlify**
- Built and publicly deployed a responsive landing page with Sign Up and Request Demo CTAs, then implemented the Amplitude Browser SDK with Autocapture and Session Replay.
- Designed and validated custom events and properties for landing-page views and CTA clicks using Amplitude Live Events and public-domain checks.
- Created a unique-user conversion funnel and a dynamic behavioural cohort to analyse sign-up intent, while separating CTA engagement from completed registration.
