---
layout: page
title: Contact
---

# Get In Touch

I'd love to hear from you! Whether you have questions about SOPs, want to discuss the LYMPHA language, share a procedural challenge, or explore partnership opportunities.

## Contact Form

<form action="https://formspree.io/f/myzpozvl" method="POST" class="contact-form">
    <div class="form-group">
        <label for="name">Name *</label>
        <input type="text" id="name" name="name" required aria-describedby="name-help">
        <small id="name-help">Your full name</small>
    </div>
    
    <div class="form-group">
        <label for="email">Email *</label>
        <input type="email" id="email" name="email" required aria-describedby="email-help">
        <small id="email-help">Your email address for replies</small>
    </div>
    
    <div class="form-group">
        <label for="company">Company/Organization</label>
        <input type="text" id="company" name="company" aria-describedby="company-help">
        <small id="company-help">Optional: Your company or organization</small>
    </div>
    
    <div class="form-group">
        <label for="subject">Subject *</label>
        <select id="subject" name="subject" required aria-describedby="subject-help">
            <option value="">Select a topic...</option>
            <option value="sop-challenge">I have an SOP challenge</option>
            <option value="lympha-question">Question about LYMPHA language</option>
            <option value="ActCalc-demo">Interested in ActCalc demo</option>
            <option value="partnership">Partnership opportunity</option>
            <option value="guest-post">Guest post proposal</option>
            <option value="sponsorship">Sponsorship inquiry</option>
            <option value="other">Other</option>
        </select>
        <small id="subject-help">Help me categorize your message</small>
    </div>
    
    <div class="form-group">
        <label for="message">Message *</label>
        <textarea id="message" name="message" rows="6" required aria-describedby="message-help" placeholder="Tell me about your ActCalcl challenges, questions, or ideas..."></textarea>
        <small id="message-help">Please be as specific as possible</small>
    </div>
    
    <div class="form-group">
        <button type="submit">Send Message</button>
    </div>
</form>

## Other Ways to Connect

