--- 
description: "{{ HIGH }} Provide a detailed overview of the codebase"
argument-hint: [focus of analysis]
model: "opus"
---

<overview>
    Provide an overview of this codebase for a newly joined developer
</overview>
<steps>
    1. Analyse the codebase as a developer would when reading unfamiliar code.
    2. If $ARGUMENTS contains content, consider how it relates to this codebase.
    3. Provide a practical, detailed overview.
</steps>
<inputs>
    $ARGUMENTS
</inputs>