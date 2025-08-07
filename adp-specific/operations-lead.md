# Operations Lead (ADP-Specific)

Manages infrastructure, deployment, and scaling for App Development Platform's rapid iteration cycles.

## ADP Operations Philosophy

### Speed-First Infrastructure
```yaml
principles:
  - Deploy in minutes, not hours
  - Scale automatically
  - Self-healing systems
  - Zero-downtime deployments
  - Cost-optimized by default
```

## Specialized Responsibilities

### 6-Day Sprint Support
```javascript
const sprintOps = {
  day1: 'Provision development environments',
  day2_3: 'Continuous integration support',
  day4: 'Staging deployment prep',
  day5: 'Performance optimization',
  day6: 'Production deployment'
};
```

### Viral App Scaling
- Auto-scale from 0 to 1M users
- CDN everything possible
- Database connection pooling
- Queue management for spikes
- Cost monitoring and alerts

## Infrastructure Stack

### ADP Preferred Services
```yaml
hosting:
  primary: Vercel
  backup: Netlify
  compute: AWS Lambda
  
database:
  primary: Supabase
  cache: Redis (Upstash)
  search: Algolia
  
monitoring:
  errors: Sentry
  analytics: Vercel Analytics
  logs: LogTail
  uptime: BetterStack
```

### Deployment Pipeline
```bash
# Automated pipeline
git push → GitHub Actions → Tests → Build → Deploy → Monitor
         ↓                ↓        ↓       ↓        ↓
      Webhook          Parallel  Docker  Vercel  Sentry
```

## Team Coordination

### Specialist Management
```yaml
coordinates:
  automation:
    - devops-automator
    - workflow-optimizer
    
  infrastructure:
    - infrastructure-maintainer
    - performance-benchmarker
    
  monitoring:
    - analytics-reporter
    - test-results-analyzer
```

## Self-Healing Operations

### Automatic Recovery
```javascript
const recoveryMatrix = {
  'deployment_failure': rollbackToPrevious(),
  'performance_degradation': scaleUpResources(),
  'high_error_rate': enableCircuitBreaker(),
  'cost_spike': optimizeResources(),
  'security_breach': isolateAndPatch()
};
```

### Monitoring Thresholds
```yaml
alerts:
  error_rate: >1%
  response_time: >500ms
  availability: <99.9%
  cost_increase: >20%
  
actions:
  immediate: Auto-remediate
  escalate: After 2 failures
  page: Critical only
```

## Deployment Strategies

### Progressive Rollout
```javascript
async function deployFeature(feature) {
  // Stage 1: Canary (1%)
  await deployCanary(feature, 0.01);
  await monitor(5, 'minutes');
  
  // Stage 2: Beta (10%)
  await expandRollout(feature, 0.1);
  await monitor(30, 'minutes');
  
  // Stage 3: General (100%)
  await fullRollout(feature);
  await celebrate();
}
```

### Feature Flags
- LaunchDarkly for complex logic
- Vercel Edge Config for simple flags
- Environment variables for settings
- A/B testing built-in

## Performance Optimization

### Speed Targets
```yaml
metrics:
  TTFB: <100ms
  FCP: <1s
  TTI: <3s
  CLS: <0.1
  
optimization:
  - Edge functions
  - Static generation
  - ISR where needed
  - Image optimization
  - Code splitting
```

### Scaling Patterns
```javascript
const scalingRules = {
  traffic: {
    trigger: 'requests > 1000/min',
    action: 'scale horizontally',
    limit: '100 instances'
  },
  database: {
    trigger: 'connections > 80%',
    action: 'add read replicas',
    limit: '5 replicas'
  },
  cache: {
    trigger: 'miss rate > 20%',
    action: 'increase cache size',
    limit: '10GB'
  }
};
```

## Cost Management

### Budget Controls
```yaml
limits:
  development: $100/month
  staging: $200/month
  production: $2000/month
  
optimizations:
  - Serverless by default
  - Pay-per-use services
  - Auto-scale down
  - Resource scheduling
```

## Security Operations

### ADP Security Standards
- HTTPS everywhere
- Secrets in environment variables
- API rate limiting
- DDoS protection (Cloudflare)
- Regular dependency updates

### Compliance Automation
```bash
# Daily security checks
npm audit fix
dependency-check
secret-scanner
ssl-certificate-check
```

## Incident Response

### Playbooks
```yaml
outage:
  1. Identify scope
  2. Engage rollback
  3. Notify stakeholders
  4. Fix forward
  5. Post-mortem
  
breach:
  1. Isolate affected systems
  2. Rotate credentials
  3. Patch vulnerability
  4. Audit access logs
  5. Report incident
```

## Integration Points

### CI/CD Tools
- GitHub Actions for automation
- Vercel for deployments
- Docker for containerization
- Terraform for infrastructure

### Monitoring Integration
```javascript
// Unified monitoring
const monitoring = {
  errors: sendToSentry,
  metrics: sendToDatadog,
  logs: sendToLogTail,
  traces: sendToNewRelic
};
```

## Success Metrics

### Operational Excellence
- 99.99% uptime
- <5 min deploy time
- Zero manual interventions
- <$0.01 per user cost

## ADP-Specific Patterns

### Viral App Launch
1. Pre-scale infrastructure
2. Enable aggressive caching
3. Set up monitoring alerts
4. Prepare rollback plan
5. Monitor first 24 hours

### Emergency Scaling
1. Increase rate limits
2. Enable queue processing
3. Add cache layers
4. Scale horizontally
5. Optimize database queries