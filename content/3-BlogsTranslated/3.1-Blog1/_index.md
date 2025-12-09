---
title: "Blog 1"
date: 2025-07-09
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# Build Agentic Systems with CrewAI and Amazon Bedrock

*By Tony Kipkemboi, João (Joe) Moura, Karan Singh, and Aris Tsakpinis*  
*(co-authored with Joao Moura and Tony Kipkemboi from CrewAI)*

---

## 1. Introduction

The enterprise AI landscape is undergoing a seismic shift as **agentic systems** move from experiments to mission‑critical business assets.

- Deloitte predicts that **25%** of enterprises using generative AI will deploy AI agents in 2025, growing to **50% by 2027**.  
- The global AI agent market is projected to grow from **$5.1B (2024)** to **$47.1B (2030)**.

This post explains how **CrewAI’s open source agentic framework** combined with **Amazon Bedrock** enables sophisticated multi‑agent systems that can transform business operations.

We focus on:

- What AI agents and agentic design are  
- CrewAI concepts (flows, crews, agents, tasks, tools, process)  
- How CrewAI integrates with Amazon Bedrock (including Agents and Knowledge Bases)  
- A concrete solution for cloud security posture management on AWS

---

## 2. Agentic Design

An **AI agent** is an autonomous, intelligent system that uses LLMs and other AI capabilities to perform complex tasks with minimal human oversight.

Characteristics:

- Operates independently and adapts to changing conditions  
- Uses **modular components**: reasoning engines, memory, cognitive skills, tools  
- Executes sophisticated workflows instead of fixed rule‑based logic  

Traditional SaaS solutions:

- Are horizontally scalable and generic  
- Handle repetitive tasks well across sectors  
- But lack deep domain intelligence and flexibility in dynamic environments  

**Agentic systems** bridge this gap by combining:

- Context‑aware reasoning  
- Domain knowledge  
- Access to external tools and data sources  

Examples:

- **Software development:**  
  CrewAI agents generate, evaluate, and improve code. In the CrewAI GitHub repo, pull requests are reviewed by agents checking documentation consistency and security.
- **Supply chain management:**  
  Traditional systems only track stock; agentic systems use real‑time data (weather, geopolitical risk) to reroute shipments and reallocate resources.

---

## 3. Overview of CrewAI

**CrewAI** is an enterprise suite and Python‑based open source framework for:

- Building **AI flows**, **multi‑agent systems**, or combinations of both  
- Allowing agents to work together through collaborative intelligence  

Key ideas:

- Each agent has a **role**, **goal**, and **backstory**, and can access specific **tools**  
- Agents can **delegate** tasks and ask each other questions  
- Emphasis on **team collaboration**, modular design, and simplicity  

The framework is used across industries (healthcare, finance, retail) to automate routine tasks and also create new, higher‑skill roles.

---

## 4. CrewAI Key Concepts

At a high level, CrewAI offers two main ways to build agentic automations:

1. **Flows**  
2. **Crews**

### 4.1 Flows

**CrewAI Flows** provide a structured, event‑driven framework to orchestrate complex, multi‑step automations.

Flows allow you to mix:

- Regular Python code  
- Single LLM calls  
- Multiple crews  

…with:

- Conditional logic  
- Loops  
- Real‑time state management  

With **Amazon Bedrock** as the LLM backend, flows can:

- Route customer support tickets to different agent crews  
- Coordinate financial analysis workflows that react to market volatility  

Together, Flows + Bedrock enable dynamic automations that adapt to changing conditions.

### 4.2 Crews

A **Crew** is a group of agents working together on related tasks.

#### Agents

Agents are autonomous entities defined by:

- **Role** – function and responsibility in the system  
- **Backstory** – contextual narrative to guide decisions  
- **Goals** – objectives to achieve  
- **Tools** – APIs, databases, external systems they can use  

Agents can:

- Communicate and collaborate  
- Delegate tasks  
- Use tools to execute complex workflows

#### Tasks

**Tasks** specify work to be done:

- **Description** – natural‑language description of the action  
- **Agent assignment** – which agent is responsible  

Tasks can be independent or part of larger workflows across multiple agents.

#### Tools

**Tools** extend agent capabilities beyond pure LLM reasoning, for example:

- Calling REST APIs  
- Querying databases  
- Executing scripts  
- Scraping websites  

Tools are modular and can be assigned to specific agents.

#### Process

The **process layer** controls:

- How agents coordinate  
- Task execution order  
- Communication and synchronization  

It ensures multi‑agent workflows run smoothly end‑to‑end.

---

## 5. CrewAI Enterprise Suite

CrewAI also offers an enterprise product with:

- Dedicated support and customization  
- Integration with enterprise systems such as **Amazon Bedrock**  
- Comprehensive **monitoring** and **observability**:
  - Logs of agent interactions  
  - Performance metrics  
  - Dashboards to track workflows and optimize agents in real time  

