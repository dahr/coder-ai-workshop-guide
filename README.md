<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coder AI Workshop Guide</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #090B0B;
            background: #F8F2F1;
            padding: 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: #ffffff;
            border-radius: 12px;
            box-shadow: 0 20px 60px rgba(9,11,11,0.1);
            overflow: hidden;
            border: 1px solid #2F2D33;
        }

        .header {
            background: #ffffff;
            color: #090B0B;
            padding: 40px 30px;
            text-align: center;
            border-bottom: 4px solid #1D4D7D;
        }

        .header-logo {
            max-width: 250px;
            height: auto;
            margin-bottom: 20px;
        }

        .header h1 {
            font-size: 2.5em;
            margin-bottom: 10px;
            color: #090B0B;
        }

        .header p {
            font-size: 1.1em;
            color: #2F2D33;
        }

        .content {
            padding: 40px 30px;
            color: #090B0B;
        }

        h2 {
            color: #1D4D7D;
            margin-top: 40px;
            margin-bottom: 20px;
            font-size: 1.8em;
            border-bottom: 3px solid #1D4D7D;
            padding-bottom: 10px;
        }

        h3 {
            color: #1D4D7D;
            margin-top: 30px;
            margin-bottom: 15px;
            font-size: 1.4em;
        }

        h4 {
            color: #090B0B;
            margin-top: 20px;
            margin-bottom: 10px;
            font-size: 1.1em;
        }

        p, li {
            margin-bottom: 10px;
            color: #2F2D33;
        }

        ul, ol {
            margin-left: 30px;
            margin-bottom: 20px;
        }

        .prompt-box {
            background: #F8F2F1;
            border-left: 4px solid #1D4D7D;
            padding: 20px;
            margin: 20px 0;
            border-radius: 6px;
            position: relative;
        }

        .prompt-box pre {
            background: #18171A;
            color: #F8F2F1;
            padding: 15px;
            border-radius: 6px;
            overflow-x: auto;
            font-size: 0.9em;
            margin-top: 10px;
            border: 1px solid #2F2D33;
        }

        .copy-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #1D4D7D;
            color: #ffffff;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            font-size: 0.85em;
            transition: background 0.3s;
            font-weight: 600;
        }

        .copy-btn:hover {
            background: #005C6A;
        }

        .copy-btn.copied {
            background: #48bb78;
            color: #ffffff;
        }

        .info-box {
            background: #F8F2F1;
            border-left: 4px solid #1D4D7D;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
            color: #2F2D33;
        }

        .warning-box {
            background: #F8F2F1;
            border-left: 4px solid #FF8067;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
            color: #2F2D33;
        }

        .success-box {
            background: #F8F2F1;
            border-left: 4px solid #48bb78;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
            color: #2F2D33;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        th, td {
            border: 1px solid #2F2D33;
            padding: 12px;
            text-align: left;
            color: #090B0B;
        }

        th {
            background: #1D4D7D;
            color: #ffffff;
            font-weight: 600;
        }

        .difficulty-badge {
            display: inline-block;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 0.85em;
            font-weight: bold;
        }

        .beginner {
            background: #48bb78;
            color: #ffffff;
        }

        .intermediate {
            background: #FF8067;
            color: #ffffff;
        }

        .advanced {
            background: #1D4D7D;
            color: #ffffff;
        }

        .checklist {
            list-style: none;
            margin-left: 0;
        }

        .checklist li {
            padding-left: 30px;
            position: relative;
            color: #2F2D33;
        }

        .checklist li:before {
            content: "☐";
            position: absolute;
            left: 0;
            font-size: 1.2em;
            color: #1D4D7D;
        }

        a {
            color: #1D4D7D;
            text-decoration: none;
            font-weight: 500;
        }

        a:hover {
            text-decoration: underline;
            color: #005C6A;
        }

        .nav-toc {
            background: #F8F2F1;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 30px;
            border: 2px solid #1D4D7D;
        }

        .nav-toc h3 {
            margin-top: 0;
            color: #1D4D7D;
        }

        .nav-toc ul {
            margin-left: 20px;
        }

        .nav-toc a {
            color: #2F2D33;
        }

        .nav-toc a:hover {
            color: #1D4D7D;
        }

        @media (max-width: 768px) {
            body {
                padding: 10px;
            }

            .header h1 {
                font-size: 1.8em;
            }

            .content {
                padding: 20px 15px;
            }

            h2 {
                font-size: 1.5em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img src="https://coder.com/brand/images/logo/sections/0/content/1/value/images/0/image.svg" alt="Coder" class="header-logo">
            <h1>AI Workshop Guide</h1>
            <p>Enterprise-Ready AI-Assisted Development with Secure Boundaries</p>
        </div>

        <div class="content">
            <div class="nav-toc">
                <h3>📋 Table of Contents</h3>
                <ul>
                    <li><a href="#overview">Workshop Overview</a></li>
                    <li><a href="#prerequisites">Prerequisites</a></li>
                    <li><a href="#part1">Part 1: Workspace Launch</a></li>
                    <li><a href="#part2">Part 2: Verify Setup & Explore</a></li>
                    <li><a href="#part3">Part 3: Working with Agent Boundaries</a></li>
                    <li><a href="#part4">Part 4: Testing Your Implementation</a></li>
                    <li><a href="#part5">Part 5: Agent Boundary Testing</a></li>
                    <li><a href="#troubleshooting">Troubleshooting Quick Reference</a></li>
                    <li><a href="#bonus">Bonus Challenges</a></li>
                    <li><a href="#resources">Resources & Next Steps</a></li>
                </ul>
            </div>

            <section id="overview">
                <h2>Workshop Overview</h2>
                <p>Participants will use Coder's workspace agents, configured with boundary controls, to collaboratively solve GitHub issues on a React memory card game. This workshop demonstrates enterprise-ready AI-assisted workflows within secure, auditable environments.</p>
            </section>

            <section id="prerequisites">
                <h2>Prerequisites</h2>
                <ul>
                    <li>GitHub Account</li>
                    <li>Workshop Guide</li>
                    <li>Workshop repository: <a href="https://github.com/coder-contrib/memory-card-ai-demo" target="_blank">https://github.com/coder-contrib/memory-card-ai-demo</a> (1st browser tab)</li>
                    <li>Coder: <a href="https://ai.coder.com" target="_blank">https://ai.coder.com</a> (2nd browser tab)</li>
                </ul>
            </section>

            <section id="part1">
                <h2>Part 1: Workspace Launch (5 minutes)</h2>

                <h3>Step 1: Access Coder</h3>
                <ol>
                    <li>Navigate to <a href="https://ai.coder.com" target="_blank">https://ai.coder.com</a></li>
                    <li>Log in with your GitHub account</li>
                </ol>

                <h3>Step 2: Launch Workshop Workspace</h3>
                <ol>
                    <li>Click "Tasks" in the Coder dashboard</li>
                    <li>Select "Memory Game App" from the template dropdown</li>
                    <li>In the "Prompt your AI agent to start a task…" box, type:</li>
                </ol>

                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Start workspace and list issues in the repository by issue number. Analyze each issue thoroughly and await for further prompts.</pre>
                </div>

                <ul>
                    <li>Click the "up" arrow on the bottom right</li>
                    <li>Below the prompt window, you will see a task initializing. Hover over the task and click to get into the workspace</li>
                    <li>Wait for automatic provisioning (~2 minutes). The screen will be briefly blank as the workspace starts up</li>
                </ul>

                <div class="info-box">
                    <strong>What's happening automatically:</strong>
                    <ul style="margin-top: 10px;">
                        <li>Repository is cloned</li>
                        <li>Dependencies are installed</li>
                        <li>Development server starts</li>
                        <li>Issues are loaded into the AI's memory</li>
                        <li>Agent boundaries are automatically configured</li>
                    </ul>
                </div>

                <h3>Step 3: Access Your Workspace</h3>
                <div class="success-box">
                    <p>Once provisioned, you'll see:</p>
                    <ul style="margin-top: 10px;">
                        <li>✅ IDE/Editor ready</li>
                        <li>✅ Terminal access</li>
                        <li>✅ App running at a provided URL</li>
                        <li>✅ AI assistant with issues pre-loaded</li>
                    </ul>
                </div>
                <p>Select the "Preview App" tab to view and start playing the Memory Card Game.</p>
            </section>

            <section id="part2">
                <h2>Part 2: Verify Setup & Explore</h2>

                <h3>Quick Verification</h3>
                <ol>
                    <li><strong>Test the Game:</strong>
                        <ul>
                            <li>Click cards to flip them</li>
                            <li>Match pairs to score points</li>
                            <li>Click "Reset Game" button</li>
                        </ul>
                    </li>
                    <li><strong>Check AI Assistant:</strong>
                        <ul>
                            <li>Open the AI chat panel</li>
                            <li>Verify you see the 6 available issues listed</li>
                        </ul>
                    </li>
                    <li><strong>Review Available Issues:</strong> The AI assistant should display:
                        <ul>
                            <li>Issue #1: Change card back design (Easy)</li>
                            <li>Issue #2: Add difficulty levels</li>
                            <li>Issue #3: Implement high score persistence</li>
                            <li>Issue #4: Create theme selector</li>
                            <li>Issue #5: Add countdown timer</li>
                            <li>Issue #6: Add full difficulty system</li>
                        </ul>
                    </li>
                </ol>
            </section>

            <section id="part3">
                <h2>Part 3: Working with Agent Boundaries</h2>

                <h3>Understanding Your Agent</h3>
                <p>Your workspace's agent comes with specific boundaries:</p>

                <table>
                    <thead>
                        <tr>
                            <th>Purpose</th>
                            <th>Boundaries</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Code editing & testing</td>
                            <td>Read/write access to the project using Node.js toolset</td>
                        </tr>
                        <tr>
                            <td>Building & validation</td>
                            <td>Follow step-by-step workflow for a given project</td>
                        </tr>
                        <tr>
                            <td>Git operations & PRs</td>
                            <td>Execute Git operations only to non-main/master branches</td>
                        </tr>
                    </tbody>
                </table>

                <h3>AI Assistant Prompts for Development</h3>

                <h4>Prompt 1: Select and start an issue</h4>
                <p><em>Best practice: solve one issue at a time</em></p>

                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>I want to work on Issue #[NUMBER]. Please:
1. Review the issue requirements
2. Create a feature branch following the pattern: coder-contrib/issue-[NUMBER]-[description]
3. Explain your implementation approach
4. Start implementing the solution</pre>
                </div>

                <p><strong>Example for Beginners (Issue #1):</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>I want to work on Issue #1 to add a red diamond to card backs. Please:
1. Review the card rendering in App.jsx
2. Create branch: coder-contrib/issue-1-card-back-diamond
3. Modify the card back display to show a red diamond emoji or SVG
4. Ensure it only shows when cards are face down</pre>
                </div>

                <h4>Prompt 2: Implement with Testing</h4>

                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>For Issue #[NUMBER], please:
1. Complete the implementation based on acceptance criteria
2. Test each requirement locally
3. Ensure the game still functions properly
4. Show me the key changes you made</pre>
                </div>

                <p><strong>Example for Intermediate (Issue #5):</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>For Issue #5 (countdown timer), please:
1. Add a 60-second countdown timer that displays prominently
2. Implement lose condition when timer reaches zero
3. Show "Time's Up!" message on timeout
4. Return to start screen after timeout
5. Ensure timer pauses on win and resets on game reset
6. Test all scenarios</pre>
                </div>

                <h4>Prompt 3: Commit and Create PR</h4>

                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Please prepare my work for review:
1. Stage all changes
2. Create a descriptive commit message
3. Push to the feature branch
4. Create a pull request with:
   - Title: "Fix #[NUMBER]: [Brief description]"
   - Description of changes
   - How it addresses the issue
   - Testing performed</pre>
                </div>

                <h3>Sample Implementation Workflows</h3>

                <h4><span class="difficulty-badge beginner">🟢 Beginner</span> Path (Issue #1 or #3)</h4>

                <p><strong>Issue #1 - Card Back Design:</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, let's add a red diamond to the card backs:
1. Locate where card backs are rendered
2. Add a red diamond (♦️) with proper styling
3. Make it large and centered on the card back
4. Test that it only appears on unflipped cards</pre>
                </div>

                <p><strong>Issue #3 - High Score:</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, implement high score tracking:
1. Add state for best score (lowest moves)
2. Use localStorage to persist between sessions
3. Display "Best: X moves" in the UI
4. Update only when current score beats the best
5. Add a running total of games played</pre>
                </div>

                <h4><span class="difficulty-badge intermediate">🟡 Intermediate</span> Path (Issue #2, #4, or #5)</h4>

                <p><strong>Issue #4 - Theme Selector:</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, create a theme selector with these requirements:
1. Add theme options: Animals, Emoji, and Flags
2. Create arrays of matching symbols for each theme
3. Add UI to select theme before game starts
4. Update cards based on selected theme
5. Example animals: 🐶🐱🐭🐹🐰🦊🐻🐼
6. Example flags: 🇺🇸🇬🇧🇫🇷🇩🇪🇯🇵🇧🇷🇨🇦🇦🇺</pre>
                </div>

                <p><strong>Issue #5 - Timer Challenge:</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, implement the countdown timer feature:
1. Create a 60-second countdown
2. Display timer prominently (suggest top-right)
3. Add lose detection at 0 seconds
4. Show modal: "Time's Up! You ran out of time."
5. Include "Play Again" button to restart
6. Timer should pause when game is won</pre>
                </div>

                <h4><span class="difficulty-badge advanced">🔴 Advanced</span> Path (Issue #2 or #6)</h4>

                <p><strong>Issue #2 - Multiple Difficulty Levels:</strong></p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, implement difficulty selection:
1. Add selection UI before game start
2. Create three options:
   - Easy: 4x4 grid (8 pairs)
   - Medium: 6x6 grid (18 pairs)  
   - Hard: 8x8 grid (32 pairs)
3. Dynamically adjust grid CSS
4. Scale card symbols appropriately
5. Display current difficulty during gameplay
6. Allow difficulty change after game completion</pre>
                </div>
            </section>

            <section id="part4">
                <h2>Part 4: Testing Your Implementation</h2>

                <h3>Manual Testing Checklist</h3>
                <p>Run through these tests based on your implemented feature:</p>

                <h4>For All Features:</h4>
                <ul class="checklist">
                    <li>Original game functionality still works</li>
                    <li>No console errors</li>
                    <li>Reset button works properly</li>
                    <li>Win condition still triggers</li>
                </ul>

                <h4>Feature-Specific Tests:</h4>

                <p><strong>Card Back (Issue #1):</strong></p>
                <ul class="checklist">
                    <li>Diamond visible on all unflipped cards</li>
                    <li>Diamond disappears when card flipped</li>
                    <li>Diamond reappears if non-match</li>
                </ul>

                <p><strong>High Score (Issue #3):</strong></p>
                <ul class="checklist">
                    <li>Best score displays</li>
                    <li>Updates only when beaten</li>
                    <li>Persists after page refresh</li>
                    <li>Games played counter increments</li>
                </ul>

                <p><strong>Theme Selector (Issue #4):</strong></p>
                <ul class="checklist">
                    <li>All themes selectable</li>
                    <li>Cards update to match theme</li>
                    <li>Themes have enough unique pairs</li>
                    <li>Theme persists during game</li>
                </ul>

                <p><strong>Timer (Issue #5):</strong></p>
                <ul class="checklist">
                    <li>Starts at 60 seconds</li>
                    <li>Counts down properly</li>
                    <li>Shows lose modal at 0</li>
                    <li>Pauses on win</li>
                    <li>Resets with game</li>
                </ul>

                <p><strong>Difficulty (Issue #2/#6):</strong></p>
                <ul class="checklist">
                    <li>All difficulty levels selectable</li>
                    <li>Grid adjusts properly</li>
                    <li>Correct number of pairs</li>
                    <li>Cards remain clickable</li>
                    <li>Layout is responsive</li>
                </ul>
            </section>

            <section id="part5">
                <h2>Part 5: Agent Boundary Testing (10 minutes)</h2>

                <p>In the prompt chat window, attempt to pull down an application from another repository instance (Bitbucket). Upon execution, the agent will report the request as blocked by Boundary.</p>

                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, Clone https://bitbucket.org/coder-contrib/memory-card-ai-demo.git to /tmp</pre>
                </div>
            </section>

            <section id="troubleshooting">
                <h2>Troubleshooting Quick Reference</h2>

                <h3>Common Issues and Solutions</h3>

                <h4>AI Assistant Not Responding:</h4>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Please check your connection and retry the last command.
If issues persist, refresh the AI chat panel.</pre>
                </div>

                <h4>Code Changes Not Appearing:</h4>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, please:
1. Save all files
2. Restart the development server
3. Clear browser cache and refresh</pre>
                </div>

                <h4>Git Push Errors:</h4>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, please help resolve git authentication:
1. Check my git configuration
2. Verify branch permissions
3. Try pushing again with verbose output</pre>
                </div>

                <h4>Build/Test Failures:</h4>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, please diagnose the build failure:
1. Show me the full error message
2. Identify the root cause
3. Suggest a fix
4. Implement the correction</pre>
                </div>
            </section>

            <section id="bonus">
                <h2>Bonus Challenges (If Time Permits)</h2>

                <h3>Challenge A: Combine Features</h3>
                <p>If you finish early, try combining two issues:</p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, I've completed Issue #[FIRST]. Now let's also implement Issue #[SECOND] 
in the same branch. Make sure both features work together seamlessly.</pre>
                </div>

                <h3>Challenge B: Add Your Own Enhancement</h3>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, I want to add a custom feature not in the issues:
[Describe your feature idea]
Please implement it following the same quality standards.</pre>
                </div>

                <h3>Challenge C: Code Review</h3>
                <p>Exchange PR links with another participant:</p>
                <div class="prompt-box">
                    <button class="copy-btn" onclick="copyPrompt(this)">Copy</button>
                    <pre>Agent, please review this PR: [URL]
1. Check for code quality
2. Verify it meets issue requirements  
3. Suggest any improvements
4. Leave constructive comments</pre>
                </div>
            </section>

            <section id="takeaways">
                <h2>Key Takeaways</h2>
                <p>By the end of this workshop, you will have:</p>
                <ul>
                    <li>✅ Experienced Coder's agent boundaries in action</li>
                    <li>✅ Used AI assistance for real development tasks</li>
                    <li>✅ Created a feature branch and PR</li>
                    <li>✅ Understood enterprise-secure AI development workflows</li>
                </ul>
            </section>

            <section id="resources">
                <h2>Resources & Next Steps</h2>
                <ul>
                    <li>Try Coder Open Source: <a href="https://github.com/orgs/coder" target="_blank">https://github.com/orgs/coder</a></li>
                    <li>Coder Documentation: <a href="https://coder.com/docs" target="_blank">https://coder.com/docs</a></li>
                    <li>Agent Boundaries Guide: <a href="https://coder.com/docs/agents/boundaries" target="_blank">https://coder.com/docs/agents/boundaries</a></li>
                    <li>Workshop Repository: <a href="https://github.com/coder-contrib/memory-card-ai-demo" target="_blank">https://github.com/coder-contrib/memory-card-ai-demo</a></li>
                </ul>
            </section>

            <section id="notes">
                <h2>Notes Section</h2>
                <div class="info-box">
                    <p><em>Use this space for your own notes during the workshop:</em></p>
                    <ul style="margin-top: 10px;">
                        <li><strong>Issue Selected:</strong> #___</li>
                        <li><strong>Branch Name:</strong></li>
                        <li><strong>Challenges Faced:</strong></li>
                        <li><strong>Solutions Found:</strong></li>
                        <li><strong>Ideas for Improvement:</strong></li>
                    </ul>
                </div>
            </section>

            <div style="text-align: center; padding: 40px 0; border-top: 2px solid #eee; margin-top: 40px;">
                <h3>Thank you for participating! 🚀</h3>
                <p style="font-size: 1.1em; color: #666;">Remember, the AI agents are here to augment your development, not replace your creativity. Happy coding!</p>
            </div>
        </div>
    </div>

    <script>
        function copyPrompt(button) {
            const promptBox = button.parentElement;
            const pre = promptBox.querySelector('pre');
            const text = pre.textContent;

            navigator.clipboard.writeText(text).then(() => {
                const originalText = button.textContent;
                button.textContent = '✓ Copied!';
                button.classList.add('copied');
                
                setTimeout(() => {
                    button.textContent = originalText;
                    button.classList.remove('copied');
                }, 2000);
            }).catch(err => {
                console.error('Failed to copy:', err);
                button.textContent = 'Failed';
                setTimeout(() => {
                    button.textContent = 'Copy';
                }, 2000);
            });
        }

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
