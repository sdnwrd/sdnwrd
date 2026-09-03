# Julian Seidensal

18, aus Fulda. Ich baue eigene Produkte, keine Übungsaufgaben: einen Proxy, mit dem Claude Code
über ein deutlich günstigeres Modell läuft, eine Instagram Analytics-App mit verschlüsselten Sessions, eine
Website, die ich verkauft habe.

Aktuell suche ich einen **dualen Studienplatz Software Engineering in Würzburg**.

📮 seidensal.julian@gmail.com

---

## Projekte

**[Instalytics](https://github.com/sdnwrd/instalytics)** · Next.js · FastAPI · PostgreSQL
Multi-User-Web-App, die Instagram-Follower über die Zeit verfolgt und zeigt, wer wann entfolgt ist.
Backend-for-Frontend, damit die Instagram-Session nie im Browser landet, Sessions mit AES-256-GCM
verschlüsselt abgelegt, Nutzertrennung in der Datenbankabfrage statt nur in der Oberfläche.

> Bewusst nie öffentlich gestartet: das Auslesen von Follower-Listen widerspricht den
> Nutzungsbedingungen von Instagram. Das Projekt lief privat auf meinem eigenen Konto.
> Technisch war es meine größte Lernstrecke, deshalb steht es hier, mit dieser Einschränkung dazu.

**[Kairotokens](https://kairotokens.cc)** · Cloudflare Workers · Durable Objects · KV
Claude Code weiterbenutzen, nur günstiger. Der Worker verhält sich für den Client exakt wie die
Anthropic-API, leitet die Anfragen aber an DeepSeek weiter: gleicher Editor, gleicher Workflow,
ein Bruchteil der Kosten. Zwei Umgebungsvariablen ändern, sonst bleibt alles wie es war.

Damit das trägt: das Modell wird immer überschrieben statt durchgereicht, Streaming läuft per
`TransformStream` unverändert durch, Felder die der Upstream nicht kennt werden entfernt statt mit
einem Fehler quittiert, und Fehler kommen in der Anthropic-Form mit Originalstatus zurück.
Verkauft wird über eigene Schlüssel mit Prepaid-Guthaben: Schlüsselprüfung über KV, Guthaben über
Durable Objects, weil zwei gleichzeitige Anfragen sonst denselben veralteten Stand lesen und beide
abbuchen könnten. Verrechnet wird erst nach der Antwort über `waitUntil()`, damit die Buchhaltung
keine Latenz kostet.

Live unter [kairotokens.cc](https://kairotokens.cc) · Quellcode nicht öffentlich.

**[PolyWeather](https://github.com/sdnwrd/polyweather)** · Python
Vergleicht Temperaturmärkte auf Polymarket mit der Prognose des US-Wetterdiensts und meldet per
Telegram, wenn ein Kurs deutlich abweicht. Die Punktprognose wird zu einer Verteilung, damit sich
einzelne Temperaturbereiche überhaupt bewerten lassen. Handelt bewusst nicht selbst.

**[rashidabdu](https://rashidabdu.com)** · Next.js
Website für einen jungen Unternehmer, als Auftrag gebaut und verkauft. Erster Kunde, erste echte
Deadline, erste Rechtstexte. Live unter [rashidabdu.com](https://rashidabdu.com).

**[SevenWebSolutions](https://github.com/sdnwrd/Seven)** und **[ChiChi](https://github.com/sdnwrd/chichi-website)** · React · Vite · Next.js
Lernprojekte, ehrlich als solche. Entstanden, um Routing, Animationen und Komponentenaufbau zu
üben. Kein Kunde, kein Produkt, aber die Grundlage für alles danach.

---

## Stack

Die Aufteilung ist Absicht. Ich schreibe lieber hin, wo ich stehe, als im Gespräch aufzufliegen.

**Kann ich erklären**
`Python` `HTML/CSS` `Git` `Vercel` `Railway`

**Im Projekt eingesetzt** - läuft, aber ich müsste vieles nachschlagen
`TypeScript` `Next.js` `React` `Tailwind CSS` `SQL` `PostgreSQL` `FastAPI` `NextAuth`
`Cloudflare Workers` `Durable Objects` `KV`

**Davor gelernt** - vor der KI-Zeit, mit C# und C++
Ein Programm, das den Bildschirm in Echtzeit ausliest und auf Farbmuster reagiert, und eines, das
sich in einen laufenden Spielprozess einklinkt. Spielereien, aber dort habe ich zum ersten Mal
gesehen, wie ein Programm mit Prozessen und Speicher umgeht.

---

## Wie ich arbeite

Mich interessiert weniger die Oberfläche als das, was passieren muss, damit sie funktioniert:
Konsistenz beim Abrechnen, wo Geheimnisse liegen dürfen, was das System macht, wenn eine fremde
API nicht antwortet. 

Dazu gehört, mich laufend mit KI zu beschäftigen. Sie verändert diese Branche gerade grundlegend,
und wer sich nicht damit auseinandersetzt, arbeitet in wenigen Jahren an einem überholten Stand.
Ich nutze sie als Werkzeug, prüfe aber, was sie ausgibt.
