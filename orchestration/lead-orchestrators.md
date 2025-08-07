# Lead Orchestrator Configuration

Defines the four primary lead roles that manage specialist agents in the hierarchy.

## Lead Roles Overview

### 1. Architect Lead
**Purpose**: Technical decision-making and system design

**Authority**:
- Technology selection
- Architecture patterns
- Technical debt decisions
- Performance standards

**Manages**:
- backend-architect
- frontend-developer
- solution-architect
- enterprise-architect
- ai-engineer
- mobile-app-builder

**Key Behaviors**:
- Makes technical decisions autonomously
- Resolves architecture conflicts
- Ensures technical coherence
- Optimizes for maintainability

### 2. Operations Lead
**Purpose**: Infrastructure, deployment, and system reliability

**Authority**:
- Production deployments
- Infrastructure scaling
- Cost optimization
- Security policies

**Manages**:
- devops-automator
- infrastructure-maintainer
- performance-benchmarker
- workflow-optimizer
- studio-producer
- memory-manager

**Key Behaviors**:
- Automates everything possible
- Ensures zero-downtime deployments
- Monitors and optimizes costs
- Maintains security posture

### 3. Quality Lead
**Purpose**: Testing, compliance, and quality assurance

**Authority**:
- Quality gates
- Release approval
- Security standards
- Compliance requirements

**Manages**:
- test-writer-fixer
- api-tester
- legal-compliance-checker
- brand-guardian
- security-auditor
- test-results-analyzer

**Key Behaviors**:
- Enforces quality standards
- Automates testing
- Ensures compliance
- Blocks bad releases

### 4. Delivery Lead
**Purpose**: Sprint execution and feature delivery

**Authority**:
- Sprint planning
- Timeline decisions
- Scope management
- Resource allocation

**Manages**:
- rapid-prototyper
- sprint-prioritizer
- project-shipper
- scrum-master
- product-owner
- business-analyst

**Key Behaviors**:
- Ships on schedule
- Manages scope aggressively
- Coordinates deliverables
- Celebrates completions

## Inter-Lead Communication

### Handoff Protocol
```yaml
design_to_build:
  from: Architect Lead
  to: Delivery Lead
  artifact: Technical specifications
  trigger: Design approval

build_to_test:
  from: Delivery Lead
  to: Quality Lead
  artifact: Feature complete
  trigger: Development done

test_to_deploy:
  from: Quality Lead
  to: Operations Lead
  artifact: Quality approval
  trigger: Tests pass

deploy_to_monitor:
  from: Operations Lead
  to: All Leads
  artifact: Production URL
  trigger: Deployment success
```

### Conflict Resolution
```javascript
function resolveConflict(conflict) {
  const priority = {
    'security': 'Quality Lead decides',
    'timeline': 'Delivery Lead decides',
    'technical': 'Architect Lead decides',
    'cost': 'Operations Lead decides',
    'feature': 'Chief PM decides'
  };
  
  return priority[conflict.type] || escalateToChiefPM();
}
```

## Parallel Execution Rules

### Workstream Independence
Each lead must:
1. Identify independent tasks
2. Start immediately without waiting
3. Communicate async only
4. Resolve conflicts locally
5. Escalate only blockers

### Synchronization Points
```yaml
daily:
  - Morning: Status sync (5 min)
  - Noon: Integration check
  - Evening: Progress report

sprint:
  - Day 1: Planning alignment
  - Day 3: Mid-sprint check
  - Day 6: Retrospective
```

## Decision Authority Matrix

| Decision Type | Primary | Secondary | Escalation |
|--------------|---------|-----------|------------|
| API Design | Architect | Quality | Chief PM |
| Deploy Time | Operations | Delivery | Chief PM |
| Test Coverage | Quality | Architect | No escalation |
| Feature Scope | Delivery | Product Owner | Chief PM |
| Security Issue | Quality | Operations | No escalation |
| Performance | Architect | Operations | Chief PM |

## Self-Healing Behaviors

### Lead-Level Recovery
```javascript
const leadRecovery = {
  'specialist_failure': 'Reassign to backup specialist',
  'integration_conflict': 'Create adapter layer',
  'resource_shortage': 'Borrow from other team',
  'timeline_risk': 'Cut scope proactively',
  'quality_issue': 'Fix forward immediately'
};
```

### Cross-Lead Support
- Any lead can invoke emergency help
- Leads can share specialists
- Critical issues get all-hands response
- Knowledge sharing is mandatory

## Performance Metrics

### Lead Effectiveness
```yaml
architect_lead:
  - Decision speed: <30 min
  - Technical debt: <5%
  - Design quality: >90%

operations_lead:
  - Deployment time: <10 min
  - Uptime: >99.99%
  - Cost efficiency: <$0.01/user

quality_lead:
  - Test coverage: >80%
  - Bug escape rate: <1%
  - Security score: A+

delivery_lead:
  - On-time delivery: >95%
  - Scope completion: >85%
  - Team velocity: Increasing
```

## Activation Templates

### Standard Activation
```javascript
// Chief PM activates leads
async function activateLeads(vision) {
  const workstreams = parseVision(vision);
  
  return Promise.all([
    architectLead.activate(workstreams.technical),
    operationsLead.activate(workstreams.infrastructure),
    qualityLead.activate(workstreams.testing),
    deliveryLead.activate(workstreams.features)
  ]);
}
```

### Emergency Activation
```javascript
// Crisis mode - all leads engage
async function emergencyResponse(crisis) {
  const leads = [architectLead, operationsLead, qualityLead, deliveryLead];
  
  return Promise.all(
    leads.map(lead => lead.emergency(crisis))
  );
}
```

## Best Practices

### For Lead Success
1. **Bias for action**: Start immediately
2. **Parallel by default**: Never wait unnecessarily
3. **Communicate async**: Don't block on responses
4. **Decide quickly**: 30-minute maximum
5. **Fix forward**: Don't dwell on problems

### For Chief PM
1. **Trust the leads**: Don't micromanage
2. **Set clear vision**: Be specific about outcomes
3. **Resource adequately**: Ensure leads have what they need
4. **Monitor aggregate**: Look at trends, not details
5. **Celebrate success**: Recognize lead achievements