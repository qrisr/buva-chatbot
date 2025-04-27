# Toolbox Agenda 2030 Chatbot MVP - Visualisierungspaket

## Übersicht

Dieses Dokument enthält eine umfassende visuelle Darstellung des MVP (Minimum Viable Product) für den KI-gestützten Chatbot zur Navigation der Toolbox Agenda 2030. Die Visualisierungen umfassen die Systemarchitektur, den Datenfluss, die Benutzeroberfläche und die Komponenteninteraktionen.

## 1. Architekturdiagramm

Das Architekturdiagramm zeigt die Hauptkomponenten des Chatbot-Systems und deren Beziehungen zueinander.

![Architekturdiagramm](/home/ubuntu/architecture_diagram.png)

**Hauptkomponenten:**
- **Benutzeroberfläche**: Chat-Widget, Sprachauswahl, Schnellzugriff-Buttons und Hilfebereich
- **n8n-Workflows**: Webhook-Empfänger, Initialisierungs-Workflow, Intentionserkennung, RAG-Komponente und Mehrsprachigkeitsmanagement
- **Externe Dienste**: OpenAI API (GPT-4o), Vektor-Datenbank für Embeddings und die Toolbox Agenda 2030 Websites

## 2. Datenflussdiagramm

Das Datenflussdiagramm visualisiert, wie Daten durch das System fließen, von der Benutzeranfrage bis zur Antwortgenerierung.

![Datenflussdiagramm](/home/ubuntu/data_flow_diagram.png)

**Hauptdatenflüsse:**
1. **Benutzeranfrage**: Der Benutzer stellt eine Frage über das Chat-Widget
2. **Spracherkennung und Intentionserkennung**: Die Anfrage wird analysiert, um die Sprache und die Intention zu erkennen
3. **RAG-Prozess**: Bei Suchanfragen werden relevante Dokumente aus der Vektordatenbank abgerufen
4. **Antwortgenerierung**: OpenAI generiert eine kontextbezogene Antwort basierend auf den relevanten Dokumenten
5. **Hintergrundprozesse**: Extraktion von Inhalten aus den Toolbox-Websites und Generierung von Embeddings

## 3. Benutzeroberflächen-Mockup

Das UI-Mockup zeigt das Design und die Funktionalität des Chatbots aus Benutzerperspektive.

### Desktop-Ansicht
![Desktop-Ansicht](/home/ubuntu/screenshots/ui_mockup_html_2025-04-26_11-54-43_8069.webp)

**Hauptelemente:**
- Chat-Widget mit Nachrichtenverlauf und Eingabefeld
- Sprachauswahl für alle Schweizer Landessprachen (DE, FR, IT) und Englisch
- Schnellzugriff-Buttons für häufige Fragen
- Hilfebereich mit Nutzungshinweisen

### Mobile-Ansicht
Die mobile Ansicht ist für Smartphones und Tablets optimiert und bietet die gleiche Funktionalität in einem angepassten Layout.

## 4. Komponenteninteraktionsdiagramm

Das Komponenteninteraktionsdiagramm zeigt, wie die verschiedenen Komponenten des Systems miteinander interagieren.

![Komponenteninteraktionsdiagramm](/home/ubuntu/component_interaction_diagram.png)

**Hauptinteraktionen:**
1. **Benutzerinteraktionen**: Anfragen stellen, Sprache wählen, Schnellzugriff nutzen, Hilfe öffnen
2. **Frontend-Backend-Interaktionen**: Übermittlung von Anfragen und Metadaten an n8n
3. **n8n-interne Interaktionen**: Weiterleitung zwischen Workflows basierend auf erkannter Intention
4. **Datenverarbeitungsinteraktionen**: Extraktion von Inhalten, Generierung von Embeddings, Ähnlichkeitssuche
5. **Antwortgenerierung**: Erstellung kontextbezogener Antworten mit OpenAI und Rückgabe an den Benutzer

## 5. Technische Details

### Verwendete Technologien
- **Frontend**: HTML, CSS, JavaScript, WordPress-Integration
- **Backend**: n8n-Workflow-Automatisierung
- **KI-Komponenten**: OpenAI GPT-4o für Textgenerierung und Embeddings
- **Datenbanken**: Vektordatenbank für Embeddings und Ähnlichkeitssuche

### Mehrsprachigkeit
Der Chatbot unterstützt alle Schweizer Landessprachen:
- Deutsch
- Französisch
- Italienisch
- Englisch (zusätzlich)

### Barrierefreiheit
Die Benutzeroberfläche wurde unter Berücksichtigung von Barrierefreiheitsstandards entwickelt:
- Tastaturnavigation
- Screenreader-Kompatibilität
- Ausreichender Farbkontrast
- Responsive Design für alle Geräte

## 6. Implementierungshinweise

Für die Implementierung des MVP in Ihrer Umgebung sind folgende Schritte erforderlich:

1. **n8n-Workflows importieren**: Laden Sie die bereitgestellten Workflow-Definitionen in Ihre n8n-Instanz
2. **WordPress-Plugin installieren**: Integrieren Sie das Chat-Widget in Ihre Toolbox-Websites
3. **OpenAI API konfigurieren**: Stellen Sie sicher, dass die API-Schlüssel korrekt eingerichtet sind
4. **Datenextraktion durchführen**: Führen Sie den Datenextraktions-Workflow aus, um Inhalte zu indexieren
5. **Testen und Anpassen**: Überprüfen Sie die Funktionalität und nehmen Sie bei Bedarf Anpassungen vor

## 7. Nächste Schritte

Nach der erfolgreichen Implementierung des MVP können folgende Erweiterungen in Betracht gezogen werden:

1. **Verbesserung der thematischen Filterung**: Präzisere Kategorisierung und Matching-Algorithmen
2. **Implementierung von Rückfragen**: Bei unklaren Anfragen kann der Chatbot gezielt nachfragen
3. **Optimierung der Antwortzeit**: Caching-Mechanismen für häufig gestellte Fragen
4. **Erweiterung der Wissensbasis**: Integration weiterer Quellen und Dokumente
5. **Nutzerfeedback-Mechanismus**: Sammlung und Auswertung von Feedback zur kontinuierlichen Verbesserung
