---
name: human
description: Rewrite text in English or Spanish so it reads like a person wrote it, stripping the tells catalogued in Wikipedia's "Signs of AI writing." Use this whenever the user invokes /human, or asks to "humanize," "de-slop," "de-AI," "make this sound human," "take the AI out of this," "que no suene a IA," "humaniza esto," or "apply the human rules" to a piece of text. Also use it to clean up text Claude just produced when the user reacts with "this sounds like AI" or "rewrite this properly." Trigger even when the user only pastes a passage and types /human with no other instruction.
---

# Human

Rewrite a piece of text so it reads like a knowledgeable person wrote it, not a language model. This removes the patterns that mark text as AI-generated (per Wikipedia:Signs of AI writing) while keeping the writer's own voice, facts, and meaning intact.

## What to operate on

- If the user pasted or attached text, that is the target.
- If the user typed `/human` with no text, rewrite the most recent substantial thing Claude wrote in this conversation.
- If neither exists, ask what text they want rewritten. Do not invent a passage.

Rewrite it in place and return the cleaned version. Preserve the original meaning, facts, names, numbers, and structure. This is a style pass, not a content rewrite: do not add claims, drop information, or change what the text says.

## The one rule that drives all the others

AI writing regresses to the mean: it smooths specific, unusual facts into generic, important-sounding statements. A sharp photograph fades into a blurry sketch while the caption shouts that the subject matters. So the core move is **keep the specific detail and cut the significance chaser.** If a sentence names a real tool, date, place, person, or number, protect it. If a sentence exists only to tell the reader that something is important, cut it.

## Remove these tells

**Manufactured significance and legacy.** Delete sentences and clauses that inflate importance: "marks a pivotal moment," "stands as a testament to," "reflects a broader shift," "cements its place," "leaves an indelible mark," "plays a vital role in the evolving landscape of." A fact does not need a significance chaser.

**The "-ing" analysis tail.** Cut participle phrases tacked onto the end of a sentence that editorialize instead of inform: "...highlighting its importance," "...underscoring the community's resilience," "...reflecting a commitment to excellence." These read as analysis but say nothing.

**Copula avoidance.** Restore plain verbs. Use "is / are / has," not "serves as / stands as / functions as / boasts / features / offers" when a simple statement is meant. Reserve "features" or "offers" for when they are literally accurate.

**Notability and coverage over-attribution.** Do not stack proof-of-importance: "featured in national media outlets," "profiled in leading publications," "maintains an active social media presence," "recognized by industry experts." State what is true plainly.

**Vague attributions (weasel words).** Cut "some critics argue," "observers have noted," "experts say," "it is widely regarded as," when no specific source is named. Either name the source or drop the framing.

**Negative parallelisms.** Remove "It's not X, it's Y," "not only X but also Y," "no X, no Y, just Z," and "X rather than Y" when used for rhetorical punch. Say the thing directly.

**Rule of three.** Break the reflexive triplet habit. Not every list needs exactly three items and not every noun needs three adjectives. Keep the items that carry real information, cut the padding.

**Forced synonym variation (elegant variation).** Let a word repeat when repeating it is clearer. Do not reach for an awkward substitute just to avoid saying the same word twice.

**Reflexive summaries.** Delete "In summary," "In conclusion," "Overall," and closing paragraphs that restate what was just said, unless the piece is genuinely long enough to need one.

**Didactic disclaimers.** Cut "it's important to note," "it's worth noting," "it's crucial to remember," and hedging preambles that acknowledge a subject is minor before explaining its importance anyway.

**Knowledge-cutoff and gap speculation.** Remove "as of my last update," "while specific details are limited," "based on available information," "maintains a low profile / keeps details private." If the information isn't known, say so plainly or leave it out.

**Chatbot residue.** Strip anything meant for a chat interface: "Certainly!," "I hope this helps," "Would you like me to...," "Here's a detailed breakdown," placeholder brackets like [Insert date], and closing offers to adjust.

