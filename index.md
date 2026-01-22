# h1 – Should Tero wear a helmet?

## Course
Information Security - ICI002AS2AE-3006

## Author
Paul Bosire

## Threat Modeling Summaries

### Threat Modeling Manifesto
- Threat modeling is about understanding and familiarizing oneself with risks. It is important because it allows people to highlight issues in a system and mitigate them.
- It is meant to be used by many roles and it is fairly simple to implement even outside of developing.
- Often times there are certain values that are necessary to assess in order to achieve a good, working result, rather than "just a result", and they usually are defined by the context of the modeling.
- Having many viewpoints in modeling more often brings useful, different viewpoints to the model, that can be used to build an ideal one.
- Threat modeling should stay focused on the whole system rather than getting stuck on one detail as this might steer it away from serving its purpose, and end up becoming too shallow.
- I wonder if a team with several people like myself, who tend to easily get within their own heads and overthink possible negative outcomes, would become more productive during threat modeling? Or would it work in the opposite way?

Source: Threat Modeling Manifesto https://www.threatmodelingmanifesto.org

### World’s Shortest Threat Modeling Course
- We do threat modeling at an early stage in order to be able to safely anticipate things that can have a negative impact on what we are working with before it gets the chance to pose as something that can get out of hand, whilst making them easy to address.
- There are four key questions that are to be answered throughout threat modeling: what are we working on, what can go wrong, what should we do about them, and whether we did a good job.
- Sketching systems and data flows helps teams comprehend how components, data and trust boundaries interact.
- STRIDE is a set of common threats that are good to take note of and apply to threat modeling, as they help structure thinking and mitigate missing obvious risks
- Tracking work will help us stay up to date with identified risks and manage them using basic risk management practices.
- Lastly, a threat model can potentially be considered good if it answers the core questions and is worth recommending to others.

I feel that it is very important to take all forms of feedback into account and listen to them carefully as it can teach us a lot that might otherwise be overlooked, and that can help us improve ourselves.

Source: World's Shortest Threat Modeling Course https://courses.shostack.org/courses/world-s-shortest-threat-modeling

### OWASP Threat Modeling Cheat Sheet
- Threat modeling is a largely structured process to identify, evaluate, and take action towards potential security risks in a system.
- Key steps include modeling the system, identifying threats, deciding how to respond to them, and reviewing results.
- There are several options for mitigation that include: reducing risk, transferring it, accepting it, or eliminating it entirely if possible.
- Threat modeling should be iterative and revisited as the system evolves, and it should involve multiple different perspectives.
- Reviewing and validating the model helps ensure it reflects real risks and maintains trust.
- Using the framework helps teams prioritize high-risk areas and make better security decisions.

I feel that regardless of a projects size, following a structured threat model can prevent serious issues before they happen and get out of hand.

Source: OWASP Threat Modeling Cheat Sheet https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html

## Darknet Diaries Podcast
- I chose episode 29: Stuxnet for the reason that it really peaked my interest. It is about a worm that targeted industrial control systems that ended up causing severe harm to uranium enrichment infrastructure.
- The episode explained how Stuxnet was designed to cause physical destruction while hiding as normal digital activity, that really went above and beyond to show the extent of harm attackers can cause on a cyber level.
- The case proved how cyber weapons can be used in geopolitical conflicts that exceed typical crime stories. When an attacker has the appropriate resources and knowledge, they can orchestrate attacks that go deeper and deeper as tight security measures are still being bypassed.
- Listening to the episode highlights how large and real the impact that malware can have on computers and even infrastructures and national security is.

I feel that the episode went well in-depth about the Stuxnet malware and proved how information security extends not only to data protection but also to properly understanding how broad the harm that attackers can cause can potentially be.

Source: Darknet Diaries Episode 29: Stuxnet https://darknetdiaries.com/episode/29/

## Security Hygiene
- Always use strong and unique passwords for different services and store them somewhere safe like a password manager.
- If possible, use 2-factor authentication with all services.
- Keep devices, systems and applications up to date with updates.
- Make regular backups of important data and store them securely for example on an external hard drive.
- Be wary of suspicious links, emails and attachments, and do not download or install anything you are not confident about.
- Never give out your personal information/login credentials to others.

## Threat Model – Imaginary Company
Company details:
- A small online food delivery service. Customers place orders through a web app, and couriers deliver food from partner restaurants. The business depends on reliable service, customer trust, and secure handling of personal and payment info.

What are we working on?
Main assets:
- Customer personal information (names, addressess, phone numbers)
- Payment information
- Order and delivery system availability
- Company reputation and trust

Key systems:
- Customer-facing web app
- Backend server that processes orders
- Database storing customer and order data
- Third-party payment processing services

From the customer’s perspective, the most important touchpoints are placing an order, paying for it, and receiving the food on time.

What can go wrong?
Using STRIDE as a reference:
- Spoofing: Attackers could potentially impersonate users or delivery drivers
- Tampering: Orders or prices could be modified during or before delivery
- Information Disclosure: Customer data could be leaked through vulnerabilites
- Denial of Service: The website could be taken offline preventing orders from going through
- Elevation of Privilege: An attacker could gain admin access through weak credentials

The biggest risks are data breaches and service downtime, as both would directly impact revenue as well as customer trust.

What are we going to do about it?
- Reduce attack extent by limiting exposed services and interfaces
- Enforce strong authentication and access control based on roles
- Use encryption for sensitive data while delivering or limit access/visibility to minimal required to carry out orders
- Rely on trusted third-party payment providers to transfer financial risk
- Accept some risks with lowest impact if mitigation costs outweigh benefits

Did we do a good job?
The threat model would be reviewed regularly even when new features are added. Security audits, testing and continuous monitoring help make sure that the model stays relevant. It is never a one-and-done deal, it has to be upkept for the process to serve its functions.

## Sources
- Karvinen 2024: Information Security Course  
  https://terokarvinen.com/information-security/
- Braiterman Z., Shostack A.: Threat Modeling Manifesto
  https://www.threatmodelingmanifesto.org
- Shostack A.: World's Shortest Threat Modeling Course
  https://courses.shostack.org/courses/world-s-shortest-threat-modeling
- Cheat Sheets Series Team: OWASP Threat Modeling Cheat Sheet
  https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html
- Rhysider J.: Darknet Diaries Episode 29: Stuxnet
  https://darknetdiaries.com/episode/29/
