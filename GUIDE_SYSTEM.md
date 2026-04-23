# 🎯 Global Guide Generator Skill System

## Quick Start

Simply ask for a guide on any topic:

```
Generate guide for Kubernetes
Generate guide for Redis Caching
Generate guide for gRPC with context: performance, protobuf, service mesh
```

That's it! I'll create a comprehensive learning guide with:
- Executive summary (5-minute read)
- Junior developer view
- Senior developer view
- Architect view
- Pros & cons
- Best practices
- Real-world examples
- Learning resources

## How It Works

### 1. You Request
```
Generate guide for [TOPIC]
Context: [optional additional info]
```

### 2. I Research
- Official documentation
- Best practices
- Common pitfalls
- Real-world usage
- Alternatives & comparisons

### 3. I Create
A comprehensive HTML guide at `/guides/[topic].html` with:
- Navigable table of contents
- Code examples (✅ good vs 🚨 bad)
- Color-coded callout boxes
- Comparison tables
- Responsive design

### 4. You Learn
- From 3 perspectives (junior/senior/architect)
- Quick reference or deep dive
- Production-ready patterns
- Debugging strategies

## Guide Structure

### 📋 Executive Summary (Top of Page)
- One-liner definition
- When to use it
- Best for: [skill level]
- Key metrics
- 5-minute read

### 👨‍💻 How Junior Developers Use It
- Basic starting patterns
- First 3 things to learn
- Common mistakes (🚨 marked)
- Simple working examples
- What NOT to do

### 👨‍💼 How Senior Developers Use It
- Advanced patterns
- Performance optimization
- Debugging strategies
- Monitoring setup
- Production considerations
- When to use carefully vs avoid

### 🏛️ How Architects Think About It
- System design implications
- Trade-offs vs alternatives (table)
- Scalability analysis
- Cost implications
- When to choose this vs competitors
- Long-term maintenance

### ✅ Benefits & Pros
- Concrete advantages with examples
- Real-world use cases
- Performance improvements

### ❌ Pitfalls & Cons
- Critical mistakes (❌ danger boxes)
- Common gotchas (⚠️ warning boxes)
- When NOT to use it
- Complexity warnings

### 🛠️ Best Practices & Guardrails
- Production-ready patterns
- Safety measures
- Testing strategies
- Monitoring & observability
- Error handling

### 💡 Real-World Examples
- 3-4 practical implementations
- Complete, runnable code
- Different use case scenarios

### 📚 Learning Resources
- Related topics
- Official documentation
- Recommended articles
- Tools and libraries

## Request Types

### Framework/Library
```
Generate guide for Spring Data JPA
Context: Database queries, N+1 problems, lazy loading
```

### Architecture Pattern
```
Generate guide for Event Sourcing
Context: CQRS, event replay, versioning
```

### Infrastructure/DevOps
```
Generate guide for Docker
Context: Networking, container orchestration, debugging
```

### Language Feature
```
Generate guide for Java Generics
Context: Type bounds, wildcards, PECS principle
```

### Debugging Topic
```
Generate guide for Memory Leaks in Java
Context: GC analysis, heap dumps, profiling
```

### Operational Topic
```
Generate guide for Database Connection Pooling
Context: HikariCP, performance tuning, deadlocks
```

## File Organization

```
/learning-hub/
├── index.html                          # Home page
├── guides/
│   ├── index.html                     # Guides hub (all guides listed here)
│   ├── kubernetes.html                # Generated guides
│   ├── redis-caching.html
│   ├── cqrs-pattern.html
│   └── ...
├── spring-boot/
│   ├── index.html
│   └── retryable.html
├── payments/
│   ├── index.html
│   └── juspay-architecture.html
└── java/
    └── (coming soon)
```

## Memory System Reference

All skill configuration is stored in memory at:

```
~/.claude/projects/.../memory/
├── SKILL_USAGE.txt                  # Quick reference (this)
├── guide_generator_skill.md         # How to use the system
├── guide_generation_prompt.md       # Research requirements & template
├── spring_boot_guide_template.md    # Spring Boot guide structure
└── payments_learning_path.md        # Payment systems guides
```

## Usage Examples

### Simple Request
```
Generate guide for Kafka
```

### Request with Context
```
Generate guide for RabbitMQ
Context: Message queues, pub-sub patterns, reliability
```

### Request with Focus Areas
```
Generate guide for Spring Cloud
Focus: Service discovery, load balancing, configuration management, circuit breaker
```

### Request for Specific Use Case
```
Generate guide for GraphQL
Context: API design, N+1 problems, subscription handling, caching strategies
```

## What Makes These Guides Different

✅ **Multi-Level Learning**
- Junior: Gets practical starting point
- Senior: Gets optimization techniques
- Architect: Gets design thinking

✅ **Production-Ready**
- Includes debugging strategies
- Monitoring setup explained
- Guardrails for production use
- Common failure modes covered

✅ **Quick Scanning**
- Executive summary at top
- 5-minute quick read available
- Clear section breaks
- Bullet points and tables for scanning

✅ **Comprehensive**
- All three perspectives covered
- Code examples for every major point
- Real-world examples included
- Related topics listed

## Styling

Every guide uses consistent styling:
- 🟢 Success boxes for best practices
- 🟡 Warning boxes for cautions  
- 🔴 Danger boxes for critical mistakes
- 📋 Info boxes for important concepts

Code examples:
- ✅ GOOD: Proper implementation
- 🚨 BAD: Anti-patterns to avoid

## Tips for Best Results

1. **Be specific about context** if it's niche or specialized
2. **Mention focus areas** if you want deep dives in certain areas
3. **Tell me the framework** if it's framework-specific (Spring Boot, Node.js, etc)
4. **Ask for debugging focus** if you need troubleshooting help
5. **Request architect view** if you want design trade-offs

## Integration with Learning Hub

All guides are:
- Linked from main hub at `/guides/index.html`
- Organized by category
- Cross-referenced with related topics
- Saved permanently for team access
- Version-controlled in git

## Next Steps

Ready to learn something new?

Just say:
```
Generate guide for [TOPIC]
```

Examples:
- "Generate guide for Kubernetes"
- "Generate guide for Redis Caching"
- "Generate guide for CQRS Pattern"
- "Generate guide for Docker Networking"
- "Generate guide for Microservices Architecture"

And you'll get a comprehensive, multi-perspective learning guide!

---

**Built for continuous learning and team knowledge sharing** 💙
