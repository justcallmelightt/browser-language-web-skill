---
name: browser-language-web
description: Build or improve a multilingual website that follows browser language preferences while respecting explicit URLs and the visitor's own language choice. Use for locale detection, language switchers, and bilingual web pages; not for translating prose alone.
---

# Browser Language Web

Implement the user's requested languages in the existing website. First inspect its framework, routes, content, translation setup, and current language controls. Reuse the project's conventions rather than adding a new i18n library by default.

## Language decision

- Establish supported locales and a documented fallback. Do not infer that every device language has a translation.
- On first visit, read the browser's ordered language preferences (`navigator.languages`, with `navigator.language` as a fallback) and choose the first supported language. Match language subtags deliberately, such as `en-US` to `en` when appropriate.
- Use this precedence when those inputs exist: valid explicit URL locale, visitor's saved manual choice, supported browser preference, fallback locale. An invalid URL locale must not accidentally override the others.
- Preserve an explicit locale while navigating between pages. A manual switch should persist across pages and future visits. Do not store the auto-detected locale as if the visitor selected it; browser settings may change.
- Handle unavailable storage without breaking navigation. Avoid redirect loops and preserve unrelated URL parameters and fragments.

## Complete the website

- Translate all visible interface copy for the requested scope, including titles, metadata, labels, placeholders, error and empty states, buttons, help text, and dynamic messages. Identify untranslated strings rather than claiming completion from a translated header.
- Set the document `lang` to the active locale. Make the language switch keyboard accessible, visibly indicate its destination or current choice, and maintain sensible focus and route behavior.
- Avoid a flash of the wrong language when the project's rendering model supports early locale selection. For server-rendered sites, use request language information where available and keep server and client decisions consistent.
- Keep dates, numbers, and pluralization locale aware when the site displays them. Use the platform's internationalization APIs or the project's existing formatter.
- Preserve the current design and functionality; change only what the language feature requires.

## Finish

Check first visit with Korean, English, and an unsupported browser language; explicit URL override; saved manual choice; navigation; reload; storage failure; and narrow screens. Verify that the actual rendered pages use the chosen language and report any copy or routes still awaiting translation.
