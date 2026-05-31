# Accessibility Checklist (WCAG 2.1 AA)

## Perceivable
- [ ] All images have alt text
- [ ] Color contrast ratio >= 4.5:1 (text)
- [ ] Color not used as sole indicator
- [ ] Text resizable to 200%
- [ ] Content adapts to zoom

## Operable
- [ ] All interactive elements keyboard accessible
- [ ] Focus order is logical
- [ ] Focus indicators visible
- [ ] No keyboard traps
- [ ] Skip navigation link present
- [ ] Touch targets >= 44x44px

## Understandable
- [ ] Language attribute on HTML
- [ ] Form labels associated with inputs
- [ ] Error messages are descriptive
- [ ] Consistent navigation across pages
- [ ] Error prevention for important submissions

## Robust
- [ ] Valid HTML (no errors in validator)
- [ ] ARIA roles used correctly
- [ ] ARIA labels for dynamic content
- [ ] Works with screen readers (VoiceOver, NVDA)
- [ ] Works with browser zoom (200%)

## Testing Tools
- axe DevTools (browser extension)
- Lighthouse Accessibility audit
- WAVE (Web Accessibility Evaluation)
- Color contrast analyzers
- Screen reader testing (VoiceOver/NVDA)
