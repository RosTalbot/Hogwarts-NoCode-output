# 🧙‍♀️ Hogwarts Acceptance Letter – n8n AI Agent

This no-code AI agent creates a fully personalized Hogwarts acceptance letter based on a short quiz. Built in [n8n](https://n8n.io), it uses OpenAI’s GPT-4 to generate a warm, magical letter that’s then automatically delivered via email.


## 💡 Project Goal

Build an AI agent that:
1. Collects quiz answers from a user
2. Passes them to GPT-4 via n8n
3. Generates a heartfelt Hogwarts acceptance letter
4. Emails the final letter using HTML formatting


## 🙌 Credits & Attribution

This project was inspired by guidance from Kaouthar (Lonely Octopus AI Agent Bootcamp). Her original instructions helped shape the early version of this workflow. I followed her outline closely but made a few key changes for functionality and formatting for my specific agent.



## 🧪 Changes From Original

Kaouthar’s version used a basic HTML output directly inside the OpenAI prompt and displayed the letter in a browser via Replit. 

When I tried this setup:
- I couldn’t get Replit to run reliably on my machine
- I was struggling with output formatting bugs (extra line breaks, HTML tag issues)

So I pivoted to email delivery - which made more sense since this is a Hogwarts **letter**.
I used Gmail’s Send Email node inside n8n with custom HTML injection for:
- A more immersive email layout
- Better paragraph spacing
- A stylized closing signature block (for Professor Goodberry, of course!)


## 🧰 Tools Used

- **n8n**: For orchestrating the workflow  
- **OpenAI GPT-4**: For generating the letter content  
- **Gmail (Send Email node)**: To deliver the final formatted letter  
- **Typeform**: Used for quiz input (in earlier versions; future versions may use n8n’s built-in form node)



## 🧵 Prompt Design (User Message)

The GPT prompt was rewritten using best practices from the Bootcamp — separating role, task, input, output, and constraints. The final version instructed the model to:

- Skip the greeting and signature (handled via HTML template)
- Return only the letter body
- Emphasize tone: poetic, in-world, moonlit, and immersive

Prompt: [`hogwarts_acceptance_letter_prompt.md`](hogwarts_acceptance_letter_prompt.md)



## 📂 Files Included

- `Hogwarts-nocode-output-workflow.json` – full working n8n build  
- `hogwarts_acceptance_letter_prompt.md` – GPT prompt used for formatting and tone  
- `screenshots/` – visual previews of the form, JSON output, and final email layout  
- `README.md` – you’re reading it!
> 🔒 **Note:** The workflow JSON has been sanitized for public sharing.  
> Personal emails, credential IDs, and webhook URLs have been replaced with placeholder text.  
> Please update these with your own values before use.

## 🖼️ Sample Screenshots

All visuals are included in the `screenshots/` folder to show the flow from form → JSON → final email.



## 🔮 Future Plans

- Swap Typeform trigger for native n8n form to avoid submission limits  
- Add option for mobile-friendly HTML styling  
- Consider embedding this as a downloadable letter via PDF



🦉 Special thanks again to Kaouthar for the original concept.
