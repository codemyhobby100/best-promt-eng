# Senior AI Development Prompt Engineering Guide

*A comprehensive guide for senior software engineers building production-ready applications with AI development tools*

## Table of Contents
- [Introduction](#introduction)
- [Core Prompt Engineering Principles](#core-prompt-engineering-principles)
- [AI Tool-Specific Optimization](#ai-tool-specific-optimization)
- [System Architecture Prompts](#system-architecture-prompts)
- [Full-Stack Development Templates](#full-stack-development-templates)
- [Multi-Agent Workflows](#multi-agent-workflows)
- [Context Preservation Strategies](#context-preservation-strategies)
- [Testing & Quality Assurance](#testing--quality-assurance)
- [Performance & Scalability](#performance--scalability)
- [Production Deployment](#production-deployment)
- [Troubleshooting & Debugging](#troubleshooting--debugging)

## Introduction

This guide provides battle-tested prompt engineering strategies for senior developers building enterprise-grade applications using AI development tools like Cursor, Trae AI, Bolt.new, and v0.dev. Focus on creating maintainable, scalable, and production-ready solutions.

### Key Differences from Basic Prompt Guides
- **Production-First**: Every prompt template targets production-ready code
- **Context Persistence**: Strategies to maintain context across long development sessions
- **Multi-Agent Integration**: Leveraging specialized AI agents for testing, optimization, and validation
- **Enterprise Patterns**: Focus on scalable architecture and enterprise development practices

## Core Prompt Engineering Principles

### 1. The MASTER Framework
```
[M]odel Definition - Specify the exact type of application/component
[A]rchitecture Constraints - Define technical architecture and patterns
[S]cale Requirements - Specify performance and scalability needs
[T]esting Strategy - Define testing approach and coverage
[E]rror Handling - Outline error handling and edge cases
[R]equirements Specification - Detailed functional requirements
```

### 2. Context Anchoring Technique
Always start prompts with context anchors that prevent AI memory degradation:

```markdown
CONTEXT ANCHOR:
Project: [Your Project Name]
Architecture: [e.g., Next.js 14, TypeScript, PostgreSQL, Redis]
Current Phase: [e.g., Authentication System, Payment Integration]
Last Completed: [Brief description of last working feature]
Current Goal: [Specific feature being built]
```

### 3. Technical Specification Template
```markdown
TECHNICAL REQUIREMENTS:
- Framework: [Specific version]
- Database: [Type and version]
- Authentication: [Method and provider]
- State Management: [Library/pattern]
- Testing Framework: [Jest, Vitest, etc.]
- Deployment Target: [Platform/environment]
- Performance SLA: [Specific metrics]
```

## AI Tool-Specific Optimization

### Cursor IDE Prompts
```markdown
@codebase You are a senior full-stack engineer working on [PROJECT_NAME].

CURSOR-SPECIFIC INSTRUCTIONS:
- Reference existing codebase patterns and maintain consistency
- Use @files to reference related components
- Implement with TypeScript strict mode
- Follow existing project's ESLint/Prettier configuration
- Maintain current dependency versions unless upgrade required

TASK: [Specific development task]
FILES TO REFERENCE: [List relevant files with @]
PATTERNS TO FOLLOW: [Existing patterns in codebase]
```

### Bolt.new Optimization
```markdown
PROJECT INITIALIZATION PROMPT:
Create a production-ready [APP_TYPE] with the following architecture:

STACK SELECTION:
- Frontend: React 18 + TypeScript + Tailwind CSS
- Backend: Node.js + Express + TypeScript
- Database: PostgreSQL with Prisma ORM
- Authentication: NextAuth.js
- File Storage: AWS S3 compatible
- Real-time: Socket.io
- Testing: Jest + React Testing Library

IMMEDIATE SETUP REQUIREMENTS:
1. Complete TypeScript configuration
2. ESLint + Prettier setup
3. CI/CD workflow files
4. Docker containerization
5. Environment variable template
6. Database schema and migrations
7. Basic authentication flow
8. Error boundary implementation
```

### v0.dev Component Prompts
```markdown
COMPONENT SPECIFICATION:
Build a production-ready [COMPONENT_NAME] component for [USE_CASE].

DESIGN SYSTEM:
- Follow shadcn/ui design patterns
- Use consistent spacing scale (4, 8, 12, 16, 24, 32px)
- Implement proper TypeScript interfaces
- Include all accessibility attributes
- Support both light and dark themes

FUNCTIONALITY:
[Detailed component requirements]

TESTING REQUIREMENTS:
- Unit tests for all user interactions
- Integration tests for data flow
- Accessibility testing with axe-core
- Visual regression test setup
```

## System Architecture Prompts

### Microservices Architecture
```markdown
SYSTEM DESIGN PROMPT:
Design a scalable microservices architecture for [APPLICATION_TYPE].

ARCHITECTURE REQUIREMENTS:
- Service decomposition strategy
- API Gateway configuration
- Database per service pattern
- Event-driven communication
- Circuit breaker implementation
- Distributed logging and monitoring
- Container orchestration (Kubernetes)
- Service mesh integration (Istio/Linkerd)

SCALABILITY TARGETS:
- Handle [X] concurrent users
- 99.9% uptime SLA
- Sub-200ms API response times
- Auto-scaling capabilities
- Multi-region deployment

SECURITY REQUIREMENTS:
- OAuth 2.0 + OIDC implementation
- JWT token management
- Rate limiting and DDoS protection
- Data encryption at rest and in transit
- Security scanning integration
- Compliance requirements [GDPR/HIPAA/SOC2]

OUTPUT: Complete system architecture diagram, service definitions, and implementation roadmap.
```

### Database Design
```markdown
DATABASE ARCHITECTURE PROMPT:
Design an optimized database schema for [APPLICATION_DOMAIN].

PERFORMANCE REQUIREMENTS:
- Query response time < 100ms for 95th percentile
- Support [X] concurrent connections
- Read/write ratio: [X:Y]
- Data retention policy: [X years/months]

SCHEMA REQUIREMENTS:
- Normalized design with strategic denormalization
- Proper indexing strategy
- Foreign key constraints
- Audit trail implementation
- Soft delete patterns
- Data versioning for critical entities

SCALING STRATEGY:
- Read replica configuration
- Sharding strategy if needed
- Caching layer design (Redis)
- Backup and disaster recovery
- Migration strategy for schema changes

OUTPUT: 
1. Complete ERD with relationships
2. SQL migration scripts
3. Index optimization plan
4. Performance testing queries
```

## Full-Stack Development Templates

### SaaS Application Template
```markdown
SAAS APPLICATION PROMPT:
Build a production-ready SaaS application for [BUSINESS_DOMAIN].

FRONTEND ARCHITECTURE:
- Next.js 14 with App Router
- TypeScript strict mode
- Tailwind CSS with component library
- React Query for server state
- Zustand for client state
- React Hook Form with Zod validation
- Error boundaries and fallback UI

BACKEND ARCHITECTURE:
- Node.js with Express/Fastify
- TypeScript with strict configuration
- Prisma ORM with PostgreSQL
- Redis for caching and sessions
- AWS S3 for file storage
- WebSocket support for real-time features
- Bull queue for background jobs

AUTHENTICATION & AUTHORIZATION:
- NextAuth.js with multiple providers
- Role-based access control (RBAC)
- Team/organization management
- API key generation for third-party access
- Multi-factor authentication (MFA)

CORE SAAS FEATURES:
- Multi-tenant architecture
- Subscription management (Stripe)
- Usage tracking and billing
- Admin dashboard
- User onboarding flow
- Feature flagging system
- Analytics integration

INFRASTRUCTURE:
- Docker containerization
- Kubernetes deployment
- CI/CD with GitHub Actions
- Environment management
- Monitoring and logging
- Database migrations
- Backup strategies

TESTING STRATEGY:
- Unit tests (Jest + Testing Library)
- Integration tests (Supertest)
- E2E tests (Playwright)
- API testing (Postman/Newman)
- Performance testing (k6)
- Security testing (OWASP ZAP)

PERFORMANCE REQUIREMENTS:
- Core Web Vitals optimization
- Database query optimization
- CDN implementation for static assets
- Image optimization and lazy loading
- Code splitting and bundle optimization
- Server-side rendering for SEO

OUTPUT STRUCTURE:
1. Project initialization with all configurations
2. Database schema and migrations
3. Authentication system implementation
4. Core feature modules
5. Admin dashboard
6. API documentation
7. Deployment configurations
8. Testing suite setup
```

### E-commerce Platform Template
```markdown
E-COMMERCE PLATFORM PROMPT:
Develop a scalable e-commerce platform with [SPECIFIC_FEATURES].

CORE E-COMMERCE FEATURES:
- Product catalog with variants
- Inventory management
- Shopping cart and checkout
- Order processing workflow
- Payment gateway integration
- Shipping calculation
- Tax calculation by location
- Customer account management

ADVANCED FEATURES:
- Product recommendation engine
- Inventory tracking with low-stock alerts
- Multi-vendor marketplace support
- Wishlist and comparison tools
- Review and rating system
- Coupon and discount system
- Abandoned cart recovery
- Customer support chat

TECHNICAL IMPLEMENTATION:
- Microservices for cart, orders, payments, inventory
- Event sourcing for order states
- CQRS pattern for read/write separation
- Elasticsearch for product search
- Redis for session and cart storage
- PostgreSQL for transactional data
- MongoDB for product catalog
- RabbitMQ for async processing

PAYMENT & SECURITY:
- PCI DSS compliance
- Stripe/PayPal integration
- Fraud detection
- Secure payment tokenization
- SSL/TLS implementation
- Data encryption standards

PERFORMANCE & SCALE:
- CDN for product images
- Database read replicas
- Caching strategies (Redis, Memcached)
- Horizontal scaling capabilities
- Load balancing configuration
- Background job processing
```

## Multi-Agent Workflows

### Development Team Simulation
```markdown
MULTI-AGENT DEVELOPMENT WORKFLOW:

ARCHITECT AGENT:
"You are a senior software architect. Design the high-level system architecture, choose the tech stack, and define service boundaries. Focus on scalability, maintainability, and performance requirements."

BACKEND DEVELOPER AGENT:
"You are a senior backend developer. Implement robust APIs, database schemas, authentication systems, and business logic. Ensure proper error handling, validation, and security measures."

FRONTEND DEVELOPER AGENT:
"You are a senior frontend developer. Build responsive, accessible, and performant user interfaces. Implement state management, routing, and integrate with backend APIs."

DEVOPS AGENT:
"You are a senior DevOps engineer. Set up CI/CD pipelines, containerization, monitoring, logging, and deployment automation. Ensure infrastructure scalability and security."

QA ENGINEER AGENT:
"You are a senior QA engineer. Design comprehensive testing strategies, write automated tests, perform security assessments, and ensure quality standards."

WORKFLOW INTEGRATION:
1. Architect defines system design
2. Backend implements core services
3. Frontend builds user interface
4. DevOps sets up infrastructure
5. QA validates and tests
6. Iterate based on feedback
```

### Testing Agent Integration
```markdown
TEST SPRITE AGENT COLLABORATION:
Primary Development Agent: [Main implementation]
Test Sprite Agent: [Validation and testing]

HANDOFF PROTOCOL:
1. Primary agent implements feature
2. Test Sprite validates implementation
3. Test Sprite generates comprehensive test suite
4. Primary agent refines based on test feedback
5. Test Sprite performs final validation

TEST SPRITE PROMPT:
"You are an expert QA engineer working with Test Sprite. Analyze the provided code and:
1. Generate comprehensive test cases
2. Identify edge cases and boundary conditions
3. Create automated test scripts
4. Perform security vulnerability assessment
5. Validate performance requirements
6. Generate test data and fixtures
7. Provide detailed test reports"
```

## Context Preservation Strategies

### Session State Management
```markdown
SESSION CONTINUATION PROMPT:
PREVIOUS SESSION SUMMARY:
- Project: [Name and type]
- Completed Features: [List with status]
- Current Tech Stack: [Versions and configurations]
- Known Issues: [Active bugs or limitations]
- Next Priorities: [Planned features]

CURRENT SESSION GOALS:
- Primary Objective: [Specific goal]
- Success Criteria: [Measurable outcomes]
- Constraints: [Time, resource, or technical limits]

CONTEXT REFRESH:
[Paste relevant code snippets or configurations]

CONTINUATION REQUEST:
[Specific task for current session]
```

### Progressive Development Protocol
```markdown
DEVELOPMENT PHASE TRACKING:

PHASE 1: FOUNDATION
✅ Project setup and configuration
✅ Database schema design
✅ Authentication system
🔄 Currently working on: [Current feature]

PHASE 2: CORE FEATURES
⏳ [List of pending core features]

PHASE 3: ADVANCED FEATURES
⏳ [List of advanced features]

PHASE 4: OPTIMIZATION
⏳ Performance optimization
⏳ Security hardening
⏳ Production deployment

PROMPT ENHANCEMENT:
"Continue development from Phase [X]. Maintain all existing patterns and architectural decisions. Reference the current codebase structure: [Brief structure overview]"
```

## Testing & Quality Assurance

### Comprehensive Testing Prompt
```markdown
TESTING IMPLEMENTATION PROMPT:
Set up a comprehensive testing suite for [PROJECT_NAME].

TESTING PYRAMID:
1. Unit Tests (70%)
   - All business logic functions
   - Utility and helper functions
   - Component logic testing
   - Database model testing

2. Integration Tests (20%)
   - API endpoint testing
   - Database integration
   - External service mocking
   - Component integration

3. E2E Tests (10%)
   - Critical user journeys
   - Payment flows
   - Authentication flows
   - Core business processes

TESTING TOOLS SETUP:
- Jest for unit testing
- Supertest for API testing
- Playwright for E2E testing
- Testing Library for component testing
- MSW for API mocking
- Faker.js for test data generation

QUALITY GATES:
- 90%+ code coverage
- 0 critical security vulnerabilities
- Performance budgets met
- Accessibility standards (WCAG 2.1 AA)
- Cross-browser compatibility

AUTOMATED TESTING PIPELINE:
- Pre-commit hooks with linting
- PR validation with full test suite
- Staging environment testing
- Production smoke tests
- Performance regression testing
```

### Security Testing Protocol
```markdown
SECURITY VALIDATION PROMPT:
Implement comprehensive security measures for [APPLICATION_TYPE].

SECURITY CHECKLIST:
- Authentication & Authorization
  - JWT implementation with refresh tokens
  - Role-based access control
  - Multi-factor authentication
  - Session management
  - Password policies

- Data Protection
  - Input validation and sanitization
  - SQL injection prevention
  - XSS protection
  - CSRF tokens
  - Data encryption (at rest/in transit)

- API Security
  - Rate limiting implementation
  - API versioning strategy
  - Request/response validation
  - CORS configuration
  - API key management

- Infrastructure Security
  - HTTPS enforcement
  - Security headers
  - Dependency vulnerability scanning
  - Container security
  - Environment variable protection

SECURITY TESTING:
- OWASP ZAP automated scanning
- Penetration testing checklist
- Security regression tests
- Compliance validation (GDPR/HIPAA)
```

## Performance & Scalability

### Performance Optimization Prompt
```markdown
PERFORMANCE OPTIMIZATION PROMPT:
Optimize [APPLICATION_NAME] for enterprise-scale performance.

FRONTEND OPTIMIZATION:
- Code splitting and lazy loading
- Image optimization (WebP, AVIF)
- Critical CSS inlining
- Service worker implementation
- Bundle analysis and optimization
- Core Web Vitals optimization
- Memory leak prevention

BACKEND OPTIMIZATION:
- Database query optimization
- Connection pooling
- Caching strategies (Redis, CDN)
- API response compression
- Background job processing
- Database indexing strategy
- Query performance monitoring

SCALABILITY MEASURES:
- Horizontal scaling architecture
- Load balancing configuration
- Auto-scaling rules
- Database sharding strategy
- CDN implementation
- Microservices decomposition
- Event-driven architecture

MONITORING SETUP:
- Application Performance Monitoring (APM)
- Real User Monitoring (RUM)
- Infrastructure monitoring
- Error tracking (Sentry)
- Performance budgets
- Alerting thresholds
```

### Load Testing Protocol
```markdown
LOAD TESTING PROMPT:
Design and implement load testing for [APPLICATION_NAME].

TESTING SCENARIOS:
- Normal load: [X] concurrent users
- Peak load: [X] concurrent users
- Stress testing: [X] concurrent users
- Spike testing: Sudden load increases
- Volume testing: Large data sets
- Endurance testing: Extended periods

TESTING TOOLS:
- k6 for load testing scripts
- Artillery for complex scenarios
- JMeter for GUI-based testing
- Lighthouse CI for performance regression
- WebPageTest for real-world conditions

PERFORMANCE METRICS:
- Response time percentiles (50th, 95th, 99th)
- Throughput (requests per second)
- Error rate thresholds
- Resource utilization
- Database performance
- Memory usage patterns

LOAD TESTING IMPLEMENTATION:
[Specific requirements for your application]
```

## Multi-Agent Workflows

### Specialized Agent Coordination
```markdown
AGENT ORCHESTRATION STRATEGY:

PRIMARY DEVELOPMENT AGENT (Cursor/Bolt.new):
Role: Core application development
Responsibilities: Feature implementation, architecture decisions, code quality

TESTING AGENT (Test Sprite):
Role: Quality assurance and validation
Handoff Trigger: "Feature complete, ready for testing validation"
Responsibilities: Test generation, edge case identification, quality gates

SECURITY AGENT:
Role: Security analysis and hardening
Handoff Trigger: "Security review required for [component]"
Responsibilities: Vulnerability assessment, security best practices

PERFORMANCE AGENT:
Role: Optimization and scalability
Handoff Trigger: "Performance optimization needed"
Responsibilities: Code profiling, optimization recommendations

DEPLOYMENT AGENT:
Role: Infrastructure and deployment
Handoff Trigger: "Ready for production deployment"
Responsibilities: CI/CD setup, infrastructure configuration

HANDOFF PROTOCOL:
1. Clear context transfer with code snippets
2. Specific success criteria for each agent
3. Standardized response format
4. Integration testing between agent outputs
```

### Test Sprite Integration
```markdown
TEST SPRITE COLLABORATION PROMPT:
Transition to Test Sprite for comprehensive validation.

CONTEXT TRANSFER TO TEST SPRITE:
```
Project: [Name]
Technology Stack: [Current stack]
Recently Implemented: [Feature description with code snippets]
Test Requirements: [Specific testing needs]
Known Edge Cases: [Any identified edge cases]
Performance Requirements: [SLA requirements]
```

TEST SPRITE OBJECTIVES:
1. Generate comprehensive test suite
2. Identify missing test coverage
3. Create realistic test data
4. Validate error handling
5. Performance testing scenarios
6. Security vulnerability assessment
7. Accessibility compliance check

RETURN REQUIREMENTS:
- Test coverage report
- Identified issues with severity
- Recommendations for improvements
- Additional test scenarios needed
```

## Production Deployment

### Deployment Readiness Checklist
```markdown
PRODUCTION DEPLOYMENT PROMPT:
Prepare [APPLICATION_NAME] for production deployment.

PRE-DEPLOYMENT CHECKLIST:
- [ ] Environment configuration validated
- [ ] Database migrations tested
- [ ] SSL certificates configured
- [ ] Monitoring and logging setup
- [ ] Backup strategies implemented
- [ ] Security scanning completed
- [ ] Performance testing passed
- [ ] Load testing completed
- [ ] Disaster recovery plan
- [ ] Rollback procedures defined

INFRASTRUCTURE SETUP:
- Container orchestration (Docker + Kubernetes)
- Load balancer configuration
- Auto-scaling policies
- Health check endpoints
- Circuit breaker implementation
- Rate limiting configuration
- CDN setup for static assets

MONITORING & OBSERVABILITY:
- Application metrics (Prometheus/Grafana)
- Error tracking (Sentry)
- Log aggregation (ELK Stack)
- Uptime monitoring
- Performance monitoring
- Security monitoring
- Business metrics tracking

DEPLOYMENT STRATEGY:
- Blue-green deployment setup
- Canary release configuration
- Feature flag implementation
- Database migration strategy
- Cache warming procedures
- DNS failover configuration
```

## Troubleshooting & Debugging

### Debug Session Protocol
```markdown
DEBUGGING SESSION PROMPT:
Debug [SPECIFIC_ISSUE] in [APPLICATION_NAME].

ISSUE DESCRIPTION:
- Error Message: [Exact error text]
- Steps to Reproduce: [Detailed steps]
- Expected Behavior: [What should happen]
- Actual Behavior: [What actually happens]
- Environment: [Development/Staging/Production]
- Browser/Platform: [Specific details]
- User Impact: [Severity and affected users]

DEBUGGING APPROACH:
1. Log analysis and error tracking
2. Database query examination
3. Network request inspection
4. Performance profiling
5. Memory usage analysis
6. Security vulnerability check

CONTEXT PRESERVATION:
- Recent changes made
- Related components affected
- Current system state
- External dependencies
- Configuration changes

RESOLUTION REQUIREMENTS:
- Root cause identification
- Immediate fix implementation
- Prevention strategy
- Test case addition
- Documentation update
```

### Error Recovery Patterns
```markdown
ERROR RECOVERY IMPLEMENTATION:
Implement robust error handling for [COMPONENT/FEATURE].

ERROR HANDLING HIERARCHY:
1. Graceful degradation
2. User-friendly error messages
3. Automatic retry mechanisms
4. Fallback functionality
5. Error reporting and logging

IMPLEMENTATION PATTERNS:
- Try-catch with specific error types
- Error boundaries for React components
- API error response standardization
- Client-side error recovery
- Offline functionality fallbacks

MONITORING INTEGRATION:
- Error rate tracking
- Error categorization
- Alert thresholds
- User impact measurement
- Recovery success metrics
```

## Best Practices & Guidelines

### Code Quality Standards
```markdown
CODE QUALITY ENFORCEMENT:
Implement enterprise-grade code quality standards.

LINTING & FORMATTING:
- ESLint with TypeScript rules
- Prettier for code formatting
- Husky for pre-commit hooks
- lint-staged for incremental linting
- Custom ESLint rules for project-specific patterns

ARCHITECTURE PATTERNS:
- SOLID principles enforcement
- Clean architecture layers
- Dependency injection patterns
- Repository pattern for data access
- Command Query Responsibility Segregation (CQRS)

CODE REVIEW CHECKLIST:
- Business logic correctness
- Error handling completeness
- Performance implications
- Security considerations
- Testing coverage
- Documentation quality
```

### Documentation Standards
```markdown
DOCUMENTATION GENERATION PROMPT:
Generate comprehensive documentation for [PROJECT/FEATURE].

TECHNICAL DOCUMENTATION:
- API documentation (OpenAPI/Swagger)
- Database schema documentation
- Architecture decision records (ADRs)
- Code commenting standards
- Setup and installation guides

USER DOCUMENTATION:
- User guides and tutorials
- FAQ sections
- Troubleshooting guides
- Feature release notes
- Migration guides

MAINTENANCE DOCUMENTATION:
- Deployment procedures
- Monitoring runbooks
- Incident response procedures
- Backup and recovery processes
- Security procedures
```

## Usage Guidelines

### Prompt Optimization Tips
1. **Be Specific**: Always include exact versions, frameworks, and requirements
2. **Context First**: Lead with the most important context and constraints
3. **Iterative Refinement**: Use follow-up prompts to refine and improve
4. **Error Prevention**: Include error handling requirements upfront
5. **Testing Integration**: Always specify testing requirements

### Common Pitfalls to Avoid
- Vague requirements leading to generic solutions
- Missing error handling specifications
- Inadequate performance requirements
- Insufficient security considerations
- Poor context preservation across sessions

### Agent Switching Protocol
When switching between AI agents or tools:
1. **Export Context**: Save current state and progress
2. **Transfer Documentation**: Include relevant code snippets and decisions
3. **Specify Continuation**: Clear instructions for the next agent
4. **Validate Handoff**: Ensure the new agent understands the context

## Advanced Patterns

### Microservices Prompt Pattern
```markdown
MICROSERVICE DEVELOPMENT:
Develop [SERVICE_NAME] microservice for [BUSINESS_DOMAIN].

SERVICE SPECIFICATION:
- Bounded context: [Domain boundaries]
- API contract: [RESTful/GraphQL specification]
- Data ownership: [Database and schema]
- Dependencies: [External service dependencies]
- SLA requirements: [Performance and availability]

IMPLEMENTATION DETAILS:
- Framework: [Express, Fastify, NestJS]
- Database: [PostgreSQL, MongoDB, etc.]
- Caching: [Redis configuration]
- Message queuing: [RabbitMQ, Apache Kafka]
- Monitoring: [Prometheus metrics]
- Health checks: [Readiness and liveness probes]

DEPLOYMENT CONFIGURATION:
- Docker containerization
- Kubernetes manifests
- Service mesh integration
- Auto-scaling configuration
- Circuit breaker implementation
```

### Event-Driven Architecture
```markdown
EVENT-DRIVEN SYSTEM PROMPT:
Design an event-driven architecture for [SYSTEM_TYPE].

EVENT MODELING:
- Domain events identification
- Event schemas (JSON Schema/Avro)
- Event versioning strategy
- Event sourcing implementation
- CQRS pattern application

MESSAGING INFRASTRUCTURE:
- Message broker selection (Kafka, RabbitMQ)
- Topic/queue design
- Partitioning strategy
- Dead letter queue handling
- Message ordering guarantees

RELIABILITY PATTERNS:
- Exactly-once delivery
- Idempotent event handlers
- Saga pattern for distributed transactions
- Event replay capabilities
- Monitoring and alerting
```

## Conclusion

This guide provides a framework for professional-grade AI-assisted development. Remember to:
- Always specify exact technical requirements
- Implement proper error handling and testing
- Focus on production-ready, scalable solutions
- Use multi-agent workflows for complex projects
- Maintain context across development sessions
- Prioritize security and performance from the start

### Contributing
This guide is designed to evolve with AI development tools and best practices. Regular updates ensure continued effectiveness in professional development environments.

### Support
For questions or improvements to this guide, reference the latest AI development best practices and community standards.

---
*Last Updated: August 2025*
*Version: 2.0*
