# Lifeline Mobile Polish Design

Date: 2026-07-01

## Goal

Make the Lifeline static site feel like a deliberate mobile/tablet version of the desktop design. The work should fix the visible mobile problems without redesigning the whole site or changing the desktop experience.

## Scope

In scope:

- Mobile layout polish for viewports up to 560px.
- Small tablet layout improvements up to 860px where they improve continuity from desktop to mobile.
- Logo asset cleanup so the header/footer logo does not appear as a white rectangle on cream or frosted backgrounds.
- Hero layout adjustment so the first screen feels unified and centered, closer to the desktop composition.
- About placeholder adjustment so "Φωτογραφία σύντομα" does not read as empty scroll space.
- Visual QA screenshots at mobile, tablet, and desktop widths.

Out of scope:

- Full content rewrite.
- New sections or new business functionality.
- Desktop redesign.
- Netlify/domain deployment changes unless requested separately.

## Design Direction

The mobile design should keep the desktop identity: clean clinical spacing, white and cream surfaces, red accent, restrained typography, and a premium diagnostic-lab feel. Mobile should not become a separate simplified theme. It should feel like the same site translated to a smaller screen.

## Logo Strategy

The current `LOGO - new logo.JPG` is a low-resolution JPEG with a white background. On mobile scroll states, the header becomes cream/frosted, making the logo look like a pasted white box.

The implementation should create a transparent logo asset from the existing logo and use that asset where the visible page chrome needs transparency, especially header and footer. The original JPEG can remain available for metadata/favicon/social image unless a better replacement is needed.

If the transparent extraction shows rough edges because the source is only 204x102, CSS should support the result with careful sizing and header spacing instead of making the logo too large.

## Hero Layout

On mobile, the hero should regain a full first-screen structure using modern viewport units such as `100svh`. The content should be vertically balanced below the fixed header, not pushed too high. The scroll into the next section should feel natural, without a visible dead zone or abrupt gap.

Hero typography and buttons should remain compact enough for 390px screens, with readable line height and stable button wrapping. The hero should not introduce horizontal overflow.

## About Placeholder

The about image placeholder should become shorter and more intentional on mobile. It should read as a designed media placeholder, not a large empty block. On tablet, the placeholder should keep a controlled aspect ratio so the section does not feel heavy before the text.

## Tablet Treatment

For tablet widths, keep the layout closer to desktop where possible: comfortable spacing, stable header behavior, and section rhythm that does not jump suddenly from desktop to mobile. Tablet changes should be minimal and only applied where the current breakpoint creates awkward spacing or oversized blocks.

## Verification

Before completion, verify with screenshots at:

- 390px mobile.
- 430px mobile.
- 768px tablet.
- Desktop sanity check.

Check specifically:

- Header logo has no visible white box.
- Hero fills and balances the first viewport.
- Scroll from hero to about feels continuous.
- About placeholder is not excessive on mobile.
- No text overlap or horizontal overflow.
- Desktop remains visually unchanged except for any intentional logo asset reference that still renders correctly.
