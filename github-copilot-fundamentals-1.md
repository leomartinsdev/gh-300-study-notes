# Responsible AI with GitHub Copilot
## Mitigate AI risks
Responsible AI is an approach to developing, assessing, and deploying artificial intelligent systems in a safe, trustworthy, and ethical way.
## Microsoft and GitHub's six principles of responsible AI
Fairness: AI systems should treat all people fairly.
Reliability and safety: AI systems should perform reliably and safely.
Privacy and security: AI systems should be secure and respect privacy.
Inclusiveness: AI systems should empower everyone and engage people.
Transparency: AI systems should be understandable.
Accountability: People should be accountable for AI systems.

**Fairness**: AI systems should treat all people fairly
AI systems should treat everyone fairly, avoiding differential impacts on similarly situated groups. In contexts like medical treatment, loan applications, or employment, AI should provide consistent recommendations to individuals with similar symptoms, financial situations, or qualifications.

**Reliability and safety**: AI systems should perform reliably and safely
These systems need to function as designed, respond safely to unexpected conditions, and resist harmful manipulation.
Safety in AI refers to minimizing unintended harm, including physical, emotional, and financial harm to individuals and societies. Reliability means that AI systems perform consistently as intended without unwanted variability or errors. Safe and reliable systems are robust, accurate, and behave predictably under normal conditions.

**Privacy and security**: AI systems should be secure and respect privacy
Microsoft and GitHub’s approach to Responsible AI aims to stop abuse and keep user trust. Key points include:

- Getting users' permission before collecting their data. Clearly explain how the AI uses their data and get their consent. Don't collect data secretly. Let users choose if they want to share personal data and inform them through clear prompts and policies.
- Collecting only the data needed for the AI to work. Avoid gathering extra information and remove sensitive data once the AI is in use. Regularly check data inputs to ensure only essential data is collected.
- Anonymizing personal data. Use methods like pseudonymization and aggregation to protect identities. Pseudonymization replaces personal details with random identifiers, while aggregation groups data into summaries, removing specific individual details.

Encrypt sensitive data both during transfer and when stored. Use strong encryption methods and secure keys through:
- Hardware Security Modules (HSMs) which store keys in a tamper-proof environment.
- Secure vaults like Microsoft Azure for key storage with controlled access.
- Envelope encryption, which uses two keys for added security.
- Organizations should control who can access keys and models, rotate keys regularly, and securely back up keys. They should also limit employee access to sensitive models and data, classify them based on sensitivity, and conduct regular security audits to prevent unauthorized access.


**Inclusiveness**: AI systems should empower everyone and engage people
Inclusiveness means ensuring that AI systems are fair, accessible, and empower everyone. Microsoft's Responsible AI standard recognizes that AI creators (including GitHub) must proactively design AI to include all people, communities, and geographies - especially those areas of society historically underrepresented.

**Transparency**: AI systems should be understandable
Implementing transparency involves documenting data and models, creating explanatory interfaces, using AI debugging tools, constructing testing dashboards, and enabling logging and auditing.

- Explain how their systems operate clearly through a clear validation framework.
- Justify the design choices behind AI systems.
- Be honest about the capabilities and limitations of AI systems.
- Enable auditability with logging, reporting, and auditing capabilities.


**Accountability**: People should be accountable for AI systems
AI creators should be responsible for how their systems operate. They need to continuously monitor system performance and mitigate risks. Accountability in the AI industry is becoming a pressing issue as high-profile cases of algorithmic harm, bias, and abuse come to light. Critics increasingly argue that without accountability, AI creators hold too much power over opaque systems impacting lives.

# Introduction to GitHub Copilot
## GitHub Copilot, your AI pair programmer
GitHub Copilot is a service that provides you with an AI pair programmer that works with all of the popular programming languages.

Microsoft developed GitHub Copilot in collaboration with OpenAI. GitHub Copilot is powered by the OpenAI Codex system.

