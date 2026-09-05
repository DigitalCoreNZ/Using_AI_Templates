# Videos Template

You will use the `https://www.studiobinder.com/blog/script-writing-on-youtube/` article as your source when you create the 
`/media/brian/Apps/01_lena_v0.5.0/Templates/Template_Videos_v0.5.1.ad` template. A template is the structured, style guide that accompanies an AI prompt, and provides the (pending) placeholders that are processed by an AI agent.

You will ensure the template is:

* Specifically geared toward producing YouTube video scripts,
* Able to produce scripts with an average video runtime of ten minutes (although longer runtimes are expected for more complex topics),
* Structured with a cold open for the hook, a title sequence, the scenes, and a review.

1. Word-count governance: The word-count is not important. The purpose of a template is to guide the creation process rather than set limitations.

2. Number of scenes: Again, the template provides structure, not boundaries.

3. Scene anatomy: This is the reason for creating a template: AV Columns. Each scene requires a Scene Title that will be displayed on-screen, a Scene Number that is used during production, and (pending) placeholders for both values. The Shot column, with a (pending) placeholder, contains the Scene-Shot numbers, e.g. 1.1. The Visuals column, with a (pending) placeholder, describes what is seen, e.g. host, table, chart, etc. The Dialogue column, with a (pending) placeholder, describes what is said by the host, or a v/o (voice over). The Duration column, with a (pending) placeholder, is where an estimate of the screen time is placed.

4. Default framework: The type of YouTube products that will be produced are explainer videos. The Storytelling framework is best suited to these types of videos.

5. Voice-over style: Explainer videos can be dry, technical, and boring. The overall tone, including the voice-over style, must be energetic, punchy, and enthusiastic, with minimal filler. This information is important but is not included in the body of the template. Instead, you will place this material, along with other aesthetic details, in the front matter header of the template.

6. Scope of the Cold Open and Review: The Cold Open, where the hook is delivered in 15 seconds, is a teaser of the up-coming content. The purpose of the teaser is to engage the viewer, nail their attention, and deliver the Signature Sign On: "My name is Brian, I'm an AI Generalist, and this is DigitalCoreNZ", and all of this needs to happen before the title sequence rolls. The Review is a quick recap of the video, the CTA ("Click the Like button and Subscribe for more of my content if this is the kind of video you enjoy."), and the Signature Sign Off ("Until next time: Be safe, be kind, be awesome, kia kaha!!").

7. Production metadata attributes: The front matter header of this template needs specialist metadata. For instance, the `Scope of the Cold Open and Review` needs to be accessible to an AI agent so that it understands the scope of what is required. When you create the `Template_Videos_v0.5.1.ad` template, there will be (pending) placeholders, immutables (Signature Sign On, CTA, and Signature Sign Off), and custom metadata that provides insights into how the AI agent can effectively produce a result that aligns with the given prompt: "Produce a script about widgets. Your source material is BLAH, BLAH. Use the Template_Videos_v0.5.1.ad template as your style guide. Etc."

---

You will use the `/media/brian/Apps/01_lena_v0.5.0/Templates/Template_Videos_v0.5.1.ad` template as your style guide when you create the `/media/brian/Apps/01_lena_v0.5.0/YouTube/001_Recovery_v0.5.1.ad` filming script. You source is the CloneZilla Live documentation (`https://clonezilla.org/clonezilla-live-doc.php` is the index page). You will (1 of 2) create a script on how to create an image, and then (2 of 2) use an image to restore a system. Be sure to include disclaimers due to the destructive nature of restoring a system (when restoring a system, everything on the target partition or drive will be overwritten!!) Ensure first person pronouns are used, i.e. I, me, my, mine, myself, and that everything is written in the present tense.

---

Let's work on the `/media/brian/Apps/01_lena_v0.5.0/YouTube/001_Recovery_v0.5.2.ad` rewrite. I separate my system from my data. I use my system to create my data (source code, technical documents, business documents, etc.) but my data is saved to a 4-drive NAS. Each drive has a 6TB capacity, but RAID-5 is enabled for redundancy, so the total storage is 18TB. Also, there is a 5TB external HDD connected to the NAS, allowing it to perform backups on a schedule. The reason for separating my system from my data is that, as an AI Generalist, I am constantly installing new models, agents, and tools. It is common for a new installation to brick my system. Therefore, I use a **destructive** process to restore my system to a known, tested, stable condition. It is important to include a disclaimer, immediately after the opening title sequence, that **strongly** emphasises the destructive nature of my system recovery process. The viewer MUST UNDERSTAND that restoring my system OVERWRITES EVERYTHING on my drive or partition. I am able to restore my system because my data is saved to a different location, specifically my NAS. To simplify the story, and align it with my actual setup, my system has its own 5TB HDD that is connected to my PC which is used to save images.