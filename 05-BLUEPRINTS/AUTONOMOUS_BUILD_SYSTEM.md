# AUTONOMOUS BUILD SYSTEM BLUEPRINT

**Version:** 1.0.0
**Status:** Active
**Owner:** Meta-Orchestrator
**Created:** 2026-01-07
**Purpose:** Self-building automation architecture with iterative improvement cycles

---

## EXECUTIVE SUMMARY

This blueprint defines a closed-loop automation system where:
1. Tasks are delegated to the most capable platform
2. Completion is verified and logged
3. Outputs feed into the next build cycle
4. Each cycle improves delegation accuracy and reduces human intervention

**Target State:** Human provides intent → System builds, deploys, monitors, and improves autonomously.

---

## ARCHITECTURE OVERVIEW

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                           LAYER 0: HUMAN INTENT                              │
│                    (Natural language goal/requirement)                       │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                      LAYER 1: META-ORCHESTRATOR                              │
│                                                                              │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐        │
│  │   Claude    │  │   Claude    │  │   ChatGPT   │  │    Gemini   │        │
│  │    Web      │  │   Desktop   │  │   Desktop   │  │     Pro     │        │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘        │
│         │                │                │                │                │
│         └────────────────┴────────────────┴────────────────┘                │
│                                   │                                          │
│                    ┌──────────────┴──────────────┐                          │
│                    │     DELEGATION ROUTER       │                          │
│                    │  (autonomous-empire rules)  │                          │
│                    └──────────────┬──────────────┘                          │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                       LAYER 2: AGENT AGENCY                                  │
│                        (agent-agency-mcp)                                    │
│                                                                              │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │                      AGENT REGISTRY (PostgreSQL)                      │  │
│  │  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐        │  │
│  │  │ Builder │ │ Content │ │ Design  │ │ Deploy  │ │ Monitor │        │  │
│  │  │ Agents  │ │ Agents  │ │ Agents  │ │ Agents  │ │ Agents  │        │  │
│  │  └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘        │  │
│  └───────┴───────────┴───────────┴───────────┴───────────┴──────────────┘  │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                      LAYER 3: EXECUTION ENGINES                              │
│                                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐    │
│  │     n8n      │  │   MCP Tools  │  │   External   │  │    Local     │    │
│  │  Workflows   │  │   Servers    │  │    APIs      │  │   Scripts    │    │
│  │              │  │              │  │              │  │              │    │
│  │ • Scheduled  │  │ • Puppet     │  │ • FAL.ai     │  │ • PowerShell │    │
│  │ • Webhook    │  │ • ChatGPT    │  │ • Printify   │  │ • Python     │    │
│  │ • Manual     │  │ • n8n-mcp    │  │ • Notion     │  │ • Node.js    │    │
│  └──────────────┘  └──────────────┘  └──────────────┘  └──────────────┘    │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                      LAYER 4: OUTPUT & STORAGE                               │
│                                                                              │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐    │
│  │   Supabase   │  │    QNAP      │  │    Notion    │  │   GitHub     │    │
│  │  (Database)  │  │   (Files)    │  │   (Docs)     │  │   (Code)     │    │
│  └──────────────┘  └──────────────┘  └──────────────┘  └──────────────┘    │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                    LAYER 5: FEEDBACK & IMPROVEMENT                           │
│                                                                              │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │                     COMPLETION VERIFIER                                │  │
│  │  • Did task complete successfully?                                     │  │
│  │  • What was the execution time?                                        │  │
│  │  • What errors occurred?                                               │  │
│  │  • Which agent performed best?                                         │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                   │                                          │
│                                   ▼                                          │
│  ┌───────────────────────────────────────────────────────────────────────┐  │
│  │                     LEARNING REGISTRY                                  │  │
│  │  • Update agent success rates                                          │  │
│  │  • Refine delegation rules                                             │  │
│  │  • Log patterns for future optimization                                │  │
│  │  • Trigger auto-agent-creator for gaps                                 │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────┘
                                      │
                                      ▼
                            [CYCLE REPEATS]