GitHub Copilot is available as an extension for VS Code, Visual Studio, Vim/Neovim, and the JetBrains suite of IDEs.

GitHub Copilot features
Beyond autocompletion, GitHub Copilot is an AI assistant throughout the entire development life cycle:

- **Copilot Chat**: Interactive chat inside supported editors to ask questions, explain code, generate tests/docs, and explore new features.
- **Pull Request Summaries**: Auto-generates PR descriptions to help reviewers understand intent.
- **Code Review Assistance**: Suggests issues, describes changes, and proposes improvements to speed up reviews.
- **Copilot CLI**: Suggests commands, generates shell scripts, and explains terminal output.
- **Copilot Spaces**: A context-rich environment to collaborate with AI on project planning, requirements, and design.
- **Copilot Cloud Agent**: Autonomously performs multi-step tasks — generating files, implementing features, or building scaffolding from a specification.


Subscription plans
GitHub Copilot is available in several plans. Plan availability and limits can change — check the official docs for current info.

**GitHub Copilot Free** — For individual developers at no cost. Includes limited monthly completions and chat requests, and access to advanced AI models.

**GitHub Copilot Pro** — For individuals wanting more. Higher usage limits, priority model access, full IDE integrations (VS Code, Visual Studio, JetBrains, Neovim), and automated test generation.

**GitHub Copilot Pro+** — All Pro features, plus additional premium request capacity and priority infrastructure access.

**GitHub Copilot Business** — For organizations. Adds centralized management and policy controls, security vulnerability filtering, public code filtering, and IP indemnity.

**GitHub Copilot Enterprise** — For large organizations. All Business features, plus codebase indexing for personalized suggestions, private model fine-tuning, GitHub chat integration, and AI-powered PR summaries.

## Interact with Copilot

Interact with Copilot

**Inline suggestions** — As you type, Copilot shows real-time completions as grayed-out text. Press `Tab` or `→` to accept, `Esc` or keep typing to reject. Best for repetitive tasks and boilerplate code.

**Command palette** — Open with `Ctrl+Shift+P` / `Cmd+Shift+P`, then type "Copilot" to access actions like *Explain This* or *Generate Unit Tests*.

**Copilot chat** — Natural language chat panel in your IDE. Ask questions, request code snippets, or explore concepts. Example: "How do I implement a binary search in Python?"

**Inline chat** — Open with `Ctrl+I` / `Cmd+I` to chat in context at your cursor location. Supports slash commands:
- `/explain` — explains selected code
- `/tests` — generates unit tests
- `/suggest` — offers code suggestions
- `/comment` — converts comments to code

**Comments to code** — Write a natural language comment and press `Enter`; Copilot generates the corresponding code.

**Multiple suggestions** — Use `Alt+]` / `Option+]` (or the light bulb icon) to cycle through alternative suggestions for a given completion.

**Explanations** — Select a code block, right-click, and choose *Copilot: Explain This* to get a plain-language explanation.

**Automated test generation** — Select a function or class and run *Copilot: Generate Unit Tests* from the command palette to generate unit tests.

> Copilot learns from context — well-structured, commented code leads to better suggestions.

## Set up, configure, and troubleshoot GitHub Copilot


# Introduction to prompt engineering with GitHub Copilot
## Prompt engineering foundations and best practices
Prompt engineering is the process of crafting clear instructions to guide AI systems, like GitHub Copilot, to generate context-appropriate code tailored to your project's specific needs.

Principles of prompt engineering
- Single: Always focus your prompt on a single, well-defined task or question. This clarity is crucial for eliciting accurate and useful responses from Copilot.
- Specific: Ensure that your instructions are explicit and detailed. Specificity leads to more applicable and precise code suggestions.
- Short: While being specific, keep prompts concise and to the point. This balance ensures clarity without overloading Copilot or complicating the interaction.
- Surround: Utilize descriptive filenames and keep related files open. This provides Copilot with rich context, leading to more tailored code suggestions.

