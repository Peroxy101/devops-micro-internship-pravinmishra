# Assignment 4 — Building Your AI Team

Part of the DevOps Micro Internship (DMI) Cohort 3 with Agentic AI

---

## Purpose

In this assignment, you will build and configure a set of specialized AI subagents inside your project. You will learn how different models and tool permissions define agent behavior, and you will trigger two real agent delegations to analyze security and cost aspects of your Terraform infrastructure.

---

# Task 1 — Create the Agents Folder and Add Files

## Goal

Create the `.claude/agents/` directory and add all required agent files.

### Evidence

#### Screenshot 1 — VS Code sidebar showing `.claude/agents/` with all 3 files

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4screenshot1.png

# Task 2 — Compare the Agent Configurations

## Goal

Analyze the configuration differences between the three agents and demonstrate understanding of model and tool selection.

### Written Answers

#### 1. Why does the cost optimizer use Haiku instead of Sonnet?

Cost checks are just fast pattern matching against known anti-patterns, not deep reasoning. That’s why Haiku handles it sharp-sharp at a fraction of the cost and latency. Even the assignment self wants you to observe this.

---

#### 2. Why does the security auditor NOT have Write in its tools list?

No Write for security auditor: Least privilege—an auditor is just there to observe and report, they must never modify the code they are reviewing. Removing Write makes the audit provably read-only, so it can’t introduce any changes or vulnerabilities, and the report stays 100% trustworthy.

---

#### 3. Why does the tf-writer use `inherit` instead of a specific model?

Inherit for tf-writer Code generation is a very high-stakes task, so tf-writer should always run on whatever model the main session is using rather than being pinned down. If you upgrade your session model, the writer upgrades automatically with zero config changes

---

### Evidence

#### Screenshot 2 — `security-auditor.md` frontmatter showing model and tools configuration

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4Screenshot2.png

#### Screenshot 3 — `cost-optimizer.md` frontmatter showing the model and tools configuration

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4Screenshot3.png

# Task 3 — Run the Security Auditor

## Goal

Trigger the security auditor agent and analyze the generated security report for your Terraform infrastructure.

### Evidence

#### Screenshot 4 — The delegation message showing Claude launched the security-auditor

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4Screenshot4.png

#### Screenshot 5 — Security audit report output

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4Screenshot5.png

# Task 4 — Run the Cost Optimizer

## Goal

Trigger the cost optimizer agent and review the generated cost optimization report.

### Evidence

#### Screenshot 6 — The full cost optimization report

Add your screenshot here.

https://github.com/Peroxy101/devops-micro-internship-pravinmishra/blob/main/week-02-agentic-ai/screenshots/AS4Screenshot6.png

# Submission Instructions

- Ensure all agent files are committed in `.claude/agents/`
- Complete all written answers in your GitHub Repo
- Push final changes to your forked GitHub repository

---

## GitHub Repository URL

Paste your forked repository URL here:

`Add your URL here`

---

# Completion Checklist

- [ ] `.claude/agents/` folder contains all 3 agent files
- [ ] Screenshot 2 shows correct `security-auditor.md` configuration
- [ ] Screenshot 3 shows correct `cost-optimizer.md` configuration
- [ ] All 3 written answers completed 
- [ ] Security auditor executed successfully
- [ ] Cost optimizer executed successfully
- [ ] Security report is visible with findings
- [ ] Cost report is visible with recommendations
- [ ] All required screenshots added
- [ ] GitHub repo updated with agents

---

## 📌 About DMI & CloudAdvisory

DevOps Micro Internship (DMI) is a project-based DevOps program run by Pravin Mishra (The CloudAdvisory) focused on real-world execution, systems thinking, and career readiness.

It helps learners build strong DevOps foundations with hands-on experience.

---

## 📌 Resources

- 🌐 DMI Official Website: https://pravinmishra.com/dmi  
- 🎓 DevOps for Beginners (Udemy): https://www.udemy.com/course/devops-for-beginners-docker-k8s-cloud-cicd-4-projects/  
- 🎓 Agentic AI DevOps with Claude Code: https://www.udemy.com/course/ultimate-agentic-ai-devops-with-claude-code/  
- 🎓 DevOps with Claude Code: Terraform, EKS, ArgoCD & Helm: https://www.udemy.com/course/devops-with-claude-code-terraform-eks-argocd-helm/  
- ▶️ YouTube Playlist: https://www.youtube.com/playlist?list=PLFeSNDtI4Cho  
- 🔗 Pravin Mishra (LinkedIn): https://www.linkedin.com/in/pravin-mishra-aws-trainer/  
- 🏢 CloudAdvisory (LinkedIn): https://www.linkedin.com/company/thecloudadvisory/

---

*This submission is part of DevOps Micro Internship (DMI) Cohort 3 — Agentic AI Track.*