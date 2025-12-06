---
icon: chatgpt
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# ChatGPT Basic Usage

ChatGPT is an AI language model capable of understanding and generating natural language text. It can assist with tasks such as writing, editing, summarizing, coding, explaining concepts, generating ideas, analyzing documents, and improving communication. It does not possess personal beliefs or real-time access to external databases; its responses are based on patterns in its training data.

## Create a ChatGPT Account

* Make sure proxy is on through Clash Verge.
{% content-ref url="../clash-verge.md" %}
[../clash-verge.md](../clash-verge.md)
{% endcontent-ref %}

* Visit [https://chatgpt.com/](https://chatgpt.com/) and click "Sign up for free".
* You can choose to either continue with your Google Account or create a new account using your email address.

Now I will introduce some useful use cases with ChatGPT.

{% hint style="danger" %}
### ⚠️ Important Note for PhD Students
### 我思故我在 (That's why we are humans)
While ChatGPT is a powerful assistant for drafting, brainstorming, and clarifying ideas, it should not become a substitute for **critical thinking**, technical reasoning, or original intellectual contributions. As researchers, we must actively exercise our analytical and problem-solving abilities — over-reliance on automated tools risks weakening these essential skills and undermining the rigor expected of doctoral-level work. ChatGPT should therefore be viewed as a supportive aid, not a replacement for deep understanding, creativity, and independent reasoning.

Asking LLMs to directly help you come up with new ideas or directly solve your problem is **strongly not suggested**.
{% endhint %}

## Use Case 1 -- Sentence Polishing

You can request ChatGPT to polish your sentence when writing papers. You can also learn from it. Below is a prompt I frequently use:

> You are an expert academic writing assistant with deep knowledge of computer science terminologies and conventions. From now on, for every sentence I provide, your task is to: 
> 1. Polish the sentence to meet the standards of formal academic writing in computer science, improving clarity, concision, and logical flow without changing the technical meaning. 
> 2. Preserve all technical details and domain-specific terminology. 
> 3. Use a professional and objective tone, avoiding redundancy or overly complex constructions unless necessary for precision. 
> 4. Ensure the result is suitable for inclusion in a peer-reviewed computer science paper. 
> 5. Also, please point out the weaknesses of my writing and explain why you polish it in that way. 
> 6. You are encouraged to use some advanced and academic-sounding words or phrases.

Additionally, you can also instruct ChatGPT to review an entire paragraph to provide suggestions and reveal logical errors. Below is a prompt I frequently use:
> You are an expert academic writing assistant with deep knowledge of computer science terminologies and conventions. From now on, given any paragraph I provide, please help me improve the writing and logic for a research paper. Please also point out the writing problems that I have. Specifically, 
> 1. Enhance clarity, conciseness, and academic tone (if needed). 
> 2. Improve logical flow (e.g., transitions, argument structure). 
> 3. Point out issues (e.g., wordiness, vague phrasing, grammar, or coherence problems). 
> 4. Suggest alternatives where necessary.

## Use Case 2 -- Paper Search

Sometimes, you have an idea and you want to search relevant papers. However, relying on existing search engines (*e.g.*, Google Scholar) may not always provide relevant papers. Therefore, you can ask ChatGPT to help you search for papers. Below is a prompt template I frequently use:
> Please search for some papers demonstrating that <mark>the topic or key idea you want to search </mark>

## Use Case 3 -- Writing Emails

I find that ChatGPT is particularly skilled at writing emails. As long as you provide your request and your current situations, ChatGPT can always write emails with polite and appropriate language. For example,
> I want to apply for a visiting PhD position at Prof. <mark>name</mark>'s group. Based on my CV and the professor's homepage (<mark>the homepage URL of the professor</mark>), please help me write an email for application.

## Use Case 4 -- Review Papers (Be Careful)

Prompts will not be released. You can directly use my customized ChatGPT, namely [PaperGPT](https://chatgpt.com/g/g-693191fca194819186bd34fb1d6ad63e-papergpt)
{% embed url="https://chatgpt.com/g/g-693191fca194819186bd34fb1d6ad63e-papergpt" %}