**Zero-shot learning**
Here, GitHub Copilot generates code without any specific examples, relying solely on its foundational training. This approach is ideal for rapidly implementing common patterns and standard functionality.


**One-shot learning**
With this approach, a single example is given, aiding the model in generating more context-aware responses that follow your specific patterns and conventions.

**Few-shot learning**
Copilot is presented with several examples, which strike a balance between zero-shot unpredictability and the precision of fine-tuning. Excels at generating sophisticated implementations that handle multiple scenarios and edge cases.

**Chain prompting and managing chat history**
- Summarize context when conversations become lengthy: "Based on our previous discussion about user authentication, now add rate limiting to prevent brute force attacks"
- Reset and provide focused context for new features: Start fresh with essential details rather than carrying forward the entire conversation
- Use concise references to previous work instead of repeating full implementations

Role prompting for specialized tasks
Instruct Copilot to act as a domain expert to get more targeted, production-ready code on the first try. Common roles:

- **Security expert**: *"Act as a cybersecurity expert. Create a password validation function following OWASP guidelines."* → generates input sanitization, attack protection, and security best practices.
- **Performance expert**: *"Act as a performance optimization expert. Refactor this sorting algorithm for large datasets."* → produces optimized algorithms, memory-efficient implementations, and scalability considerations.
- **Testing specialist**: *"Act as a testing specialist. Create comprehensive unit tests for this payment module, including edge cases."* → generates thorough coverage, mocks, and error condition tests.


## GitHub Copilot user prompt process flow

**Inbound:**
1. **Context gathering** -- Prompt is sent over HTTPS. Copilot collects surrounding code (using Fill-in-the-Middle/FIM), filename, open tabs, project structure, and language/framework info.
2. **Proxy filter** -- Prompt passes to a GitHub-owned Azure proxy that blocks prompt injection and manipulation attempts.
3. **Toxicity filtering** -- Filters out hate speech, offensive content, and personal data before code generation.
4. **LLM code generation** -- The filtered prompt is sent to the LLM, which generates context-aware code suggestions.

**Outbound:**
5. **Post-processing** -- Toxicity filter runs again on output. Proxy checks for bugs/vulnerabilities (e.g., XSS, SQL injection). Optionally, public code matching can be enabled to suppress suggestions that closely resemble (~150+ chars) existing GitHub code.
6. **Delivery and feedback loop** -- Only clean responses are delivered. Accepted/rejected suggestions feed back into Copilot's learning.
7. **Repeat** -- The cycle continues with each prompt, with Copilot improving from accumulated context and feedback.

## GitHub Copilot Data

## GitHub Copilot Large Language Models (LLMs)


# Introduction to Copilot Spaces
## Creating your first space
## Sharing, Discoverability, and Governance
## Do's and Dont's of Working in a Space


# Using advanced GitHub Copilot features
## Advanced GitHub Copilot features
## Applied GitHub Copilot techniques


# GitHub Copilot Across Environments: IDE, Chat, Github.com and Command Line Techniques
## Code completion with GitHub Copilot
## GitHub Copilot Chat
## GitHub Copilot on Github.com
## GitHub Copilot for the CLI


# Management and customization considerations with GitHub Copilot
## Explore GitHub Copilot plans and their associated management and customization features
## Explore contractual protections in GitHub Copilot and disabling matching public code
## Manage content exclusions
## Troubleshoot common problems with GitHub Copilot


# Developer use cases for AI with GitHub Copilot
## Introduction
## Boost developer productivity with AI
## Align with developer preferences
## AI in the Software Development Lifecycle (SDLC)
## Understand limitations and measure impact


# Develop unit tests using GitHub Copilot tools
## Introduction
## Examine the unit testing tools and environment
## Create unit tests using the Generate Tests smart action
## Create unit tests using Inline Chat
## Create unit tests using Chat view modes
