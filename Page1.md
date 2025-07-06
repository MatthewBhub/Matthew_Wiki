#literature #AI
**Source:**  
[Tina Huang’s 20-min summary of Google’s 9-hour course](https://youtu.be/p09yRj47kNM?si=eVNECvSz9iLNI6V9)  
**Course Structure:** 4 Modules  
**Main Frameworks:**  
- **Prompt Design:** Task, Context, References, Evaluate, Iterate  
  → Mnemonic: *Tiny Crabs Ride Enormous Iguanas*  
- **Prompt Iteration:** Revisit, Simplify, Reframe, Constrain  
  → Mnemonic: *Ramen Saves Tragic Idiots*

---

## 🧠 Module 1: Prompting Fundamentals

### 🎯 TASK  
Define what you want the AI to do.  
```

"Summarise this research article in 3 bullet points."

```

### 📚 CONTEXT  
Provide background or constraints.  
```

"You are a PhD student summarising for a journal club."

```

### 🔁 REFERENCES  
Give examples or desired output formats.  
```

Example output:

- Key finding 1
    
- Key finding 2
    
- Key finding 3
    

```

### ✅ EVALUATE  
Review the output for relevance, clarity, tone, accuracy.  
```

"Did it capture the main points without fluff?"

```

### 🔧 ITERATE  
Adjust the prompt based on the output.  
```

1st try: "Summarize the article."  
→ Too vague  
2nd try: "Summarize in 3 bullet points for undergrads."  
→ Better tone & clarity

```

---

## 🔁 Prompt Iteration Techniques

### 1. 🔁 REVISIT  
Re-add missing elements (task/context/persona).  
```

Forgot to specify audience → add “for high school students.”

```

### 2. ✂️ SIMPLIFY  
Break complex prompts into simpler sentences.  
```

❌ "As a seasoned financial expert, provide a concise summary of Q4, ensuring inclusion of key metrics, market factors, and projections."  
✅ "You're a finance expert. Summarize Q4. Include key metrics. Mention market trends. Add next quarter projections."

```

### 3. 🔄 REFRAME  
Change the way you ask (e.g., analogy, story, dialogue).  
```

"Explain AI overfitting like a bedtime story."

```

### 4. 🧱 CONSTRAIN  
Add word limits, formats, tone restrictions.  
```

"Write in exactly 3 bullet points, no more than 10 words each."

```

---

## 🖼️ Multimodal Prompting

AI accepts **text, images, video, audio, code**.  
Still apply the 5-step framework.  
```

"You're a UX designer. Analyze this screenshot [image]. Suggest 3 UI improvements based on accessibility standards."

```

---

## ⚠️ Responsible Use

- Don’t blindly trust outputs → **fact-check**  
- Avoid private/sensitive info  
- Use **checklist** for ethics (bias, inclusivity, safety)  
```

"Does this job ad avoid gendered language?"  
→ Ask AI to check for biased phrasing.

```

---

## 🛠️ Module 2: Prompts for Everyday Work

```

"Write a professional email declining a meeting politely."

"Summarise this Zoom transcript in bullet points for a team update."

"Give 5 name ideas for a new productivity app targeting students."

"Make a table comparing free vs paid AI tools by features."

```

---

## 📊 Module 3: Data + Presentations

```

"Write a Google Sheets formula to count cells with dates in the past."

"What are the top 3 trends in this sales data [attach CSV]?"

"Generate slide titles and bullet points for a pitch on 'AI in education'."

```

---

## 🧠 Module 4: Creative & Expert Prompts

### Prompt Chaining  
Break down tasks into sequential prompts.  
```

1. "Write 5 blog title ideas."
    
2. "Expand idea #3 into a full outline."
    
3. "Now draft the intro paragraph."
    

```

### Chain of Thought (CoT)  
```

"Explain your reasoning as you solve this math problem."

```

### Tree of Thought (ToT)  
```

"List 3 different approaches to improve app retention. Evaluate pros/cons for each."

```

### Meta-Prompting  
```

"Help me design a prompt to generate social media ideas for a travel brand."

```

---

## 👥 Agents

Give detailed role + rules so AI behaves as a specific character.  
```

"You are a picky book editor.  
Your task: critique this short story for grammar, tone, and structure.  
Stop when all paragraphs are covered. Be blunt."

```

---

## ✅ Final Takeaway

> Build prompts like structured instructions. Always refine.  
> Use frameworks: TCR-EI + RSR-C  
> Examples & constraints make a huge difference.