```

---

## COMPONENT MAPPING

### Layer 1: Meta-Orchestrator Platforms

| Platform | MCP Server | Primary Use | Fallback |
|----------|------------|-------------|----------|
| Claude Web | Native tools | Complex reasoning, planning, this blueprint | Claude Desktop |
| Claude Desktop | agent-agency-mcp, n8n-mcp, Desktop Commander | Local execution, file ops | ChatGPT Desktop |
| ChatGPT Desktop | chatgpt-mcp-server | Alternative execution, browser tasks | Claude Web |
| n8n | Native | Scheduled automation, webhooks | Direct API calls |

### Layer 2: Agent Registry

**Repository:** `agent-agency-mcp`
**Database:** PostgreSQL `agent_system`

| Agent Type | Purpose | Auto-Created By |
|------------|---------|-----------------|
| Builder | Creates new agents, workflows, code | auto-agent-creator |
| Content | Generates text, prompts, documentation | prompt-engineer-agent |
| Design | Creates images, mockups, assets | midjourney-automation, asset-vault |
| Deploy | Pushes to production, manages releases | n8n workflows |
| Monitor | Tracks completion, reports errors | hourly-autopilot-system |



### Layer 3: Execution Engine Mapping

| Engine | Repo/Tool | Capabilities | Trigger Method |
|--------|-----------|--------------|----------------|
| n8n Workflows | bermech-n8n-workflows | 50+ workflows, all integrations | Webhook, Schedule, Manual |
| MCP Puppet | mcp-puppet-pipeline | Browser automation, scraping | MCP tool call |
| ChatGPT MCP | chatgpt-mcp-server | File ops, PowerShell, n8n control | SSE endpoint |
| n8n MCP | n8n-mcp | Direct workflow execution from Claude | MCP tool call |
| OpenAI Notion | openai-notion-mcp | Notion CRUD via OpenAI | HTTP API |

### Layer 4: Storage Mapping

| Storage | Purpose | Access Method |
|---------|---------|---------------|
| Supabase | Structured data, asset-vault, auth | REST API, SDK |
| QNAP NAS | Large files, media, backups | SMB, HTTP |
| Notion | Documentation, task tracking, agent docs | API |
| GitHub | Code, version control, deployments | CLI, API |
| PostgreSQL | Agent registry, workflow state | Direct connection |

---

## DELEGATION RULES

### Rule 1: Platform Selection Matrix

```
TASK TYPE → PREFERRED PLATFORM → FALLBACK CHAIN

Code Generation     → Claude Desktop (Desktop Commander) → Claude Web → ChatGPT
File Operations     → Claude Desktop (Desktop Commander) → ChatGPT MCP → n8n
Browser Automation  → mcp-puppet-pipeline → ChatGPT MCP → Manual
Image Generation    → n8n → FAL.ai → Midjourney (via puppet)
Scheduled Tasks     → n8n (cron) → Windows Task Scheduler
Database Operations → n8n → Direct PostgreSQL → Supabase
Documentation       → Claude Web → Notion API → Manual
Deployment          → GitHub Actions → n8n → PowerShell scripts
```

### Rule 2: Complexity Routing

```python
def route_task(task):
    complexity = assess_complexity(task)
    
    if complexity == "simple":
        # Single tool, single step
        return delegate_to_n8n(task)
    
    elif complexity == "medium":
        # Multiple tools, sequential steps
        return delegate_to_agent_agency(task)
    
    elif complexity == "complex":
        # Requires planning, multiple agents, verification
        return delegate_to_meta_orchestrator(task)
    
    elif complexity == "novel":
        # Never done before, may need new agent
        return create_agent_then_delegate(task)
```

### Rule 3: Failure Escalation

```
Level 0: Automatic retry (3x with backoff)
Level 1: Try fallback platform
Level 2: Log to Notion, alert via webhook
Level 3: Queue for human review
Level 4: Create improvement ticket
```

---

## SELF-BUILDING CYCLE

### Phase 1: Task Intake

```yaml
trigger: Human provides natural language intent
actions:
  - Parse intent using prompt-engineer-agent
  - Classify task type (build/content/design/deploy/monitor)
  - Check agent-agency-mcp for existing capable agent
  - If no agent exists: trigger auto-agent-creator
  - Route to appropriate execution engine
output: Structured task with assigned agent
```

### Phase 2: Execution

```yaml
trigger: Task assigned to agent
actions:
  - Agent retrieves context from autonomous-empire
  - Agent executes using mapped tools
  - Progress logged to PostgreSQL
  - Intermediate outputs stored to appropriate layer 4 storage
output: Task result or error state
```

### Phase 3: Verification

```yaml
trigger: Execution complete
actions:
  - Completion verifier checks success criteria
  - If failed: escalate per failure rules
  - If succeeded: log metrics (time, resources, quality)
  - Update agent success rate in registry
output: Verified completion status
```

### Phase 4: Learning

```yaml
trigger: Verification complete
actions:
  - Analyze execution patterns
  - If new pattern detected: document in autonomous-empire
  - If agent underperformed: flag for review
  - If gap identified: queue auto-agent-creator
  - Update delegation rules based on outcomes
