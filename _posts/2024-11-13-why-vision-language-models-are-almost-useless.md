---
title: "Why Vision-Language Models Are (Almost) Useless"
description: >-
  Vision-language models produce fluent text but not structured data, which is
  why they stall in real systems. The fix is moving from vision-to-language to
  vision-to-structured-output.
date: 2024-11-13
categories: [engineering]
tags: [vlms, structured-output, production, florence-2]
---

The advent of Vision-Language Models (VLMs) promised a revolution in AI, offering a seamless blend of visual and linguistic understanding. These models showcased the ability to generate descriptive captions for images, answer visual questions, and even assist in complex tasks involving both vision and language. Yet, beyond the impressive demos and proof-of-concept projects (POCs), their real-world utility often falls short. Let's delve into why VLMs struggle in practical applications, what limitations they face, and explore a path forward that could make them genuinely useful for industrial and practical needs.

<!--more-->

## The Fundamental Flaw

Useful AI models transform unstructured data into structured, actionable outputs that can easily integrate into automated systems. VLMs, however, often generate unstructured text descriptions, which limit their direct applicability. For example, a VLM might generate a caption like "A person is sitting at a desk, using a computer," but this text output lacks the structured data format required for downstream automation. Without structured data, these models struggle to interface with systems, trigger automated actions, or even provide consistent, predictable information that can be directly utilized by machines.

Another issue with VLMs is that their outputs are inherently probabilistic and often require human intervention to verify. In real-world environments, such as manufacturing or healthcare, the need for manual verification can be a major drawback. Decision-makers need AI outputs that are not only accurate but also reliably formatted in a way that can be understood by other software and machines, without relying on additional natural language processing (NLP) steps. This fundamental flaw restricts the scalability and effectiveness of VLMs in domains where automation is key.

## The Solution: Vision to Structured Language

To unlock the potential of VLMs, we must shift towards Vision-Structured Language Models (VSLMs), which transform visual inputs into structured data formats like JSON. By producing structured outputs, we can bridge the gap between perception and action, making AI more relevant and applicable in real-world scenarios. This approach demands high-quality, predictable outputs that can be verified and easily used by existing software systems for decision-making and automation.

Imagine a VSLM that, instead of producing a generic description, outputs a well-structured JSON object, detailing the objects, actions, and contexts present in an image. For instance, instead of generating "A person wearing a blue shirt is riding a bicycle," the model could output:

```json
{
  "object": "person",
  "clothing": "blue shirt",
  "activity": "riding",
  "vehicle": "bicycle",
  "speed": 15,
  "distance": 100
}
```

Such a structured representation can be directly used by other systems to trigger automated actions, such as generating alerts, initiating workflows, or providing clear analytics. Structured data is inherently easier to integrate into existing systems and can significantly reduce the friction between AI perception and practical utility.

Some models, particularly Florence-2, represent significant progress in this direction. Florence-2 has demonstrated improved capabilities in bridging visual inputs to structured language outputs, showing promise in delivering more actionable and structured insights from complex visual data. Its architecture is specifically designed to enhance accuracy while providing outputs that are easier to integrate into downstream systems, making it an important milestone towards the vision of Vision-Structured Language Models.

## Why This Shift Matters

Moving from Vision-Language Models to Vision-Structured Language Models isn't just a technical upgrade. It's a fundamental shift in how we think about applying AI. This transition is about making AI practical and actionable for industries that thrive on efficiency, automation, and seamless data integration. Whether it's logistics, where identifying and categorizing goods accurately can streamline operations, or healthcare, where structured data can be used to monitor patient conditions in real-time, VSLMs have the potential to dramatically enhance productivity and decision-making.

Additionally, this transition could pave the way for better integration into existing enterprise systems. Unlike free-form text, structured outputs can be directly used by databases, management software, and automation tools without needing complex NLP parsing or human oversight. Structured data is inherently more predictable, easier to validate, and less prone to ambiguity, which makes it a much more reliable component for building automated solutions.

I'm curious to hear from others working with AI. Do you see similar limitations in current VLM approaches?
