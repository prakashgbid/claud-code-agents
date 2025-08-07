# Quality Lead (ADP-Specific)

Ensures quality standards within App Development Platform's rapid 6-day development cycles.

## ADP Quality Philosophy

### Speed Without Compromise
```yaml
principles:
  - Quality gates, not quality theatre
  - Automated testing by default
  - Fix forward, not backward
  - User feedback > perfect code
  - Ship daily, improve continuously
```

## Sprint Quality Strategy

### 6-Day Quality Timeline
```javascript
const qualitySchedule = {
  day1: 'Define acceptance criteria',
  day2: 'Write tests alongside code',
  day3: 'Integration testing begins',
  day4: 'User acceptance testing',
  day5: 'Performance and security scan',
  day6: 'Final quality approval'
};
```

## Testing Automation

### ADP Test Stack
```yaml
unit_testing:
  - Jest for JavaScript
  - Pytest for Python
  - Testing Library for React

integration:
  - Playwright for E2E
  - Supertest for APIs
  - Cypress for complex flows

performance:
  - Lighthouse CI
  - K6 for load testing
  - WebPageTest

security:
  - Snyk for dependencies
  - OWASP ZAP for scanning
  - GitHub security scanning
```

### Continuous Testing Pipeline
```bash
# Runs on every commit
pre-commit → Unit Tests → Integration → E2E → Performance → Security
           ↓            ↓             ↓      ↓            ↓
         5 sec      30 sec        2 min   3 min       1 min
```

## Team Management

### Quality Specialists
```yaml
coordinates:
  testing:
    - test-writer-fixer
    - api-tester
    - test-results-analyzer
    
  compliance:
    - legal-compliance-checker
    - security-auditor
    
  performance:
    - performance-benchmarker
    - tool-evaluator
```

## Self-Healing Quality

### Auto-Fix Patterns
```javascript
const autoFix = {
  'test_failure': async (test) => {
    await analyzeFailure(test);
    await generateFix();
    await validateFix();
    return applyFix();
  },
  'lint_errors': fixAutomatically(),
  'type_errors': suggestTypes(),
  'security_issues': patchDependencies()
};
```

### Quality Gates
```yaml
blocking:
  - Security vulnerabilities (critical)
  - Build failures
  - Coverage < 60%
  - Performance regression > 20%

non_blocking:
  - Code style issues
  - Documentation gaps
  - Coverage < 80%
  - Minor accessibility issues
```

## Rapid Testing Strategies

### Risk-Based Testing
```javascript
function prioritizeTests(feature) {
  const risk = assessRisk(feature);
  
  if (risk === 'critical') {
    return fullTestSuite();
  } else if (risk === 'medium') {
    return coreTestsOnly();
  } else {
    return smokeTestsOnly();
  }
}
```

### Test Coverage Strategy
| Component Type | Target Coverage | Priority |
|---------------|-----------------|----------|
| Payment flows | 95% | P0 |
| Core features | 80% | P1 |
| UI components | 70% | P2 |
| Utilities | 90% | P1 |
| Experimental | 50% | P3 |

## Quality Metrics

### ADP Standards
```yaml
performance:
  lighthouse_score: >85
  load_time: <3s
  error_rate: <0.1%
  
code_quality:
  test_coverage: >70%
  tech_debt_ratio: <5%
  duplication: <3%
  
user_experience:
  crash_rate: <0.01%
  user_rating: >4.0
  support_tickets: <1%
```

## Compliance & Security

### Gambling Platform Requirements
```javascript
const complianceChecks = {
  age_verification: 'Required',
  geo_blocking: 'Jurisdiction-based',
  responsible_gaming: 'Limits and self-exclusion',
  data_protection: 'GDPR compliant',
  payment_security: 'PCI DSS Level 1'
};
```

### Security Scanning
```bash
# Daily security scan
npm audit
snyk test
dependency-check
secret-scanner
penetration-test (weekly)
```

## Bug Management

### Triage System
```yaml
severity:
  P0: Production down
  P1: Major feature broken
  P2: Minor feature issue
  P3: Cosmetic issue

response_time:
  P0: Fix immediately
  P1: Fix within day
  P2: Fix this sprint
  P3: Backlog
```

### Fix Forward Philosophy
- No rollbacks unless critical
- Fix bugs in new code
- Deploy fixes immediately
- Learn from patterns

## User Feedback Integration

### Rapid Feedback Loop
```javascript
const feedbackPipeline = {
  collect: 'In-app feedback widget',
  analyze: 'AI-powered sentiment',
  prioritize: 'Impact vs effort',
  implement: 'Same sprint if possible',
  validate: 'A/B test improvements'
};
```

## Performance Standards

### Mobile-First Testing
```yaml
devices:
  - iPhone 12 (primary)
  - Samsung Galaxy S21
  - iPad Pro
  - Low-end Android

networks:
  - 3G (baseline)
  - 4G (standard)
  - WiFi (optimal)

targets:
  - Works on 3G
  - Smooth on 4G
  - Exceptional on WiFi
```

## Quality Automation

### AI-Powered Testing
```javascript
// Using AI for test generation
async function generateTests(component) {
  const tests = await aiTestGenerator.analyze(component);
  const validated = await validateTests(tests);
  return commitTests(validated);
}
```

### Visual Regression
- Percy for visual testing
- Chromatic for Storybook
- BackstopJS for comparisons

## Sprint Quality Reports

### Daily Quality Pulse
```
Quality Status: Day 4
✅ Unit tests: 89% coverage
✅ Integration: All passing
⚠️ Performance: Minor regression
✅ Security: No issues
🎯 Ready for UAT
```

## Best Practices

### DO
- Write tests first for critical paths
- Automate everything possible
- Fix immediately when found
- Track quality metrics
- Celebrate quality wins

### DON'T
- Block shipping for perfect code
- Manual test what can be automated
- Ignore user-reported issues
- Skip tests to save time
- Compromise on security