output: Improved routing for next cycle
```

### Phase 5: Self-Improvement

```yaml
trigger: Weekly or after N tasks
actions:
  - Aggregate performance metrics
  - Identify bottlenecks and failures
  - Generate improvement recommendations
  - Auto-create tickets for system upgrades
  - Test new agent configurations
  - Deploy improvements to production
output: Enhanced system capabilities
```

---

## IMPLEMENTATION PHASES

### PHASE 1: Foundation (Week 1-2)

**Objective:** Establish core delegation infrastructure

| Task | Repo | Action | Verification |
|------|------|--------|--------------|
| 1.1 | agent-agency-mcp | Verify all MCP tools operational | `delegate_task` returns success |
| 1.2 | bermech-n8n-workflows | Audit active workflows, document in Notion | Workflow inventory complete |
| 1.3 | autonomous-empire | Create 03-AGENTS folder with registry schema | Agents documented |
| 1.4 | n8n-mcp | Build and test MCP server | Claude can trigger workflows |
| 1.5 | chatgpt-mcp-server | Verify SSE endpoint operational | ChatGPT executes commands |

**Deliverable:** Any AI platform can delegate to agent-agency-mcp



### PHASE 2: Self-Building Loop (Week 3-4)

**Objective:** Enable system to create new agents autonomously

| Task | Repo | Action | Verification |
|------|------|--------|--------------|
| 2.1 | auto-agent-creator | Connect to agent-agency-mcp registration API | New agents auto-register |
| 2.2 | prompt-engineer-agent | Deploy n8n workflow, test plain English → prompt | Prompts generated correctly |
| 2.3 | mcp-puppet-pipeline | Fix git path issues, test browser automation | Can automate web tasks |
| 2.4 | autonomous-empire | Add agent templates to 04-PROMPT-TEMPLATES | Templates available |
| 2.5 | Integration | Create "build new agent" n8n workflow | End-to-end agent creation works |

**Deliverable:** "Create an agent that does X" → working agent in registry

### PHASE 3: Cross-Platform Coordination (Week 5-6)

**Objective:** All AI platforms can delegate to each other

| Task | Repo | Action | Verification |
|------|------|--------|--------------|
| 3.1 | openai-notion-mcp | Deploy HTTP service, connect to n8n | OpenAI can write to Notion |
| 3.2 | hourly-autopilot-system | Configure Windows scheduler, connect to n8n | Hourly tasks run |
| 3.3 | Buddy System | Implement delegation webhooks between platforms | Claude → ChatGPT works |
| 3.4 | Memory API | Verify localhost:8765 serves to all platforms | Context shared |
| 3.5 | Handover Protocol | Test full handover between Claude Web → Desktop | Seamless transitions |

**Deliverable:** Task started on any platform completes on most capable platform

### PHASE 4: Revenue Automation (Week 7-8)

**Objective:** Money-generating workflows run autonomously

| Task | Repo | Action | Verification |
|------|------|--------|--------------|
| 4.1 | balding-pig-automation | Deploy full system, test end-to-end | Products auto-listed |
| 4.2 | midjourney-automation | Connect to balding-pig, test image pipeline | Images generated on demand |
| 4.3 | asset-vault | Run Supabase migration, deploy to Emergent | Characters stored, generated |
| 4.4 | jesse-novel-factory | Deploy Next.js app, test novel pipeline | Novel → audiobook works |
| 4.5 | AutoDesign-POD-Empire | Connect trend monitoring, test auto-design | Trending designs created |

**Deliverable:** POD products created and listed without human intervention

### PHASE 5: Production Systems (Week 9-12)

**Objective:** Full autonomous production capability

| Task | Repo | Action | Verification |
|------|------|--------|--------------|
| 5.1 | gremlos-world-puppet | Configure 14 agents, test video production | Videos produced |
| 5.2 | taleweaver | Build memoir platform, deploy | Users can create books |
| 5.3 | ai-orchestrator-platform | Complete React UI, deploy | Multi-LLM dashboard works |
| 5.4 | All | Implement monitoring dashboards | Real-time visibility |
| 5.5 | All | Document in autonomous-empire | Complete runbooks |

**Deliverable:** All revenue streams automated with monitoring

---

## N8N WORKFLOW SPECIFICATIONS

### Core Workflows Required

#### WF-001: Task Delegation Router

```yaml
name: task-delegation-router
trigger: Webhook (POST /webhook/delegate)
inputs:
  - task_description: string
  - source_platform: string
  - priority: high|medium|low
  - callback_url: string (optional)

steps:
  1. Parse task with Claude API
  2. Query agent-agency-mcp for capable agents
  3. Select best agent based on:
     - Success rate
     - Current load
     - Task type match
  4. Execute via appropriate engine
  5. POST result to callback_url or store