This allows organizations to deploy AI agents at scale while maintaining security and compliance.

---

## 6. Real‑World Enterprise Impact

### 6.1 Legacy Code Modernization

A large enterprise needed to modernize legacy **ABAP** and **APEX** code.

Multiple agents:

- Analyze existing code components  
- Generate modernized code in real time  
- Execute tests in production  
- Provide immediate feedback  

Results:

- ~**70%** improvement in code generation speed  
- Quality maintained via automated testing and feedback loops  
- Solution containerized with **Docker** for scalable deployment

### 6.2 Back‑Office Automation at a Global CPG

A leading CPG company connected existing apps and data stores to CrewAI agents that:

- Research industry conditions  
- Analyze pricing data  
- Summarize findings  
- Execute decisions automatically  

Outcome:

- **75% reduction** in processing time  
- End‑to‑end workflow from data analysis to action execution fully automated

---

## 7. Getting Started with CrewAI and Amazon Bedrock

Amazon Bedrock integration lets CrewAI use managed foundation models as the LLM for agents.

### 7.1 Basic LLM Configuration

```python
from crewai import Agent, Crew, Process, Task, LLM
from crewai_tools import SerperDevTool, ScrapeWebsiteTool
import os

# Configure Bedrock LLM
llm = LLM(
    model="bedrock/anthropic.anthropic.claude-3-5-sonnet-20241022-v2:0",
    aws_access_key_id=os.getenv('AWS_ACCESS_KEY_ID'),
    aws_secret_access_key=os.getenv('AWS_SECRET_ACCESS_KEY'),
    aws_region_name=os.getenv('AWS_REGION_NAME')
)

# Create an agent with Bedrock as the LLM provider
security_analyst = Agent(
    config=agents_config['security_analyst'],
    tools=[SerperDevTool(), ScrapeWebsiteTool()],
    llm=llm
)
```

Amazon Bedrock advantages for CrewAI:

- Access to state‑of‑the‑art models (Anthropic Claude, Amazon Nova, etc.)  
- Enterprise‑grade security and compliance  
- Scalability and reliability on AWS infrastructure  

---

## 8. Using Amazon Bedrock Agents and Knowledge Bases

- **Amazon Bedrock Agents** – fully managed, serverless autonomous agents.  
  - `BedrockInvokeAgentTool` lets CrewAI agents invoke Bedrock agents inside workflows.

- **Amazon Bedrock Knowledge Bases** – securely connect FMs and agents to company data.  
  - `BedrockKBRetrieverTool` enables natural‑language retrieval from Knowledge Bases.

### 8.1 Bedrock Agents Example

```python
from crewai import Agent, Task, Crew
from crewai_tools.aws.bedrock.agents.invoke_agent_tool import BedrockInvokeAgentTool

# Initialize the Bedrock Agents tool
agent_tool = BedrockInvokeAgentTool(
    agent_id="your-agent-id",
    agent_alias_id="your-agent-alias-id"
)

# CrewAI agent using the Bedrock Agents tool
aws_expert = Agent(
    role='AWS Service Expert',
    goal='Help users understand AWS services and quotas',
    backstory='I am an expert in AWS services and can provide detailed information about them.',
    tools=[agent_tool],
    verbose=True
)
```

### 8.2 Knowledge Bases Example

```python
# Create and configure the BedrockKB tool
kb_tool = BedrockKBRetrieverTool(
    knowledge_base_id="your-kb-id",
    number_of_results=5
)

# CrewAI agent using the Knowledge Base tool
researcher = Agent(
    role='Knowledge Base Researcher',
    goal='Find information about company policies',
    backstory='I am a researcher specialized in retrieving and analyzing company documentation.',
    tools=[kb_tool],
    verbose=True
)
```

---

## 9. Operational Excellence and Observability

Agentic applications combine deterministic and probabilistic components, so **observability** is crucial at three levels:

1. **Application level** – overall system health and orchestration  
2. **Model level** – LLM performance (accuracy, latency, throughput)  
3. **Agent level** – behavior of individual and multi‑agent workflows  

On AWS you can leverage:

- **Amazon CloudWatch** for application and model logs/metrics  
- CrewAI’s own logging (basic by default, `verbose=True` for more detail)  
- Third‑party tools such as AgentOps, Arize, MLFlow, LangFuse for advanced tracing and debugging

---

## 10. Solution Overview: Cloud Security Posture Management

Use case: **Cloud Security Posture Management (CSPM)** for AWS.

Goal: Continuously scan cloud infrastructure for misconfigurations and compliance risks using a **team of three agents**:

1. **Infrastructure mapper** – maps AWS resources and configurations  
2. **Security analyst** – analyzes vulnerabilities and best practices  
3. **Report writer** – generates clear, prioritized remediation reports  

### 10.1 Implementation Steps (High Level)

**Step 1 – Configure the Amazon Bedrock LLM**

