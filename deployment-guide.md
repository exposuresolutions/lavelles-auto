# Deployment & Automation Guide

## 1. Current Status
We have updated the `feedback-survey.html` with:
*   **Floating Social Icons:** WhatsApp, Snapchat, Telegram, Facebook (Fixed right side).
*   **New "Upgrade Philosophy" Section:** Educating users about upgrading suspension/tyres for Achill roads.
*   **Expanded Share Options:** Added Snapchat and Telegram to the share buttons.

## 2. How to Deploy These Changes (Manual)
1.  Open `Agents/EthanLavelleMechanics/feedback-survey.html` in VS Code.
2.  Copy the entire code.
3.  Go to GoHighLevel -> Sites -> Funnels -> Lavelle's Auto -> Feedback Step.
4.  Edit the page -> Open the "Custom Code" element.
5.  Paste the new code -> Save -> Preview.

## 3. Future Automation: "The Fetch Method"
To avoid manually copying and pasting code every time we make a change, we can set up a "Fetch" system.

### Concept
Instead of pasting the *entire* HTML into GHL, we paste a small "Loader Script". This script grabs the latest code from a file hosted on the web (e.g., GitHub Pages or a dedicated server) and injects it into the page.

### Step-by-Step Setup

**Step A: Host the Code**
1.  Push this repository to GitHub.
2.  Enable **GitHub Pages** for the repository (Settings -> Pages -> Source: Main).
3.  Your file will be available at: `https://your-username.github.io/repo-name/Agents/EthanLavelleMechanics/feedback-survey.html`

**Step B: The Loader Script (Put this in GHL)**
Replace the massive HTML block in GHL with just this:

```html
<div id="dynamic-content">
    <div style="text-align:center; padding: 50px;">
        <h2>Loading Survey...</h2>
        <p>Please wait a moment.</p>
    </div>
</div>

<script>
    // The URL where your raw HTML file lives
    const SOURCE_URL = 'https://exposuresolutions.github.io/lavelles-auto/Agents/EthanLavelleMechanics/feedback-survey.html';

    fetch(SOURCE_URL)
        .then(response => response.text())
        .then(html => {
            // Inject the HTML
            document.open();
            document.write(html);
            document.close();
        })
        .catch(err => {
            console.error('Failed to load content:', err);
            document.getElementById('dynamic-content').innerHTML = '<h3>Error loading content. Please refresh.</h3>';
        });
</script>
```

### Benefits
*   **Instant Updates:** As soon as you `git push` to GitHub, the live site updates automatically.
*   **Version Control:** You have a history of all changes in Git.
*   **No GHL Login Needed:** You don't need to open the GHL editor for code changes.

### Risks
*   **Caching:** GitHub Pages can take 1-2 minutes to update.
*   **CORS:** You might need to ensure the host allows requests from your domain (GitHub Pages usually does).

## 4. Next Steps for Project
1.  **Deploy the Survey:** Get the link to Ethan so he can start sharing it.
2.  **Review Data:** Watch the console logs (or connect a webhook) to see what names/domains people prefer.
3.  **Finalize Domain:** Buy the winning domain (e.g., `lavellesauto.ie`).
4.  **Build the "Upgrade Package":** If the survey shows interest, create a dedicated landing page for the "Achill Road Ready" package.