outputs:
  - task_id: string
  - assigned_agent: string
  - status: queued|running|complete|failed
```

#### WF-002: Agent Auto-Creator

```yaml
name: agent-auto-creator
trigger: Webhook (POST /webhook/create-agent)
inputs:
  - agent_description: string
  - capabilities: string[]
  - template: string (optional)

steps:
  1. Generate agent spec using prompt-engineer-agent
  2. Select template from autonomous-empire/04-PROMPT-TEMPLATES
  3. Generate agent code using Claude API
  4. Register in agent-agency-mcp
  5. Document in Notion
  6. Test with sample task
  7. If test fails: iterate or flag for review

outputs:
  - agent_id: string
  - registration_status: success|failed
  - test_result: pass|fail
```

#### WF-003: Completion Verifier

```yaml
name: completion-verifier
trigger: Webhook (POST /webhook/verify)
inputs:
  - task_id: string
  - expected_outputs: object
  - verification_method: file_exists|api_check|manual

steps:
  1. Fetch task details from PostgreSQL
  2. Execute verification based on method
  3. Log result to task record
  4. Update agent success metrics
  5. If failed: trigger escalation workflow
  6. If succeeded: trigger learning workflow

outputs:
  - verification_status: verified|failed|pending
  - metrics: object
```

#### WF-004: Hourly Autopilot

```yaml
name: hourly-autopilot
trigger: Cron (0 * * * *)

steps:
  1. Check task queue for scheduled items
  2. Check monitoring dashboards for alerts
  3. Process any pending completions
  4. Generate hourly status report
  5. If anomalies: alert via webhook
  6. Archive old logs (>7 days)

outputs:
  - tasks_processed: number
  - alerts_generated: number
  - status: healthy|degraded|critical
```

#### WF-005: Platform Handover

```yaml
name: platform-handover
trigger: Webhook (POST /webhook/handover)
inputs:
  - source_platform: claude_web|claude_desktop|chatgpt|n8n
  - target_platform: claude_web|claude_desktop|chatgpt|n8n
  - context: object
  - task_continuation: string

steps:
  1. Package context as WARP.md format
  2. Store in handoff location (QNAP or local)
  3. Trigger target platform via appropriate method:
     - Claude Desktop: Update claude_desktop_config.json MCP
     - ChatGPT: POST to chatgpt-mcp-server
     - n8n: Trigger workflow webhook
  4. Confirm target received context
  5. Log handover in PostgreSQL

outputs:
  - handover_id: string
  - status: complete|failed
  - target_confirmation: boolean
```



### Revenue Workflows

#### WF-006: Balding Pig Product Pipeline

```yaml
name: balding-pig-product-pipeline
trigger: Webhook or Schedule (daily)
inputs:
  - trend_source: perplexity|manual
  - product_type: tshirt|mug|poster|all
  - quantity: number

steps:
  1. Fetch trending topics via Perplexity API
  2. Generate design concepts using Claude
  3. Create images via midjourney-automation or FAL.ai
  4. Upload to Printify
  5. Generate product descriptions
  6. Create listings
  7. Log to Notion database
  8. Update inventory tracking

outputs:
  - products_created: number
  - printify_ids: string[]
  - notion_entries: string[]
```

#### WF-007: Novel Factory Pipeline

```yaml
name: novel-factory-pipeline
trigger: Webhook (POST /webhook/novel)
inputs:
  - title: string
  - genre: string
  - outline: string
  - target_length: short|medium|long

steps:
  1. Expand outline using Claude
  2. Generate chapters iteratively
  3. Apply style consistency checks
  4. Generate audiobook via ElevenLabs
  5. Package outputs (ePub, PDF, MP3)
  6. Store in QNAP
  7. Update Notion tracking

outputs:
  - novel_id: string
  - formats: string[]
  - storage_paths: object
