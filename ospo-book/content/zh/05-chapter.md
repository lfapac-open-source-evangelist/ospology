---
title: "第5章：开源安全管理"
status: Completed
weight: 60
---

- [Introduction](#introduction)
- [Training and Education](#training-and-education)
- [Key Steps](#key-steps)
- [Applying This to Your Organization](#applying-this-to-your-organization)
- [Resources and Footnotes](#resources-and-footnotes)

- [总体介绍](#总体介绍)
- [培训与教育](#培训与教育)
- [关键举措](#关键举措)
- [应用到您的组织](#应用到您的组织)
- [资源和脚注](#资源和脚注)

## 总体介绍

> NOTE: This chapter has been developed through the expertise of Open Source Security Foundation (OpenSSF) representatives, with support from the TODO Group
> 提示：本章节使用到了开源安全基金会（OpenSSF）的专业知识，并得到TODO Group的支持。

Open source software is an important part of the software supply chain. Because of this, it's part of an OSPO’s responsibility to help secure the OSS supply chain. This includes tasks such as:
开源软件是软件供应链的重要组成部分。因此，OSPO开源办公室的重要职责之一就是协助实现开源软件供应链的安全性，包括如下的任务：

- Helping development teams assess the security of the OSS they use in products.
- Encouraging development teams to contribute to upstream open source projects to help improve their security.
- Following secure software development best practices in open source projects that the company maintains, contributes to, or leads.
- 协助开发团队评估他们在产品中使用的开源软件的安全性
- 鼓励开发团队向开源上游项目提交贡献，提升其安全性
- 在公司维护、贡献或主导的开源项目中，遵循软件研发安全的最佳实践

This chapter includes useful resources to help OSPOs and open source developers apply secure software development and supply chain best practices - both in the software they use and the software they create.
本章节包含对OSPO开源办公室和开源软件开发者的有用资源，用于实施软件研发安全和供应链管理的最佳实践，包括他们引入和自己研发的软件。

In some ways, security is just like any other requirement. However, many software developers and their managers haven't received enough training in security. Also, security is about defending against intelligent attackers, and it often depends on how the entire system works together — not just on one part.
在某个意义上，安全就是另一种功能需求。然而，很多软件研发者和他们的管理者都未得到足够的安全培训。另外安全也是涉及抵御机密窃取的攻击，这依赖与整个系统的协同工作，不仅仅是其中一环。

Fixing security problems later is often expensive. It's better to prevent them, reduce their chances or impact, and be prepared in case something still goes wrong. It’s important to plan from the beginning and allocate resources (such as time and money) to handle security properly. Open source software can have a security advantage because it allows for mass peer review and follows the principle of “open design” — but these benefits don’t happen automatically.
事后的安全问题修复常常成本高昂。较好的做法是预防安全问题，减少其概率和影响面，并为某环节出错的情况做好准备。在早期就对安全体系投入时间和财务资源是非常重要的。开源软件能够具备安全优势，因为它允许广泛的同行评审和遵循开放涉及的原则，但这些优势并不是自动就到来。

## Training and Education
## 培训与教育

Many software developers and managers don’t know what they need to know about security. This lack of knowledge often causes problems. Here are some key areas to understand, along with links to free OpenSSF courses that can help. These specific courses aren't required, but it's important that everyone involved in software development gets the right training.
很多软件研发人员和管理者不知道为何他们需要理解安全。这些认知的缺乏常常导致问题。这里给出一些需要理解的关键领域，以及有助解决问题的OpenSSF开源机构免费课程的链接。这些课程不是强制的，但每位软件研发的从业者能获取合适的培训是非常重要的事情。

Managers (of both open and closed source projects) should understand how to manage secure software development. This includes knowing basic security terms, how to manage risks, how to build security into the design, how to protect all environments, how to identify risks early, and how to set clear expectations with stakeholders. Managers should also understand what their developers need to learn. If they haven’t been trained yet, they can take the free Open Source Security Foundation OpenSSF course *Security for Software Development Managers (LFD125)* [^1].
管理者（包括开源和闭源软件项目）应当理解如何管理安全的软件研发，包括理解掌握基本的安全术语，管控风险，如何把安全嵌入软件设计，如何确保全部软件环境的安全，如何预先识别风险，以及给相关方一个清晰的预期。管理者还应该知晓他们的研发人员应该学习什么安全知识。若管理者们尚未接受培训，他们可以参加开源安全基金会（OpenSSF）的免费培训 “软件研发管理者的安全培训 Security for Software Development Managers (LFD125)” [^1] 。

Developers should take a course on secure software development. This includes how to build secure software during planning, design, coding, testing, and release. Developers also need to know how to evaluate third-party software. They should understand common vulnerabilities (like those in the OWASP Top Ten for web apps [^2] and CWE Top 25 for general software [^3]) and how to avoid them. They should also know how to secure development environments and respond to vulnerability reports. If they haven't had this training, they can take the free OpenSSF course Developing Secure Software (LFD121) [^4].
软件研发人员应该参加软件安全开发课程。包括如何在软件的规划、设计、编码、测试和发布各个阶段嵌入安全能力。软件研发人员还应该了解如何评估第三方软件，他们应当理解常见的被攻击点（Web应用的OWASP前十攻击点 [^2]、通用软件的CWE前25攻击点 [^3]、这些攻击点的规避方法）他们也应对知晓如何确保研发环境的安全性，如何应对安全披露报告。若他们未接受这些培训，可以参加开源安全基金会（OpenSSF）的免费培训 “开发安全软件Developing Secure Software (LFD121)” [^4]

Both developers and managers must understand any laws or regulations they need to follow. For example, anyone involved in software that may be used in the European Union (EU) should understand the EU Cyber Resilience Act (CRA). This includes knowing what the CRA applies to, the different roles it defines (such as manufacturer or open source steward), and the legal responsibilities it creates. Because the CRA covers a wide range and includes strong penalties, those who need to understand it can take the free OpenSSF course Understanding the European Union (EU) Cyber Resilience Act (CRA) (LFEL1001) [^5].
软件研发人员和管理者都必须理解他们需要遵循的法律和监控条例。例如，所有设计在欧盟（EU）使用软件的相关方，都应当了解欧盟《网络弹性法案》（CRA, Cyber Resilience Act），这包含知晓该法案的适用面，法案定义的不同参与角色（例如制造商、开源管理者）和法律义务。由于CRA法案覆盖了较大的适用面和较强的惩罚性，受法案约束的相关方可以参加开源安全基金会（OpenSSF）的免费培训 “理解欧盟《网络弹性法案》Understanding the European Union (EU) Cyber Resilience Act (CRA) (LFEL1001)” [^5]

## Key Steps
## 关键举措

**For developing your own software:**
**研发您的自有软件：**

1. Review the OpenSSF Concise Guide for Developing More Secure Software, which links to practical resources [^6].
1. 评估开源安全基金会OpenSSF的《Concise Guide for Developing More Secure Software》指引文档，文档中提供了实用资源 [^6]。

2. Work to meet the OpenSSF Baseline, a short list of security checks [^7].
2. 致力于达到开源安全基金会OpenSSF的安全基线，其包含的安全检查项清单 [^7]。

3. Earn an OpenSSF Best Practices badge for your project. Start with “passing” and plan to achieve “silver” or “gold” over time [^8].
3. 获取开源安全基金会OpenSSF的安全实践徽章，从“达标 passing”开始，并规划依次实现“银标 silver”或“金标 gold” [^8]。

4. Improve your OpenSSF Scorecard score. While this is often used to evaluate other projects, it can also help you measure your own [^9].
4. 改进您项目的开源安全基金会OpenSSF安全评分表 Scorecard 得分，这个评分表常常用来评估外部外部项目，也可以为您评估您自己的项目 [^9]。

**Most modern software reuses other software. Choose and use open source components carefully:**
**大部分现代软件重用了外部软件，选用开源组件需严谨：**

1. Use the Concise Guide for Evaluating Open Source Software [^10].
1. 使用开源软件简要评估 [^10]。 

2. Double-check software names to avoid “typosquatting” attacks (where malicious packages have names similar to trusted ones).
2. 仔细检查软件名称以规避“近似名称”攻击（恶意软件包使用与可信软件包近似的名称）。

3. Use the OpenSSF Scorecard to evaluate software before using it [^9].
3. 使用开源安全基金会OpenSSF安全评分表 Scorecard，在引入外部软件时先评估其安全评分表得分。

**Protect your environments, including development, build, test, and distribution:**
**保护你的软件环境，包括研发、构建、测试和分发环境：**

1. Use multi-factor authentication (MFA) to make it harder for attackers to gain access.
1. 使用多因素认证（MFA），增大攻击者访问难度。

2. Secure your build environment. See OpenSSF SLSA for more guidance [^11].
2. 安全加固您的构建环境，请参考开源安全基金会OpenSSF发布的SLSA规范作为指引 [^11]。

**Use automated tools in your continuous integration (CI) pipeline to catch security issues early:**
**在您的持续集成流水线中使用自动化工具，提早发现安全问题：**

1. Use multiple types of tools, as each may find different problems, see the Guide to Security Tools [^12].
1. 使用多类型工具，每一种工具可以发现不同的安全问题，请参考 the Guide to Security Tools [^12]。

2. For new projects (“green field”), enable all security checks. For older projects (“brown field”), start with the most important checks so the reports are manageable
2. 对新建类型的项目（绿地项目），要执行全部安全检测。对存量类型项目（棕地项目），以最重要的安全检测为启动，确保检测报告的可管控。

3. Enable tools that detect known vulnerabilities in reused components
3. 对复用组件，启用安全工具来检测已知的攻击点。 

Prepare for vulnerability reports — they can happen to any project. Clearly explain how people can report vulnerabilities. Open source projects should review the OpenSSF Guide to implementing a coordinated vulnerability disclosure process [^13].
为安全风险披露报告做好准备，任何项目都会面对这种情况。要告知人们如何提交安全风险点。开源项目需要评估开源安全基金会OpenSSF的指引，实施安全风险披露流程 [^13]。

## Applying This to Your Organization
## 如何在您的组织机构中实施

Improving the security of OSS in your organization isn't just about using tools. It also requires changes in culture and daily work processes. One of the first steps is to build a mindset where security is everyone’s responsibility, not just the job of a small team. Leaders should clearly communicate that secure software development is important and support this with time, resources, and recognition for those who work on it.
提升您所在组织机构的开源安全水平不仅仅是使用工具，也涉及到企业文化和日常工作流程。启动工作之一是灌输这个安全理念，安全是全部人的责任而不仅仅是小团队的工作。领导者需清晰地表达软件安全研发的重要性，为这个工作提供持续的支持、资源投入和对相关责任团队的认可。

Security practices should be part of everyday development work, not something separate. For example, instead of running security checks only once in a while, make tools like scorecards and vulnerability scans part of your regular CI/CD pipeline. This helps make security a normal and expected part of how your team builds software.
软件安全实践应纳入日常的研发工作，而不是分离的独立工作。例如，替换掉安全检测只会偶尔执行一次的模式，改为常态化的CI/CD流水线中执行漏洞扫描和生成安全打分卡的模式。这会让软件安全成为您团队认同的理念和纳入预期。

Training and education should happen regularly, not just once. Developers and managers should be encouraged to learn the basics of secure software development. This can include free OpenSSF courses and other programs. Make sure your teams know that learning about security is important and will be recognized. This builds long-term interest and responsibility.
培训和教育应常态化定期执行，而不是一次性工作。研发人员和管理者应被鼓励学习软件安全研发的基础知识，包括开源安全基金会OpenSSF的免费和其他课程。要确保您的团队知晓安全非常重要，并会获得认可，这会构建长期的兴趣和责任感。

It also helps to be open about security progress. Encourage teams to track and share their progress on goals like earning Best Practices badges or improving their Scorecard results. This creates a positive environment where teams help each other and improve together, instead of feeling blamed when something goes wrong.
对安全改进的开放心态是非常有用的，要鼓励团队跟踪和分享他们的任务进展，例如获得最佳实践徽章，或提升他们的安全打分卡成绩。这会带来相互帮助和改进的积极团队文化，而不是发生错漏时的相互指责。

Lastly, support continuous improvement. Security isn't something you finish — it’s always changing. Set up regular times to review risks, update tools and practices, and share what your teams have learned. Give teams the freedom to make decisions about security early in the development process, not just at the end or after a problem happens.
最后，要支持持续的改进。软件安全不是一劳永逸的工作，它始终在变化。要设置常态化的风险评估时间计划，更新工具和实践流程，分享您团队的经验，让研发团队可以自主和预先决定研发流程中的安全工作，而不是在最后阶段或发生问题时才实施。

By creating a culture of shared responsibility, adding security into everyday work, investing in learning, encouraging openness, and improving over time, your organization can make real progress in securing the OSS it builds and uses.
通过构建责任共担文化、在日常工作中嵌入安全任务、投入资源学习、鼓励开放、持续改进等工作，您的组织机构可以实现开源软件安全开发和使用的实质性提升。

## Resources and Footnotes
## 资源和脚注

### Resources
### 资源

- OpenSSF: https://openssf.org
- OWASP: https://owasp.org/
- CWE: https://cwe.mitre.org/index.html

### Footnotes
### 脚注

[^1]: Open Source Security Foundation OpenSSF course *Security for Software Development Managers (LFD125)*
 https://training.linuxfoundation.org/training/security-for-software-development-managers-lfd125/.

[^2]: OWASP Top Ten for web apps: https://owasp.org/www-project-top-ten/

[^3]: CWE Top 25 for general software: https://cwe.mitre.org/top25/

[^4]: OpenSSF course Developing Secure Software (LFD121): https://training.linuxfoundation.org/training/developing-secure-software-lfd121/

[^5]: https://training.linuxfoundation.org/express-learning/understanding-the-eu-cyber-resilience-act-cra-lfel1001/

[^6]: Concise Guide for Developing More Secure Software: https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software

[^7]: https://baseline.openssf.org/

[^8]: OpenSSF Best Practices badge https://www.bestpractices.dev/

[^9]: OpenSSF Scorecard: https://github.com/ossf/scorecard

[^10]: Concise Guide for Evaluating Open Source Software: https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software

[^11]: OpenSSF SLSA: https://slsa.dev/

[^12]: Guide to Security Tools: https://github.com/ossf/wg-security-tooling/blob/main/guide.md#readme

[^13]: OpenSSF Guide to implementing a coordinated vulnerability disclosure process:
https://github.com/ossf/oss-vulnerability-guide/blob/main/maintainer-guide.md#readme
