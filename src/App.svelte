<script lang="ts">
    import "./app.css";
    import Intro from "$lib/Intro.svelte";
    import Navbar from "$lib/Navbar.svelte";
    import WorkExperience from "$lib/WorkExperience.svelte";
    import Projects from "$lib/Projects.svelte";
    import { Copyright } from "@lucide/svelte";

    const experiences = [
        {
            title: "Werkstudent C-Entwickler",
            organization: "ipoque GmbH",
            period: "Juli 2026 - Jetzt",
            bullets: [
                "Performance- und Genauigkeitsoptimierung sowie Weiterentwicklung eines internen Analyse-Tools",
                "Modernisierung von Integrationstests auf aktuelles Format",
                "Implementierung eines CI-Jobs zur automatisierten Validierung von Dateinamenskonventionen",
            ],
        },
        {
            title: "Praktikum C-Entwickler",
            organization: "ipoque GmbH",
            period: "April 2026 - Juni 2026",
            bullets: [
                "Klassifikation von Netzwerkapplikationen durch Analyse von Netzwerkverkehr mit Wireshark und internen Tools",
                "Eigenständige Implementierung von drei Netzwerkprotokollen (Zabbix, NDMP, IEEE 802.15.4)",
                "Entwicklung Lumos - KI-gestütztes Tool zur automatisierten Erstellung von Klassifikationen",
                "Bearbeitung von Wartungsaufgaben und Modernisierung von Integrationstests auf aktuelles Format",
                "Automatisierung wiederkehrender Prozesse mittels selbstgeschriebener Python- und Shell-Skripte",
                "Arbeit im Kanban-Team; Nutzung von Jira, Confluence, GitLab, Wireshark, CMake/Make",
            ],
        },
        {
            title: "LLM-unterstütztes Autotesting für moderne Web-Frontends - Softwareprojekt",
            organization: "Check24",
            period: "April 2025 - Februar 2026",
            bullets: [
                "Entwicklung eines Chatbots zur automatisierten Generierung von Auto-Playwright-Tests",
                "Aufbau eines Go-Backends (Gin, Wire) mit klarer DDD-inspirierter Architektur",
                "Containerisierung der Testausführung mittels Docker",
                "Sicherstellung von Code-Qualität durch table-driven Unit-Tests, Linting und static analysis",
                "Entwicklung eines Svelte-Frontends (TypeScript, Prettier, ESLint)",
                "Schreiben von Unit- und Component-Tests mit Vitest",
                "Erstellung einer vollständigen RESTful API-Spezifikation nach OpenAPI",
                "Arbeiten nach agilen Methoden (Scrum)",
            ],
        },
        {
            title: "Entwicklung einer PHP-API zur Messwertverarbeitung",
            organization: "Auftragsarbeit – Psychologe",
            period: "Januar 2025 — März 2025",
            bullets: [
                "Konzeption und Implementierung einer Single-Page-Application (PHP, TypeScript)",
                "Sessionbasierte Datenspeicherung und serverseitige Berechnung von Messwerten",
            ],
        },
        {
            title: "Stadt in der Stadt - Ehrenamtlich",
            organization: "Haus Steinstraße e.V.",
            period: "Sommer 2017/2018",
            bullets: [
                "Betreuung von 5–15 Kindern (6–10 Jahre) beim Bau kleiner Holzhäuser",
            ],
        },
    ];

    const projects = [
        {
            title: "Grafikrenderer",
            link: "https://github.com/Skzter/CG-Renderer",
            period: "April 2025 - Juli 2025",
            bullets: [
                "Entwicklung eines fotorealistischen Raytracing-Renderers (C++)",
                "Implementierung von Beschleunigungsstrukturen und Lichtmodellen",
                "Projektarbeit im Rahmen des Moduls Computergrafik (2er-Team)",
            ],
        },
        {
            title: "Kniffel",
            link: "https://github.com/Brubi25/Abschlussprojekt-Kniffel",
            period: "August 2024 - September 2024",
            bullets: [
                "Abschlussprojekt im Modul Anwendungsorientierte Programmierung (3er-Team)",
                "Java-11-Anwendung mit Java Swing",
                "Aufbau solider Grundlagen in objektorientierter Programmierung",
            ],
        },
        {
            title: "Modifiziertes Damespiel",
            link: "https://github.com/Skzter/dame",
            period: "Januar 2024 - Februar 2024",
            bullets: [
                "Terminalbasierte C++11-Anwendung",
                "Grundlegende Datenstrukturen und Spiel-Logik implementiert",
            ],
        },
    ];
</script>

<nav class="sticky top-0 z-999 bg-neutral-300">
    <Navbar></Navbar>
</nav>

<main class="flex flex-col p-2">
    <section id="about" class="scroll-mt-5">
        <Intro></Intro>
    </section>

    <section id="work" class="scroll-mt-5">
        <h1>Berufserfahrung</h1>
        {#each experiences as exp}
            <WorkExperience {...exp} />
        {/each}
    </section>

    <section id="projects" class="scroll-mt-5">
        <h1>Projekte</h1>
        {#each projects as project}
            <Projects {...project} />
        {/each}
    </section>
</main>

<footer>
    <div class="flex justify-center gap-5 m-2">
        <div class="flex">
            <Copyright />
            <p>Vincent Götze 2026</p>
        </div>
        <div class="border border-black"></div>
        <p>build with svelte and tailwind</p>
    </div>
</footer>
