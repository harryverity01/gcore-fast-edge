# gcore-fast-edge
ACT ONE: THE COLD OPEN
[0:00 – 0:30]
[HOOK — TANGENTIAL COLD OPEN]
(On screen: a simple heading that reads "About Us" in clean text.)
This costs three tokens.
(On screen: the same heading, but now wrapped in full HTML — <h2 class="section-title" id="about">About Us</h2> — surrounded by div wrappers, nav bars, and script tags.)
This costs fifteen.
Same two words. Five times the price. And every single time an AI agent visits your website — and by the way this is now happening about eight billion times a month — it's paying fifteen-tokens, not three. For two words.
(Beat.)
But not for long. The web is being rebuilt for AI and today we’re looking at one inataitve that you can implement today to prepare for the new world. 
[OPEN LOOP 1 — Who is the web being rebuilt for?]

[0:30 – 1:30]
[THESIS / STAKES]
The month Gcore has launched a feature that lets any website on their network serve a completely different version of itself to AI systems. The same content, stripped down to its skeleton.
This is Markdown for Agents.
Google's most prominent search advocate has called this  "a stupid idea."
Is he right? I think you aready know what my answer is going to be.
[OPEN LOOP 2 — Is Google right? We'll come back to this.]
This is a story about the future of the internet and one about compute and energy and whether your website exists at all in the future we are building. 

ACT TWO: THE HISTORY NOBODY ASKED FOR (BUT NEEDS)
[1:30 – 3:30]
[RETENTION RISK — Keep this section to 90 seconds max. History is context, not content.]
(On screen: timeline visual, starting in 1991.)
To understand why this matters, we need to go back to 1991. To a decision made in a physics lab in Switzerland thirty-five years ago. One man is the reason your AI agent is wasting money right now.
Tim Berners-Lee invented HTML for one simple reason: he wanted physicists at CERN to be able to click between documents. That's it. Hyperlinks between text files. The entire purpose of HyperText Markup Language was to let one person see what was connected to what. Headings. Paragraphs. Links. Done.
And for about five years, that's all the web was. Black text on a grey background. No styling. No animation. No cookie banners asking if you accept cookies in seventeen different jurisdictions.
(Beat. Dry.)
Then we wanted it to look nice. So we added CSS for styling. Then we wanted it to do things. So we added JavaScript for interactivity. Then we wanted it to sell things. So we added tracking pixels, analytics scripts, ad injection frameworks, consent management platforms, A/B testing libraries, chat widgets, notification pop-ups, and — God help us all — auto-playing video.
A technology designed to link physics papers now takes an average of 2.5 megabytes to load a single webpage. The YouTube page you're watching this on right now? It loads more code just to render the like button and comments section than Tim Berners-Lee's entire first website weighed
[OPEN LOOP 3 — But here's the number that changes everything. We'll get to it.]
None of this was a problem when the only things reading websites were humans with browsers and mice. But something has changed.

[3:30 – 5:30]
ACT THREE: THE MACHINES START READING
In March 2026, Cloudflare CEO Matthew Prince stood on a stage at SXSW and said something that made a lot of infrastructure engineers quietly update their resumes: AI bot traffic will exceed human web traffic by 2027.
That is a staggering statistic. 
And this isn't speculation from a startup pitch deck. Cloudflare processes requests for 20% of all websites on earth. They can see it happening. Global internet traffic grew 19% in 2025, and the curve is not flattening. 
Unlike the COVID traffic spike — which surged and plateaued — this is a slow, relentless, compounding climb.
Right now, automated traffic already accounts for over 51% of all web requests. DataDome's network processed 7.9 billion AI agent requests in just January and February of this year. Meta's AI crawler alone surged from 8.5% to 15.6% of all AI bot traffic in two months. At that rate, it'll hit 20% by April.
And here's the thing nobody talks about: every single one of those requests is reading your website the hard way.

When you open a website, your browser takes all that HTML, CSS, and JavaScript and renders it into something beautiful. Buttons. Colours. Layout. You never see the code. But when an AI agent opens that same page, it doesn't care about the buttons. It doesn't care about the layout. It needs the text. That's it. The actual information.
And yet it has to swallow the entire page — every div wrapper, every script tag, every tracking pixel, every comment left by a developer three years ago who wrote "TODO: fix this later" — just to get to the words.
Now if we use a single blog post from the Gcore site and run it through a token calculator - it consumed 16,180 tokens when served as HTML. The same content, converted to Markdown? 3,150 tokens. That's an 80% reduction. 
Or put another way: four out of every five tokens an AI agent processes on a typical webpage are packaging, not content.

ACT FOUR: TWO FUTURES
[5:30 – 7:30]
So we've got a problem. The web is built for human browsers. But increasingly, the things reading it aren't human. And we're at a crossroads with two very different paths forward.
Future One: The Clumsy Robot
You've probably seen demos of AI agents using a computer. Anthropic's Computer Use. OpenAI's Operator. These are AI systems that literally control a mouse and keyboard, clicking through websites the way you or I would. Opening menus. Scrolling. Waiting for pages to load. Dismissing cookie banners.
It works. Sort of. The way a toddler driving a car works. Technically the vehicle is moving forward.
These browser-use agents are burning enormous amounts of compute to do something incredibly simple: extract text from a webpage or do basic functions. 

Future Two: The Lean Machine
The second path is what I think is going to win. Instead of forcing AI agents to navigate the human web, you build a parallel layer. Same content. Different format. When an AI agent sends a request and says "I'd like Markdown, please" — via a standard HTTP header that already exists, by the way, this isn't new technology — the server responds with clean, structured text. 

This is content negotiation. It's the same mechanism that lets your browser request a JPEG instead of a PNG, or JSON instead of XML. It's how the web has worked for decades. The same URL. The same content. Just a different representation.
And the efficiency gains aren't marginal. We're talking about 80% fewer tokens per page. At the scale of eight billion AI requests a month — and growing — that's not an optimisation. That's a fundamental shift in the economics of how AI interacts with the internet.

ACT FIVE: GOOGLE SAYS IT’S STUPID
Now, remember I said Google called this stupid? Let's talk about that, because it's more interesting than it sounds.
In January 2026 — weeks before Cloudflare launched their version of this — a developer posted on Reddit describing a plan to use middleware to detect AI user agents and serve them raw Markdown files instead of HTML. Google Search Advocate John Mueller responded across multiple platforms, and he was not subtle about it.

On Bluesky (sarcastic face), he wrote: "Converting pages to markdown is such a stupid idea. Did you know LLMs can read images? WHY NOT TURN YOUR WHOLE SITE INTO AN IMAGE?"

His argument boils down to three points. First, LLMs have been trained on HTML since the beginning. They can parse it fine. In fact they might be better at it than markdown.

Second, creating a separate version for bots is cloaking — showing different content to machines than to humans, which Google has banned for over a decade. 

And third, if search engines need to verify that your Markdown matches your HTML, they have to crawl both versions, which doubles the load and negates any efficiency gains.
Bing's Fabrice Canel piled on too, warning that they'd crawl both versions anyway to check similarity.

And here's the thing. Mueller is right but there is a crucial distinction we need to point out. 

The developer on Reddit was describing user-agent sniffing. Detecting when a bot visits and serving it a completely different page. That is cloaking. Mueller is correct to push back on it. If you build separate Markdown shadow pages and only show them to AI crawlers, you've created exactly the kind of divergence that bad actors exploit.

But here's what Mueller never addressed. He never addressed the 80% token reduction. He never addressed the compute waste. The energy cost of processing five times more data than necessary across billions of requests per month. And critically, he conflated two very different technical approaches.

What that Reddit developer described is user-agent sniffing. 
What we’ve built is content negotiation. In content negotiation, the AI agent sends a standard HTTP header saying "I prefer Markdown." The server responds with the same content in a different format. This isn't cloaking any more than a website serving JSON to an API client and HTML to a browser is cloaking. 

It's how the web was designed to work.

ACT SIX: THE INFRASTRUCTURE PLAY
[9:30 – 11:30]

So let's bring this back to what actually matters: what do you do about it?
If you're running a website in 2026 — especially if you're serving technical content, documentation, product pages, or anything that AI agents need to reference — you need to start thinking about your site the way a restaurant thinks about Deliveroo. You still need a beautiful dining room for human customers. But you also need a streamlined, efficient pipeline for the delivery riders who just need the food.

At Gcore, we built FastEdge to handle exactly this kind of problem at the edge. FastEdge runs WebAssembly on over 210 edge nodes worldwide, which means you can deploy lightweight conversion logic — HTML to Markdown, content negotiation, token-aware responses — directly on the infrastructure closest to where the request originates. Average global latency of 30 milliseconds.
The practical difference matters. With FastEdge, you write a small Wasm application that intercepts incoming requests, checks the Accept header, and — if the client is asking for Markdown — strips the HTML response down to clean, structured text before it reaches the agent. No separate pages. No shadow sites and no cloaking. 

Let’s set it up. 


ACT SEVEN: THE CLOSE
[11:30 – 13:00]
Here's what I want you to take away from this.
The web was built for humans. And it will continue to serve humans beautifully. Nobody is suggesting you tear down your website and replace it with a Markdown file. The dining room stays open.
But the delivery window is about to become the busiest part of the restaurant. And right now, most websites are forcing every delivery rider to sit down, order from the full menu, wait for the appetiser, compliment the wine selection, and then finally take the food.
The question isn't whether this happens. It's whether your infrastructure is ready when it does.
If you want to set this up for your own site, we've published a step-by-step guide using Gcore FastEdge — link in the description. And if you found this useful, you know the drill.