**AI-vocabulary words.** Cut or replace when they appear as filler: delve, intricate, tapestry, pivotal, underscore, landscape (as metaphor), foster, testament, crucial, enhance, robust, seamless, realm, navigate (as metaphor), garner, showcase, boast, meticulous, vibrant, bolster, interplay, align with. One of these can be fine in context; a cluster is the tell.

## Formatting tells

- Do not bold every key term like a textbook. Bold sparingly, if at all.
- Avoid the "**Term:** definition" bulleted-list layout unless a real list is warranted.
- Use prose where a paragraph reads better than bullets.
- Sentence case for headings, not Title Case On Every Word.
- No emojis as decoration in headers or bullets.
- Straight quotes and apostrophes, used consistently.

## Punctuation: no em dashes (English only)

Never use em dashes (—) in English output. This is a hard rule. In Spanish, see the raya rule in the Spanish section: the dash is legitimate there and banning it outright makes the text read as translated. Replace them with a comma, a colon, parentheses, or a separate sentence, whichever fits. Use en dashes (–) only for real ranges (1990–2000, 3–2). Do not overcorrect into hyphens where other punctuation belongs.

## What human writing actually does (do these, don't just avoid the above)

The goal is not sterile, tell-free prose. It is writing that sounds like a person who knows the subject. So:

- Use simple "is / has" constructions.
- Use plain verbs: wrote (not authored), used (not utilized), moved (not relocated), tried (not attempted), died (not passed away), started (not embarked on).
- Make definite claims when they are true: "the first," "the only," "one of the best," instead of hedged mush.
- Keep ordinary human qualifiers where they fit: "perhaps," "roughly," "tends to," "for the most part."
- Keep everyday constructions AI tends to prune: "as a result of," "the fact that," "a part of." They are not errors.
- Favor one concrete, specific detail over three generic important-sounding phrases.
- Name emotions plainly. "She was afraid" and "I was frustrated" are human; a tightening chest, cold sweat, and a breath she didn't know she was holding are the machine's version of feeling. Research on AI fiction (StoryScope, COLM 2026) found AI renders emotion through the body 81% of the time while humans do it 38%; humans just name the feeling far more often. Don't convert every emotion into anatomy.
- Name real things. Specific books, songs, brands, streets, and people, cited by name, are among the strongest human signals. AI defaults to vague allusion ("a classic novel," "a well-known study"); a person says which one.
- Let the writing acknowledge the reader when it's natural: a direct aside, a "you know the type," a rhetorical question actually aimed at someone. AI writes as though no one is watching.

## Structural tells (beyond the sentence level)

Style edits alone don't fool anyone paying attention: research on AI-generated fiction (StoryScope, COLM 2026) showed that after professionally editing AI text for style, structural analysis still detected it at 93.9%. The shape of the writing is a tell, not just the words. These apply to all writing, adapted by type.

**Any writing (emails, posts, essays, marketing, reports):**

- **Don't state the takeaway the reader can infer.** AI over-explains its point: it makes the argument, then adds a sentence telling you what the argument meant. Cut the "what this means is," "the lesson here is," "at the end of the day" paragraph. Trust the reader.
- **Don't over-embody.** Cut the reflexive somatic dressing: "my stomach dropped," "I felt a knot in my chest," "a wave of relief washed over me" as default emotional language. Say what you felt.
- **Break the single track.** AI writing moves in one straight line: point, support, conclusion, every paragraph a tidy link in one chain. Human writing digresses, doubles back, drops in an aside, mentions something and returns to it later. One tangent that earns its place makes a piece read more human than ten clean transitions.
- **Tolerate loose ends.** Not every piece needs full resolution. Humans end on an open question, a partial answer, or an admission of what they still don't know. AI resolves everything into acceptance and closure.
- **Engage the outside world.** Cite the actual article, name the competitor, mention the specific customer call. AI keeps everything generic and self-contained.

**Narrative or story-driven text (case studies, founder stories, sermons, fiction, personal posts):**

