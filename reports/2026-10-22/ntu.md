# Nanyang Technological University (NTU) · usability audit · 2026-10-22

Pages read: home https://www.ntu.edu.sg/ (ok, HTTP 200, 205 ms, 156 KB) ·
admissions https://www.ntu.edu.sg/admissions (ok, HTTP 200, 208 ms, 140 KB)
robots.txt: rules read; both pages are allowed.

## Heuristics

| # | Heuristic | Severity | Evidence from the HTML |
|---|---|---|---|
| 1 | Visibility of system status | 1 | `home:breadcrumbs.present` = true; `admissions:breadcrumbs.present` = true; `home:navigation.aria_current_count` = 0; `admissions:navigation.aria_current_count` = 0; `home:headings.h1_count` = 0; `home:http.response_ms` = 205 |
| 2 | Match between system and the real world | 1 | `home:navigation.landmarks.0.top_level_links` = ["About Us", "Admissions", "Education", "Research", "Innovation", "Life at NTU", "Alumni"]; `home:navigation.landmarks.1.top_level_links` = ["Corporate NTU"]; `home:lang` = "en" |
| 3 | User control and freedom | 1 | `home:navigation.home_links` = 2; `home:breadcrumbs.present` = true; `home:carousel_or_slider_hints` = 19; `admissions:carousel_or_slider_hints` = 12; `home:autoplay_media` = 0; `home:skip_link.present` = false |
| 4 | Consistency and standards | 2 | `home:headings.h1_count` = 0; `admissions:headings.h1_count` = 0; `home:landmarks.main` = false; `admissions:landmarks.main` = false; `home:links.empty_text` = 6; `admissions:links.empty_text` = 1; `home:images.missing_alt` = 0; `home:forms.inputs_without_label` = 1 |
| 5 | Error prevention | 1 | `home:forms.inputs_without_label` = 1; `home:forms.unlabelled_with_placeholder_only` = 1; `admissions:forms.inputs_without_label` = 1; `admissions:forms.unlabelled_with_placeholder_only` = 1; `admissions:forms.inputs` = 38 |
| 6 | Recognition rather than recall | 0 | `home:navigation.landmarks.0.top_level_link_count` = 7; `home:links.vague_text_total` = 0; `admissions:links.vague_text_total` = 0; `home:search.search_input` = true; `admissions:search.search_input` = true; `admissions:breadcrumbs.present` = true |
| 7 | Flexibility and efficiency of use | 2 | `home:skip_link.present` = false; `admissions:skip_link.present` = false; `home:navigation.landmarks.0.links` = 303; `home:search.search_form` = true; `home:meta_viewport` = "width=device-width, initial-scale=1.0"; `home:scripts.external` = 6 |
| 8 | Aesthetic and minimalist design | not judged | not judged from HTML: layout and visual clutter cannot be seen in the HTML; indirect counts only: `home:navigation.landmarks.0.links` = 303; `home:visible_word_count` = 1437; `home:carousel_or_slider_hints` = 19 |
| 9 | Help users recognise, diagnose and recover from errors | not judged | not judged from HTML: no error states are on these pages; `home:forms.inputs_without_label` = 1 only bears on how error messages would be tied to labels |
| 10 | Help and documentation | 0 | `home:help_faq_contact_links` = ["Frequently Asked Questions", "Contact Us", "Contact Service Desk", "FAQs"]; `admissions:help_faq_contact_links` = ["Frequently Asked Questions", "Contact Us", "Contact Service Desk", "FAQs"]; `home:footer_contact.phone_pattern` = true; `home:footer_contact.postal_address_pattern` = true |

Severity: 0 no problem, 1 cosmetic, 2 minor, 3 major, 4 severe (see HEURISTICS.md). Lower is better.

## Three suggestions for the web team
1. **The page title area on both pages (no main heading) · Consistency and standards.** Both pages have no `h1` (`home:headings.h1_count` = 0) and no `main` landmark. Please add one `h1` and wrap the page content in `main`, so screen reader users can jump to the content.
2. **The site menu (303 links) · Flexibility and efficiency of use.** There is no skip link before the menu. Please add a "Skip to main content" link as the first focusable item, so keyboard users do not tab through 303 links on every page.
3. **The search box in the header · Error prevention.** One text field has no label and relies on its placeholder (`unlabelled_with_placeholder_only` = 1 on both pages). Please add a visible or screen-reader label so the purpose stays clear once someone types.

## Since last week
First audit; nothing to compare yet.

## Limits
Judged from the HTML of two pages only. Visual design, colour contrast and real tasks were not judged.
These findings are prompts for a human evaluator, not verdicts.