```

---

## METRICS & SUCCESS CRITERIA

### System Health Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Task Completion Rate | >95% | Completed / Total tasks |
| Average Task Time | <5 min (simple), <30 min (complex) | Timestamp delta |
| Agent Utilization | >70% | Active time / Available time |
| Handover Success | >99% | Successful handovers / Total |
| Self-Created Agents | >5/month | New agents registered |
| Human Intervention Rate | <5% | Manual tasks / Total tasks |

### Build Cycle Metrics

| Cycle | Metric | Target |
|-------|--------|--------|
| 1 | Foundation operational | All MCP servers responding |
| 2 | Self-building active | 1 agent auto-created |
| 3 | Cross-platform working | Handover < 30s |
| 4 | Revenue generating | $100/day automated |
| 5 | Full production | All systems monitored |

### Improvement Velocity

```
Cycle N → Cycle N+1 improvements:
- 10% reduction in task completion time
- 5% increase in first-attempt success rate
- 1 new capability added
- 2 manual steps automated
```

---

## IMMEDIATE ACTION ITEMS

### Today (Priority 1)

1. **Verify agent-agency-mcp status**
   ```powershell
   cd C:\Users\bermi\Projects\agent-agency-mcp
   npm run build
   npm start
   # Test: POST to /api/agents/register
   ```

2. **Create n8n workflow: task-delegation-router**
   - Import base workflow
   - Configure Claude API credential
   - Set webhook URL
   - Test with sample task

3. **Update autonomous-empire with this blueprint**
   ```powershell
   cd C:\Users\bermi\Projects\autonomous-empire
   mkdir 05-BLUEPRINTS
   cp C:\Users\bermi\Projects\BLUEPRINTS\AUTONOMOUS_BUILD_SYSTEM.md 05-BLUEPRINTS/
   git add -A
   git commit -m "Add autonomous build system blueprint"
   git push
   ```

### This Week (Priority 2)

4. **Audit bermech-n8n-workflows**
   - List all active workflows
   - Document in Notion
   - Identify gaps vs blueprint requirements

5. **Build n8n-mcp server**
   - Review existing code
   - Implement missing tools
   - Test with Claude Desktop

6. **Create agent templates**
   - Builder agent template
   - Content agent template
   - Design agent template
   - Deploy agent template
   - Monitor agent template

### Next Week (Priority 3)

7. **Implement auto-agent-creator integration**
8. **Deploy prompt-engineer-agent workflow**
9. **Fix mcp-puppet-pipeline path issues**
10. **Test end-to-end self-building cycle**

---

## APPENDIX A: Repository → Blueprint Mapping

| Repository | Blueprint Layer | Primary Function |
|------------|-----------------|------------------|
| autonomous-empire | L1, L5 | Governance, rules, templates |
| agent-agency-mcp | L2 | Agent registry, delegation |
| bermech-n8n-workflows | L3 | Execution engine |
| n8n-mcp | L1→L3 | Bridge Claude to n8n |
| chatgpt-mcp-server | L1→L3 | Bridge ChatGPT to system |
| mcp-puppet-pipeline | L3 | Browser automation |
| auto-agent-creator | L2, L5 | Self-building capability |
| prompt-engineer-agent | L1, L2 | Intent parsing |
| openai-notion-mcp | L1→L4 | OpenAI to Notion bridge |
| hourly-autopilot-system | L3, L5 | Scheduled execution |
| balding-pig-automation | L3, L4 | Revenue: POD |
| midjourney-automation | L3 | Image generation |
| asset-vault | L3, L4 | Asset storage/generation |
| jesse-novel-factory | L3, L4 | Revenue: Books |
| AutoDesign-POD-Empire | L3, L4 | Revenue: Auto-POD |
| gremlos-world-puppet | L3 | Video production |
| taleweaver | L3, L4 | Revenue: Memoirs |
| ai-orchestrator-platform | L1 | Multi-LLM UI |

---

## APPENDIX B: API Endpoints Summary

| Endpoint | Purpose | Auth |
|----------|---------|------|
| `http://192.168.50.246:5678/webhook/*` | n8n webhooks | None/API Key |
| `http://localhost:3000/sse` | ChatGPT MCP | None |
| `http://localhost:8765/context` | Memory API | None |
| `http://localhost:8765/api/skills` | Skill storage | None |
| `https://ylcepmvbjjnwmzvevxid.supabase.co` | Supabase | API Key |
| PostgreSQL `192.168.50.246:5432` | Agent registry | Password |

---

## APPENDIX C: File Locations

| Resource | Path |
|----------|------|
| This Blueprint | `C:\Users\bermi\Projects\BLUEPRINTS\AUTONOMOUS_BUILD_SYSTEM.md` |
| Master Prompt Library | `C:\Users\bermi\Projects\MASTER_PROMPT_LIBRARY.md` |
| Memory JSON | `http://localhost:8765/memory.json` |
| Playbook JSON | `http://localhost:8765/playbook.json` |
| Agent Templates | `autonomous-empire/04-PROMPT-TEMPLATES/` |
| n8n Workflows | `bermech-n8n-workflows/` |
| Handover Files | `C:\Users\bermi\Projects\*\WARP.md` |

---

**END OF BLUEPRINT**

*This document is the canonical reference for the autonomous build system. All implementations must align with this architecture.*