- Watch for the tidy arc: linear chronology, no subplots, protagonist solves everything through their own choices, ending states the moral. Humans jump in time, start at the end, leave threads hanging, and let the point stay implicit.
- Watch for morally clean protagonists. Human stories let their subject be partly wrong, conflicted, or unresolved.
- Watch for setting-mirrors-mood (rain when sad, dawn when hopeful) and smell imagery as reflexes; AI over-uses both.
- Claude specifically favors quiet, reverent endings and tacked-on epilogue paragraphs. If the last paragraph is a gentle coda restating the emotional resolution, cut it and end on the last real event.

Since this skill is a style pass, don't restructure the text without being asked. When structural tells are present, fix what a line edit can fix (stated takeaways, somatic filler, generic references) and add one short note at the end flagging the structural issues: "Reads AI at the structural level: fully linear, everything resolved, moral stated. Consider reordering / cutting the epilogue / leaving X open." Offer to do the structural rewrite as a second pass.

## Do not overcorrect

Wikipedia's own page warns that many of these signs are also ordinary human habits, and that hunting them too aggressively produces its own bad writing. So do not mangle grammar, strip all structure, or ban every flagged word to prove a point. A single well-placed instance of a "watch" word is fine. Preserve the writer's voice; this pass removes slop, it does not flatten personality.

## Spanish

If the source text is in Spanish, rewrite it in Spanish. Never translate to English unless asked. Everything above still applies, with the adjustments below.

### Variant and address

Write neutral Latin American Spanish, Caribbean-leaning, the way an educated Puerto Rican writes.

- Use tú for singular, ustedes for plural. Always.
- Never use vos or voseo conjugations: no tenés, querés, sos, podés, vení, mirá.
- Never use vosotros or peninsular forms: no tenéis, habéis, sabéis, os, vuestro.
- Avoid regionalisms that don't travel: no órale, chido, güey, che, pibe, coger in the peninsular sense, ordenador, móvil, vale, guay, zumo.
- Use computadora, celular, jugo, carro, apartamento, estacionamiento.
- Caribbean and Puerto Rican usage is fine when it's natural to the writer. Don't sand the voice down into a corporate press release.

### Spanish AI vocabulary

Cut or replace these when they show up as filler. A cluster of them is the tell.

adentrarse, sumergirse, panorama, entramado, tejido (as metaphor), crisol, crucial, fundamental, clave, esencial, robusto, sólido, integral, potenciar, impulsar, fomentar, propiciar, aprovechar al máximo, optimizar, transformador, innovador, vanguardia, sinergia, holístico.

Same for the stock phrases: "en constante evolución," "un antes y un después," "sin fisuras," "de la mano de," "no es casualidad que," "en un mundo cada vez más," "cabe resaltar," "en definitiva."

### Copula avoidance in Spanish

Restore es, está, tiene, hace. Cut these when a plain statement is meant: se erige como, se posiciona como, se consolida como, se perfila como, constituye, representa, funge como, ostenta, alberga, cuenta con (when it just means tiene).

### Gerundio de posterioridad

In English the trailing "-ing" clause is a style tic. In Spanish it's a grammatical error, so the rule is stricter. Never write a gerund describing something that happens after the main verb: "Lanzó el producto en julio, generando ventas récord." Rewrite as two clauses or with que: "Lanzó el producto en julio y las ventas rompieron récord."

The editorializing tails are the same idea and also go: "...destacando su importancia," "...reflejando el compromiso del equipo," "...marcando un hito."

### Translation calques

These mark text as English run through a model. Fix them.

- "en orden de" → para
- "hacer sentido" → tener sentido
- "remover" (to take away) → quitar, eliminar
- "eventualmente" (meaning finally) → finalmente, con el tiempo
- "aplicar para" un trabajo → solicitar
- "asumir" (to suppose) → suponer, dar por sentado
- "eventos" for every occasion → actos, actividades, funciones
- "realizar" as the default verb → hacer, llevar a cabo, cumplir
- "soportar" (to support) → apoyar, admitir, ser compatible con
- "acceder a" as a catch-all → entrar a, consultar, obtener
- "basado en" at the start of a sentence → según, a partir de
- "adicionalmente" → además

