# Repository Updates - 2026-05-27

| # | Area | What was updated today | Outcome |
|---|---|---|---|
| 1 | Home metrics cleanup | Removed `Assigned to You` and `Overall Progress` from the Home summary card. | Eliminated non-SME workflow signals and reduced clutter. |
| 2 | Home layout balance | Refactored summary card layout into metric tiles and adjusted spacing so the right side is no longer empty after metric removal. | Card now looks visually balanced and intentional. |
| 3 | Context metadata | Added a small `Last updated` row under the metric tiles. | Added lightweight context without adding noise. |
| 4 | SME workflow alignment | Removed `Completed` from Home metrics, leaving `In Draft` and `Submitted`. | Matches SME-first process where approval is not part of their step. |
| 5 | Home CTA copy | Removed the sentence `You have 5 assets pending your review`. | Removed review-language mismatch for SME users. |
| 6 | Suggestion detail copy | Replaced `pending your review and approval` with `ready for your edits`. | Messaging now reflects editing/cleanup work. |
| 7 | Status label update | Changed `Submitted — awaiting approval` to `Submitted — sent`. | Removed approval dependency language. |
| 8 | UX improvement 1 | Added a `What to fix before submitting` checklist on Home (plain language, jargon removal, business meaning). | Gives SMEs concrete quality guidance before editing. |
| 9 | UX improvement 2 | Added `Needs Attention First` summary row and guidance in Explore. | Prioritizes high-value cleanup work first. |
| 10 | UX improvement 3 | Performed terminology pass from review/approval wording to cleanup/edit wording across major UI elements (header, nav, filters, badges, banners, buttons, alerts). | Consistent SME-first language throughout key flows. |
| 11 | Dynamic count | Made `Needs Attention First` count dynamic from currently visible filtered assets with status `partial`. | Count now reflects active filters/search in real time. |
| 12 | Dynamic helper note | Made the helper note under `Needs Attention First` dynamic with zero/singular/plural variants. | Users get contextual guidance that stays synced with the live count. |

## Updated file

- `SME-Dashboard-UX-Improved-v1.html`