**Professional Networking:**
- [LinkedIn](https://linkedin.com/in/rickard-hultgren) - Best for business discussions and partnerships

**Development & Code:**
- [GitHub](https://github.com/rickardhultgren) - Open source projects and code samples

**Response Time:**
I typically respond within 24-48 hours during business days. For urgent matters, please mention it in your message subject.

## What I'm Looking For

**SOP Challenges:**
- Complex ActCalcl decisions that are hard to automate
- Industry-specific workflow problems
- Manual processes that need digitization

**Partnership Opportunities:**
- Tool integrations with ActCalc platform
- Content collaboration and guest posting
- Affiliate partnerships with complementary tools

**Community Contributions:**
- Real-world SOP examples and case studies
- LYMPHA language feedback and suggestions
- Industry expertise and domain knowledge

---

*All messages are handled confidentially. If you're sharing proprietary process information, please mention if you'd prefer to sign an NDA before detailed discussions.*

<style>
.contact-form {
    max-width: 600px;
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group small {
    display: block;
    color: var(--text-secondary);
    font-size: 0.875rem;
    margin-top: 0.25rem;
}

select {
    width: 100%;
    padding: 0.75rem;
    background-color: var(--surface-color);
    border: 1px solid var(--border-color);
    border-radius: 0.25rem;
    color: var(--text-primary);
    font-family: inherit;
}

select:focus {
    outline: 2px solid var(--text-accent);
    border-color: var(--text-accent);
}

textarea {
    resize: vertical;
    min-height: 120px;
}
</style>

---
<!-- _posts/2025-08-12-from-kitchen-to-code-lympha-recipe-sop.md -->
---
layout: post
title: "From Kitchen to Code: A LYMPHA Language Recipe for SOP"
date: 2025-08-12 01:00:00 +0200
author: "Rickard Hultgren"
tags: [sop, lympha, recipe, introduction]
---

Welcome to the first post on ActCalc, a blog dedicated to the art and science of Standard Operating Procedures (SOP). As a foundational principle in many fields, from manufacturing to medicine, a well-defined SOP ensures consistency, accuracy, and reliability. But what if we could make these procedures more formal, more structured, and even machine-readable?

This is where languages like **LYMPHA** come in. Originally designed for clinical workflows, LYMPHA provides a syntax for defining a series of events, or statements, which can be either **procedures** (actions to be executed) or **factors** (data points or conditions). Each statement is linked in a logical flow, much like a flow chart, but expressed in a clean, code-like format.

To illustrate how powerful this can be, let's move out of the clinic and into the kitchen. We'll use a classic **chocolate chip cookie recipe** to demonstrate how to implement a real-world SOP using the LYMPHA language. This recipe is a perfect example because it has a clear, sequential flow and depends on specific conditions (having all the ingredients).

## Understanding the LYMPHA Components in Our Recipe

Before we write the code, let's break down the recipe into LYMPHA's core concepts:

* **Factors (Conditions):** These are our ingredients. In the LYMPHA syntax, factors end with a question mark (`?`). We'll create a factor for each essential ingredient and a binary factor to check if they are all ready. This ensures we don't start the process without everything we need.
* **Procedures (Steps):** These are the actions we take to make the cookies. In LYMPHA, procedures end with a full stop (`.`). The flow of the recipe is represented by a series of these procedures connected by `->`.

## The LYMPHA Recipe Implementation

Here is the full recipe translated into the LYMPHA language. The flow begins with checking our factors and then moves through each step of the baking process.

### 1. Define the Factors (Ingredients Check)

```lympha
butter_softened? = 1 ;
brown_sugar_available? = 1 ;
white_sugar_available? = 1 ;
eggs_available? = 1 ;
vanilla_extract_available? = 1 ;
flour_available? = 1 ;
baking_soda_available? = 1 ;
salt_available? = 1 ;
chocolate_chips_available? = 1 ;

all_ingredients_ready? = 9 == |{butter_softened?, brown_sugar_available?, white_sugar_available?, eggs_available?, vanilla_extract_available?, flour_available?, baking_soda_available?, salt_available?, chocolate_chips_available?}| ;
```

In this section, we've assigned a value of `1` to each ingredient factor, indicating they are present. The final factor, `all_ingredients_ready?`, is a binary check that becomes `1` only if all nine ingredients are available.

### 2. Define the Procedures (Baking Steps)

```lympha
preheat_oven. -> prep_baking_sheet. ->
cream_butter_and_sugars. ->
beat_in_eggs_and_vanilla. ->
whisk_dry_ingredients. ->
combine_wet_and_dry_ingredients. ->
fold_in_chocolate_chips. ->
drop_rounded_tablespoons. ->
bake_for_10-12_minutes. ->
cool_on_wire_rack. ;
```

This is the core of our recipe. It's a clean, linear workflow. Each procedure will only be executed if the preceding one has successfully completed. This perfectly models the step-by-step nature of following a recipe.

## Why Does This Matter?

By using a structured language like LYMPHA, we are not just writing down instructions; we are creating a formal, verifiable model of a process. This approach offers several advantages:

* **Clarity:** The syntax enforces a strict, unambiguous definition of each step and condition.
* **Consistency:** A LYMPHA-based SOP ensures every execution of the procedure follows the exact same path.
* **Automation:** In a real-world scenario, this kind of code could be used to drive automated systems or provide interactive checklists, ensuring no step is missed.

## Real-World Applications

While our cookie recipe is charming, the same principles apply to critical industrial processes:

- **Chemical safety procedures** where missing a step could be dangerous
- **Quality control workflows** where consistency determines product reliability  
- **Medical protocols** where precision saves lives
- **Manufacturing processes** where efficiency and repeatability matter

## What's Next?

From clinical trials to baking cookies, the principles of a good SOP are universal. By exploring tools like the LYMPHA language, we can elevate our understanding and implementation of these critical workflows.

In upcoming posts, we'll dive deeper into:
- Threshold-based decision making in LYMPHA
- Real industrial SOP challenges and solutions
- How the ActCalc platform makes LYMPHA accessible to domain experts

---

*Have a ActCalcl challenge you'd like to see translated into LYMPHA? [Share it with me](/contact/) and I might feature it in a future post!*

---
<!-- _posts/2024-08-15-welcome-to-ActCalc-blog.md -->
---
layout: post
title: "Welcome to the ActCalc Blog"
date: 2024-08-15 10:00:00 +0200
author: "Rickard Hultgren"
tags: [introduction, ActCalc, lympha, sop]
---

Welcome to the ActCalc Blog! I'm Rickard Hultgren, and I'm excited to share this journey with you as we explore the fascinating world of Standard Operating Procedures (SOPs), process automation, and the revolutionary LYMPHA programming language.

## Why This Blog Exists

Every day, domain experts across industries face the same challenge: they know *what* needs to be done and *how* to do it, but translating that knowledge into systems that computers can execute requires technical expertise they don't have. This gap between domain knowledge and technical implementation is what inspired me to create ActCalc.

This blog serves several purposes:

**Knowledge Sharing:** Real solutions to ActCalcl challenges across industries
**Community Building:** Connecting domain experts with process automation enthusiasts  
**Transparent Development:** Behind-the-scenes updates about building ActCalc
**Market Validation:** Understanding which ActCalcl problems need solving most urgently

## What We'll Cover

### Standard Operating Procedures in Action
- Real-world SOP challenges from chemical safety to quality control
- Best practices for documenting complex decision trees
- Case studies of successful ActCalcl automation

### LYMPHA Language Deep Dives  
- How threshold-based decisions work in practice
- Parameter-centric programming for domain experts
- Converting prose procedures into executable logic

### Industry Applications
- **KemSäker**: Chemical safety and risk management procedures
- **KvalKontroll**: Quality control and manufacturing processes  
- **FlödeStyr**: General process management across sectors

### Tool Integration & Reviews
I'll be exploring tools that complement ActCalcl work - workflow automation platforms, quality management systems, documentation tools, and more. Some of these reviews will include affiliate partnerships, which help support this blog while providing you with valuable insights.

## The LYMPHA Difference

Traditional programming languages follow a linear "start-process-end" structure, but ActCalcl work is different. Decisions are made continuously based on current conditions, measurements, and parameters. That's why LYMPHA uses:

- **Threshold-based decisions** instead of rigid if-then statements
- **Parameter-centric structure** that mirrors how experts actually think
- **Concurrent procedure processing** for complex, interdependent workflows

## Join the Conversation

This isn't just a blog - it's the beginning of a community. I want to hear about:
- Your most challenging ActCalcl automation problems
- Industries where SOPs are critical but hard to digitize  
- Tools and workflows you're already using
- Ideas for making domain expertise more accessible

## What's Coming

Over the next few weeks, you can expect:
- **SOP Sunday**: Weekly breakdowns of interesting ActCalcl challenges
- **Industry Spotlights**: Deep dives into sector-specific process needs
- **Tool Tuesday**: Reviews and integrations with complementary platforms
- **Behind the Code**: Updates on ActCalc development progress

## Get Involved

Have a ActCalcl challenge you'd like me to tackle? An industry perspective to share? A tool you think I should review? [Get in touch](/contact/) - I'd love to hear from you.

You can also follow along on [LinkedIn](https://linkedin.com/in/rickard-hultgren) and [GitHub](https://github.com/rickardhultgren) for updates and code samples.

---

*Next week: I'll be breaking down a real chemical safety procedure and showing how LYMPHA's threshold-based approach makes it more intuitive than traditional programming. Stay tuned!*