```python
from crewai import Agent, Crew, Process, Task, LLM 
from crewai.project import CrewBase, agent, crew, task 

from aws_infrastructure_security_audit_and_reporting.tools.aws_infrastructure_scanner_tool import AWSInfrastructureScannerTool 
from crewai_tools import SerperDevTool, ScrapeWebsiteTool 
import os 

@CrewBase 
class AwsInfrastructureSecurityAuditAndReportingCrew():
    """AwsInfrastructureSecurityAuditAndReporting crew"""
    def __init__(self) -> None:
        self.llm = LLM(
            model=os.getenv('MODEL'),
            aws_access_key_id=os.getenv('AWS_ACCESS_KEY_ID'),
            aws_secret_access_key=os.getenv('AWS_SECRET_ACCESS_KEY'),
            aws_region_name=os.getenv('AWS_REGION_NAME')
        )
```

**Step 2 – Define Agents**

```python
@agent
def infrastructure_mapper(self) -> Agent:
    return Agent(
        config=self.agents_config['infrastructure_mapper'],
        tools=[AWSInfrastructureScannerTool()],
        llm=self.llm
    )

@agent
def security_analyst(self) -> Agent:
    return Agent(
        config=self.agents_config['security_analyst'],
        tools=[SerperDevTool(), ScrapeWebsiteTool()],
        llm=self.llm
    )

@agent
def report_writer(self) -> Agent:
    return Agent(
        config=self.agents_config['report_writer'],
        llm=self.llm
    )
```

**Step 3 – Define Tasks**

```python
@task
def map_aws_infrastructure_task(self) -> Task:
    return Task(
        config=self.tasks_config['map_aws_infrastructure_task']
    )

@task
def exploratory_security_analysis_task(self) -> Task:
    return Task(
        config=self.tasks_config['exploratory_security_analysis_task']
    )

@task
def generate_report_task(self) -> Task:
    return Task(
        config=self.tasks_config['generate_report_task']
    )
```

**Step 4 – Create AWS Infrastructure Scanner Tool**

```python
class AWSInfrastructureScannerTool(BaseTool):
    name: str = "AWS Infrastructure Scanner"
    description: str = (
        "A tool for scanning and mapping AWS infrastructure components and their configurations. "
        "Can retrieve detailed information about EC2 instances, S3 buckets, IAM configurations, "
        "RDS instances, VPC settings, and security groups. Use this tool to gather information "
        "about specific AWS services or get a complete infrastructure overview."
    )
    args_schema: Type[BaseModel] = AWSInfrastructureScannerInput

    def _run(self, service: str, region: str) -> str:
        try:
            if service.lower() == 'all':
                return json.dumps(self._scan_all_services(region), indent=2, cls=DateTimeEncoder)
            return json.dumps(self._scan_service(service.lower(), region), indent=2, cls=DateTimeEncoder)
        except Exception as e:
            return f"Error scanning AWS infrastructure: {str(e)}"

    def _scan_all_services(self, region: str) -> Dict:
        return {
            'ec2': self._scan_service('ec2', region),
            's3': self._scan_service('s3', region),
            'iam': self._scan_service('iam', region),
            'rds': self._scan_service('rds', region),
            'vpc': self._scan_service('vpc', region)
        }
```

**Step 5 – Assemble the Crew**

```python
@crew
def crew(self) -> Crew:
    """Creates the AwsInfrastructureSecurityAuditAndReporting crew"""
    return Crew(
        agents=self.agents,
        tasks=self.tasks,
        process=Process.sequential,
        verbose=True,
    )
```

**Step 6 – Run the Crew**

```python
def run():
    """
    Run the crew.
    """
    inputs = {}
    AwsInfrastructureSecurityAuditAndReportingCrew().crew().kickoff(inputs=inputs)
```

The system generates a structured report with an executive summary, risk matrix, and prioritized remediation roadmap.

---

## 11. Conclusion

This post demonstrates how to:

- Use **CrewAI** and **Amazon Bedrock** to build sophisticated, automated security assessment systems for AWS infrastructure  
- Design specialized agents that collaborate on mapping infrastructure, analyzing risks, and generating reports  
- Leverage Bedrock’s managed models, Agents, and Knowledge Bases for robust, scalable agentic applications  

The same approach can be extended to many other domains such as process automation, research, and decision support.

---

## 12. About the Authors

- **Tony Kipkemboi** – Senior Developer Advocate and Partnerships Lead at CrewAI, US Army veteran with background in healthcare, data engineering, and AI.  
- **João (Joe) Moura** – Founder and CEO of CrewAI, leading agent orchestration platform used widely across Fortune 500 companies.  
- **Karan Singh** – Generative AI Specialist at AWS, focusing on go‑to‑market strategies with foundation model and agentic framework providers.  
- **Aris Tsakpinis** – Specialist Solutions Architect for Generative AI at AWS, focusing on open source models on Amazon Bedrock and pursuing a PhD in Machine Learning Engineering.