Also watch the syntax calques: English word order forced onto Spanish, possessives where Spanish uses the article ("me duele la cabeza," not "mi cabeza duele"), and passive voice where Spanish would use se ("se publicó el informe," not "el informe fue publicado").

### Rhythm

Spanish sentences run longer than English ones and use subordination. Chopping everything into short declarative sentences is itself a tell of machine translation. Let clauses connect with que, donde, aunque, mientras, ya que. Don't manufacture staccato punch that the language doesn't have.

### Spanish punctuation and typography

- Open every question and exclamation: ¿ and ¡. Non-negotiable.
- The raya (—) is correct Spanish for dialogue and for parenthetical incisos. Keep it where it belongs. What to cut is the decorative dash used for dramatic pause, which is the English AI habit wearing a Spanish coat.
- Comillas: « » or " " used consistently. Don't mix.
- Lowercase for months, days, nationalities, languages, and religions: enero, lunes, puertorriqueño, español.
- Sentence case for headings. Spanish capitalizes titles even less than English does.
- Accents on capital letters: Álvarez, Ángel, ÉXITO.
- Decimals and thousands follow the local convention the writer already uses. Don't switch it mid-document.
- Percentages: 30 %, or 30% if that's the writer's habit. Be consistent.

### Mixed-language text

If the writer code-switches, leave it. Spanglish in a Puerto Rican context is voice, not error. Clean the slop around it, keep the switch.

### Structural tells in Spanish

The structural rules above apply in Spanish with the same force; only the surface phrases change.

- Cut the stated takeaway: "la lección aquí es," "lo que esto significa es," "al final del día," "esto nos demuestra que."
- Cut the somatic filler: "se me hizo un nudo en la garganta," "sentí un vuelco en el estómago," "una ola de alivio me recorrió." Name the feeling: tenía miedo, estaba frustrada, me alegré.
- Name real things: the actual libro, canción, calle, or marca, not "una obra clásica" or "un estudio reconocido."
- Same flag-don't-restructure rule: fix what a line edit fixes, note the structural issues briefly at the end, offer the rewrite as a second pass.

## Output

Return the rewritten text and nothing else, unless the user asks to see what changed. If the user asks for a diff or explanation, list the specific tells you removed after the rewrite, briefly. Keep the rewrite roughly the same length as the original; humanizing usually means cutting, not padding.

## Example

**Input:**
The Q3 launch marks a pivotal milestone in our company's journey, serving as a testament to our team's unwavering commitment to innovation. Featured in several prominent industry outlets, the product has garnered significant attention—underscoring its transformative potential in an ever-evolving marketplace.

**Output:**
We launched the product in Q3. Three trade publications covered it, and early signups ran ahead of our forecast. It does one thing our competitors' tools don't: it syncs leads back to the CRM in real time.

The rewrite drops the significance language ("pivotal milestone," "testament," "unwavering commitment"), the copula avoidance ("serving as"), the coverage puffery ("prominent industry outlets," "garnered significant attention"), the "-ing" tail ("underscoring its transformative potential"), the AI-vocab ("transformative," "ever-evolving"), and the em dash. It replaces the vague claim with a concrete, checkable one.

## Ejemplo en español

**Entrada:**
El lanzamiento del tercer trimestre se erige como un hito fundamental en la trayectoria de nuestra empresa, constituyendo un testimonio del compromiso inquebrantable de nuestro equipo con la innovación. Basado en la cobertura de destacados medios del sector, el producto ha captado una atención significativa, reflejando su potencial transformador en un mercado en constante evolución.

**Salida:**
Lanzamos el producto en el tercer trimestre. Lo cubrieron tres revistas del sector y los registros iniciales superaron lo que habíamos proyectado. Hace algo que las herramientas de la competencia no hacen: sincroniza los leads con el CRM en tiempo real.

Se van la inflación de importancia ("hito fundamental," "testimonio," "compromiso inquebrantable"), la evasión de la cópula ("se erige como," "constituyendo"), el calco ("basado en" al inicio), el gerundio de posterioridad ("reflejando"), y el vocabulario de IA ("transformador," "en constante evolución"). En su lugar queda un dato concreto que se puede verificar.
