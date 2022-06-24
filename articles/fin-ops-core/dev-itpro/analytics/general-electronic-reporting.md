---
title: Überblick über die elektronische Berichterstellung (ER)
description: Dieser Artikel bietet eine Übersicht zum Tool zur elektronischen Berichterstellung. Es beschreibt Schlüsselkonzepte, unterstützte Szenarien und Formate, die Teil der Lösung sind.
author: NickSelin
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65f7a642d3b2c2ddfca1e2d92570b49ef2f8c2b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869256"
---
# <a name="electronic-reporting-er-overview"></a>Überblick über die elektronische Berichterstellung (ER)

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält eine Übersicht über das Tool zur elektronischen Berichterstellung (EB). Es umfasst Informationen über wesentliche Konzepte, vom ER unterstützte Szenarien und eine Liste der Formate, die im Rahmen der Lösung entwickelt und veröffentlicht wurden.

EB ist ein konfigurierbares Tool, das Ihnen hilft, gesetzliche elektronische Berichterstellungen und Zahlungen zu erstellen und zu verwalten. Es basiert auf den folgenden drei Konzepten:

- Konfigurieren statt Codieren:

    - Die Konfiguration kann von einer Im geschäftlichen Bereich tätigen Person durchgeführt werden und erfordert keinen Entwickler.
    - Das Datenmodell ist betriebswirtschaftlich definiert.
    - Visuelle Editoren werden verwendet, um alle Komponenten der EB-Konfiguration zu erstellen.
    - Die Sprache, die für die Datentransformation verwendet wird, ähnelt der Sprache, die in Microsoft Excel verwendet wird.

- Eine Konfiguration für mehrere Dynamics 365 Finance-Releases:

    - Verwalten Sie ein domänenspezifisches Datenmodell, das betriebswirtschaftlich definiert ist.
    - Isolieren Sie Anwendungsreleasedetails in releaseabhängigen Datenmodellzuordnungen.
    - Pflegen Sie eine Formatkonfiguration für mehrere Releases der aktuellen Version, basierend auf dem Datenmodell.

- Einfaches oder automatisches Upgrade:

    - Versionsverwaltung von EB-Konfigurationen wird unterstützt.
    - Die Microsoft Dynamics Lifecycle Services (LCS) Assets-Bibliothek kann als Repository für EB-Konfigurationen zum Versionsaustausch verwendet werden.
    - Lokalisierungen, die auf ursprünglichen EB-Konfigurationen basieren, können als untergeordnete Versionen eingeführt werden.
    - Ein EB-Konfigurationsbaum wird als Werkzeug bereitgestellt, das hilft, Abhängigkeiten für Versionen zu kontrollieren.
    - Unterschiede in der Lokalisierung oder der Delta-Konfiguration werden aufgezeichnet, um ein automatisches Upgrade auf eine neue Version der ursprünglichen EB-Konfiguration zu ermöglichen.
    - Konflikte, die während des automatischen Upgrades von Lokalisierungsversionen entdeckt werden, können einfach manuell gelöst werden.

Mit EB können Sie elektronische Formatstrukturen definieren und anschließend beschreiben, wie diese Strukturen ausgefüllt werden sollen, indem Sie Daten und Algorithmen verwenden. Sie können eine Formelsprache verwenden, die der Excel-Sprache für die Datentransformation ähnelt. Um die Datenbank-zu-Format-Zuordnung leichter handhabbar, wiederverwendbar und unabhängig von Formatänderungen zu machen, wird ein Zwischendatenmodellkonzept eingeführt. Dieses Konzept ermöglicht das Ausblenden von Implementierungsdetails aus der Formatzuordnung und ermöglicht die Wiederverwendung eines einzelnen Datenmodells für mehrere Formatzuordnungen.

Sie können EB verwenden, um Formate für eingehende und ausgehende elektronische Dokumente in Übereinstimmung mit den gesetzlichen Anforderungen verschiedener Länder und Regionen zu konfigurieren. ER ermöglicht Ihnen, diese Formate während ihres Lebenszyklus zu verwalten. Sie können z.B. neue gesetzliche Vorgaben übernehmen und Geschäftsdokumente im erforderlichen Format generieren, um Informationen elektronisch mit Regierungsstellen, Banken und anderen Parteien auszutauschen.

Das ER-Modul ist für die Verwendung durch geschäftliche Benutzer anstatt Entwickler bestimmt. Da Sie Formate statt Code konfigurieren, ist der Prozess zum Erstellen und Anpassen von Formaten für elektronische Dokumente schneller und einfacher.

EB unterstützt zurzeit TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel und OPENXML-Arbeitsblattformate.

## <a name="capabilities"></a>Funktionen

Das ER-Modul hat folgende Funktionen:

- Es stellt ein einzelnes freigegebenes Tool für elektronische Berichterstellung in verschiedenen Domänen dar und ersetzt mehr als 20 verschiedene Module, die einige Arten der elektronischen Berichterstellung für Finance and Operations ausführen.
- Es erstellt ein Berichtsformat, das von der aktuellen Implementierung isoliert ist. Mit anderen Worten, das Format gilt für verschiedene Versionen.
- Es unterstützt die Erstellung eines benutzerdefinierten Formats, das auf einem ursprünglichen Format basiert. Es umfasst zudem Funktionen zum automatischen Aktualisieren von benutzerdefinierten Formaten, wenn am Originalformat Änderungen durch die Einführung von Lokalisierungs-/Anpassungsanforderungen entstehen.
- Es wird das primäre Standardtool zur Unterstützung von Lokalisierungsanforderungen in der elektronischen Berichterstellung, sowohl für Microsoft als auch für MS-Partner.
- Es unterstützt die Möglichkeit, Formate an Partner und Kunden über Microsoft Dynamics Lifecycle Services (LCS) zu verteilen.

## <a name="key-concepts"></a>Schlüsselkonzepte

### <a name="main-data-flow"></a>Hauptdatenfluss

[![EB-Hauptdatenfluss.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponenten

ER unterstützt die folgenden Komponententypen:

- Datenmodell
- Modellzuordnung
- Formate
- Metadaten

Weitere Informationen finden Sie unter [Komponenten der elektronischen Berichterstellung](er-overview-components.md).


#### <a name="component-versioning"></a>Teilversionsverwaltung

Die Versionsverwaltung wird für ER-Komponenten unterstützt. Der folgende Workflow wird für die Verwaltung von Änderungen in ER-Komponenten bereitgestellt:

1. Die Version, die ursprünglich erstellt wurde, ist als **Entwurf**-Version gekennzeichnet. Diese Version kann bearbeitet werden und ist für Testläufe verfügbar.
2. Die **Entwurf**-Version kann in eine **Abgeschlossen**-Version konvertiert werden. Diese Version kann in lokalen Berichtsprozessen verwendet werden.
3. Die **Abgeschlossen**-Version kann in eine **Freigegeben**-Version konvertiert werden. Diese Version wird im LCS veröffentlicht und kann in den globalen Berichterstellungsprozessen verwendet werden.
4. Die **Gemeinsam genutzt**-Version kann in eine **Eingestellt**-Version konvertiert werden. Diese Version kann anschließend gelöscht werden.

Versionen in einem **Abgeschlossen** oder **Gemeinsam genutzt**-Status sind für anderen Datenaustausch verfügbar. Die folgenden Aktionen können für eine Komponente mit diesen Status ausgeführt werden:

- Die Komponente kann im XML-Format serialisiert und als Datei im XML-Format exportiert werden.
- Die Komponente kann aus einer XML-Datei reserialisiert und als neue Version einer ER-Komponente in der Anwendung importiert werden.

#### <a name="component-date-effectivity"></a>Teildatumswirksamkeit

ER-Komponentenversionen haben ein Gültigkeitsdatum. Sie können das **Gültig ab**-Datum für eine ER-Komponente definieren, um das Datum anzugeben, ab dem diese Komponente für Berichtsprozesse wirksam wird. Das Anwendungs-Sitzungsdatum wird verwendet, um zu definieren, ob eine Komponente für die Ausführung gültig ist. Wenn mehrere Versionen für ein bestimmtes Datum gültig sind, wird die aktuellste Version für die Berichterstattung verwendet.

#### <a name="component-access"></a>Teilzugriff

Der Zugriff auf ER-Formatkomponenten hängt von den Einstellungen des ISO-Länder-/Regionscode ab. Wenn diese Einstellung für eine ausgewählte Version einer Formatkonfiguration leer ist, kann der Zugriff auf eine Formatkomponente von jedem Unternehmen aus zur Laufzeit erfolgen. Wenn diese Einstellung ISO-Länder-/Regionscodes enthält, steht eine Formatkomponente nur von Unternehmen zur Verfügung, die eine primäre Adresse besitzen, die für einen der ISO-Länder-/Regionscodes einer Formatkomponente definiert ist.

Für unterschiedliche Versionen einer Datenformatkomponente kann es verschiedene Einstellungen von ISO-Länder-/Regionscodes geben.

#### <a name="configuration"></a><a name="Configuration"></a>Konfiguration

Eine ER-Konfiguration ist der Wrapper einer bestimmten ER-Komponente. Diese Komponente kann entweder eine Datenmodellkomponente oder eine Formatkomponente sein. Eine Konfiguration kann unterschiedliche Versionen einer ER-Komponente beinhalten. Jede Konfiguration wird markiert als im Besitz von einem bestimmten Konfigurationsanbieter. Die **Entwurf**-Version einer Konfigurationskomponente kann bearbeitet werden, wenn der Besitzer einer Konfiguration als aktiver Anbieter in den ER-Einstellungen in der Anwendung ausgewählt wurde.

Jede Modellkonfiguration enthält eine Datenmodell-Komponente. Eine neue Format-Konfiguration kann von einer bestimmten Datenmodellkonfiguration abgeleitet sein. In der Konfigurationsstruktur wird die erstellte Formatkonfiguration als untergeordnetes Element der ursprünglichen Modellkonfiguration aufgeführt.

Die erstellte Formatkonfiguration enthält eine Format Komponente. Die Datenmodell-Komponente der ursprünglichen Modellkonfiguration wird automatisch in die Format -Komponente der untergeordneten Formatkonfiguration als Standard-Datenquelle eingefügt.

Eine ER-Konfiguration wird für Anwendungs-Unternehmen gemeinsam genutzt.

#### <a name="provider"></a><a name="Provider"></a>Anbieter

Der ER-Anbieter ist der Bezeichner einer Partei, die verwendet wird, um den Autor (Besitzer) jeder einzelnen ER-Konfiguration anzugeben. ER ermöglicht die Verwaltung einer Liste von Konfigurationsanbietern. Formatkonfigurationen, die als Teil der Finance and Operations-Lösung für elektronische Dokumente freigegeben sind, werden als Eigentum des **Microsoft**-Konfigurationsanbieters gekennzeichnet.

Informationen zum Registrieren eines neuen ER-Anbieters enthält der Aufgabenleitfaden **ER – Konfigurationsanbieter erstellen und als aktiv markieren** (Teil des Geschäftsprozesses **7.5.4.3 Erwerben/Entwickeln von IT-Service-/-Lösungskomponenten (10677)**).

#### <a name="repository"></a><a name="Repository"></a>Repository

Ein ER-Repository speichert ER-Konfigurationen. Folgende Typen von ER-Repositorys werden derzeit unterstützt: 

- Gemeinsame LCS-Bibliothek
- LCS-Projekt
- Dateisystem
- RCS
- Operations-Ressourcen
- Globales Repository

Ein **LCS-freigegebene Bibliothek** Repository bietet Zugriff auf die Liste der Konfigurationen innerhalb der freigegebenen Anlagebibilothek in den Lifecycle Services (LCS). Dieser Typ von ER-Repository kann nur für den Microsoft-Anbieter erfasst werden. Von der Bibliothek LCS-freigegebener Anlage können Sie die neuesten Versionen von ER-Konfigurationen in die aktuelle Instanz importieren.

Ein **LCS-Projekt**-Repository bietet Zugriff auf die Konfigurationsliste eines bestimmten LCS-Projekts (LCS-Projektanlagenbibliothek), das ausgewhlt wurde, wenn das Repository ausgewählt wurde. ER ermöglicht Ihnen, freigegebene Konfigurationen von der aktuellen Instanz in ein spezifisches **LCS-Projekt**-Repository hochzuladen. Sie können auch Konfigurationen aus einem **LCS-Projekt**-Repository in die aktuelle Instance Ihrer Apps für Finanzen und Betrieb importieren.

Ein **Dateisystem**-Repository bietet Zugriff auf die Liste von Konfigurationen, die sich als XML-Dateien im speziellen Ordner des lokalen Dateisystems des Computer befinden, auf dem der AOS-Dienst gehostet wird. Obligatorischer Ordner wird in der Repositoryregistrierungsphase ausgewählt. Sie können Konfigurationen aus einem **Dateisystem**-Repository in die aktuelle Instanz importieren. 

Beachten Sie, dass auf diesen Repositorytyp in die folgenden Umgebungen zugegriffen werden kann:

- Cloud gehostete Umgebungen, die für Entwicklungszwecke bereitgestellt werden (enthalten Testmodelle eingeschlossener Suiten)
- Lokal bereitgestellte Umgebungen (on-premises)

Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) importieren](./electronic-reporting-import-ger-configurations.md).

Ein **RCS**-Instanz-Repository bietet Zugriff auf die Konfigurationsliste einer bestimmten Instanz vom [Konfigurationsdienst](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration), der in der Repository-Registrierungsphase ausgewählt wurde. Mithilfe von EB können Sie abgeschlossene oder geteilte Konfigurationen aus der ausgewählten RCS-Instanz in die aktuelle Instanz importieren, damit Sie sie für die elektronische Berichterstellung verwenden können.

Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) aus RCS importieren](./rcs-download-configurations.md).

Ein **Globales** Repository bietet Zugriff auf die Liste der Konfigurationen innerhalb des globalen Repositorys im [Konfigurationsdienst](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Dieser Typ von ER-Repository kann nur für den Microsoft-Anbieter erfasst werden. Vom globalen Repository aus können Sie die neueste Version der ER-Konfiguration in die aktuelle Instanz importieren.

Weitere Informationen unter [Importieren von elektronischen Berichtstellungskonfigurationen aus dem globalen Repository der Konfigurationsdienste](./er-download-configurations-global-repo.md).

Ein **Betriebliches Ressourcen**-Repository bietet Zugriff auf die Liste der Konfigurationen, die Microsoft als ER-Konfigurationsanbieter bereitstellt, die ursprünglich als Teil der Anwendungslösung freigegeben wurden. Diese Konfigurationen können in die aktuelle Instanz importiert und für die elektronische Berichtserstellung verwendet werden oder als Muster-Aufgabenleitfaden abgespielt werden. Sie können auch für zusätzliche Lokalisierungen und Anpassungen verwendet werden. Beachten Sie, dass die neuesten Versionen, die von der Microsoft ER Konfigurationen bereitgestellt werden, von der Bibliothek der LCS-freigegebenen Anlagen importiert werden müssen, indem das ER-Repository entsprechend verwendet wird.

Benötigte **LCS-Projekt**-, **Dateisystem**- und **Gesetzliche Konfigurationsdienste (RCS)**-Repositorys können einzeln für jeden Konfigurationsanbieter der aktuellen Instanz registriert werden. Jedes Repository kann für einen bestimmten Konfigurationsanbieter dediziert werden.

## <a name="supported-scenarios"></a>Unterstützte Szenarien

### <a name="building-a-data-model"></a>Erstellen eines Datenmodells

ER bietet einen Modell-Designer an, den Sie verwenden können, um ein Datenmodell für eine bestimmte Geschäftsdomäne zu erstellen. Alle domänenspezifischen Geschäftsentitäten und deren Beziehungen untereinander, können in einem Datenmodell als hierarchische Struktur dargestellt werden. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Datenmodell entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="translating-data-model-content"></a>Übersetzen von Datenmodellinhalten

Ein Datenmodellinhalt (Etiketten und Beschreibungen) kann in andere Sprachen übersetzt werden, die von der Anwendung unterstützt werden. Sie möchten möglicherweise Datenmodellinhalte aus folgenden Gründen übersetzen:

- Um Inhalte für fremdsprachige Formatdesigner, die das Datenmodell zur Datenzuordnung von Formatkomponenten verwenden, zur Entwurfszeit verständlicher zu machen.
- Um Inhalte zur Laufzeit benutzerfreundlicher zu machen, indem Befehle und Hilfen für Laufzeitparameter sowie konfigurierte Prüfungsnachrichten (Fehler und Warnungen) in der bevorzugten Sprache des angemeldeten Benutzers angezeigt werden.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Konfigurieren von Datenmodellzuordnungen für ausgehende Dokumente

ER stellt einen Modellzuordnungsdesigner bereit, mit dem der Benutzer Datenmodelle, die zu bestimmten Anwendungsdatenquellen erstellt wurden, zuordnen kann. Auf Grundlage die Zuordnung werden die Daten zur Laufzeit aus ausgewählten Datenquellen in das Datenmodell importiert. Das Datenmodell wird dann als abstrakte Datenquelle der ER-Formate verwendet, die ausgehende elektronische Dokumente erstellen. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Definieren der Modellzuordnung und Auswählen von Datenquellen** und **ER-Datenmodell den ausgewählten Datenquellen zuordnen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Konfigurieren von Datenmodellzuordnungen für eingehende Dokumente

ER stellt einen Modellzuordnungsdesigner bereit, mit dem der Benutzer Datenmodelle, die zu bestimmten Ziele erstellt wurden, zuordnen kann. Beispielsweise können Datenmodelle den aktualisierbaren Datenkomponenten (Tabellen, Datenentitäten und Ansichten) zugeordnet werden. Basierend auf der Zuordnung werden die Daten zur Laufzeit unter Verwendung der Daten aus dem Datenmodell aktualisiert. Als abstrakte Lagerung des ER-Formats, wird das Datenmodell mit Daten aufgefüllt, die aus einem eingehenden elektronischen Dokument importiert werden. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Speichern einer entworfenen Modellkomponente als Modellkonfiguration

Mit ER kann ein entworfenes Datenmodell zusammen mit den entsprechenden Datenzuordnungen als Modellkonfiguration der aktuellen Instanz gespeichert werden. Die folgende Abbildung zeigt ein Beispiel für diesen Typ der Datenmodellkonfiguration (die Zahlungsmodellkonfiguration).

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **Er-Datenmodell den ausgewählten Datenquellen zuordnen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Erstellen eines Formats, das ein Datenmodell als Basis verwendet

ER unterstützt einen Formatdesigner, um ein Format eines elektronischen Dokuments für eine ausgewählte Geschäftsdomäne herzustellen, durch Auswählen der Modellkomponente als Basis. Der gleiche ER-Formatdesigner ermöglicht die Zuordnung eines erstellen Formats zu einer Datenmodellzuordnung einer ausgewählten Domäne als Datenquelle. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Format entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Erstellen einer Konfiguration, um elektronische Dokumente im OPENXML-Arbeitsblattformat zu generieren

Der ER-Formatdesigner kann zum Erstellen eines elektronischen Dokuments im OPENXML-Arbeitsblattformat verwendet werden. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Erstellen einer Konfiguration für Berichte im OPENXML-Format** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder. Als Teil des Schritts für das Importieren einer Vorlage im Aufgabenleitfaden, verwenden Sie die [Vorlage des Zahlungsberichts (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx)-Excel-Datei als Vorlage.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Erstellen einer Konfiguration, um elektronische Dokumente in einem Word-Dokumentformat zu generieren

Der ER-Formatdesigner kann zum Erstellen eines elektronischen Dokuments in einem Word-Dokumentformat verwendet werden. Die folgende Abbildung zeigt ein Beispiel für diesen Formattyp. Beachten Sie, dass dieses Format die vorhandene ER-Konfiguration erneut verwendet, die ursprünglich entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden ER Design einer Konfiguration zur Generierung von Berichten im Microsoft-WORD-Format (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder. Als Teil des Schritts für das Importieren einer Vorlage im Aufgabenleitfaden verwenden Sie die folgenden Word-Dateien als Vorlagen für das ER-Format:

- [Vorlage eines Zahlungsberichtes (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Begrenzte Vorlage eines Zahlungsberichtes (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Erstellen einer Konfiguration, um Daten von eingehenden elektronischen Dokumenten zu importieren

Der ER-Format-Designer kann verwendet werden, um ein elektronisches Dokument zu beschreiben, für das Datenimport in XML- oder Textformat geplant wird. Das entworfene Format wird verwendet, um ein eingehendes Dokument zu analysieren. Der ER-Formatzuordnungsdesigner kann verwendet werden, um die Bindung der Elemente des entworfenen Formats zum Datenmodell zu definieren. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden " Erforderliche ER-Konfigurationen zum Import von Daten aus einer externen Datei erstellen" (Teil des Geschäftsprozesses 7.5.4.3 Anschaffen/Entwickeln von IT-Dienstleistungs-/-Lösungskomponenten (10677)) wieder. Verwenden Sie die folgenden Dateien, um diesem Leitfaden wiederzugeben:

- [ER-Datenmodellkonfiguration (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER-Formatkonfiguration (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Beispiel eines eingehenden Dokuments im XML-Format (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Beispiel der Arbeitsmappe zur Verwaltung von Daten aus eingehenden Dokumenten (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Speichern einer entworfenen Formatkomponente in der Formatkonfiguration

Mit ER kann ein entworfenes Format zusammen mit den konfigurierten Datenzuordnungen als Formatkonfiguration der aktuellen Instanz gespeichert werden. Die vorherige Abbildung zeigt ein Beispiel für diesen Formatkonfigurationstyp (**BACS (UK)**, der der **Zahlungsmodell**-Konfiguration untergeordnet ist). Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Format entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Finance konfigurieren, um mit der internen Verwendung eines erstellten Formats zu beginnen

Die Anwendung kann so konfiguriert werden, dass die elektronische Berichtsgenerierung unter Verwendung eines erstellten Formats gestartet wird. Der Verweis auf die erstellte Formatkonfiguration sollte in den Einstellungen einer spezifischen Domäne definiert sein. Wenn Sie beispielsweise eine ER-Formatkonfigurierung für elektronische Kreditorenzahlungen im BACS-Format verwenden wollen, sollte auf die Formatkonfiguration in bestimmten Zahlungsmethoden verwiesen werden.

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Format zum Erstellen elektronischer Zahlungsdokumente verwenden** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

## <a name="handling-er-components"></a>ER-Komponenten handhaben

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Veröffentlichen einer ER-Komponente in LCS, um diese extern anzubieten (Lokalisierung)

Der Eigentümer einer erstellten Komponente (Modell oder Format) kann ER zum Veröffentlichen der abgeschlossenen Version dieser Komponente in LCS verwenden. HIerfür ist ein Repository des **LCS-Projekt**-Typs für den aktuellen ER-Konfigurationsanbieter erforderlich. Wenn der Status der abgeschlossenen Version einer Komponente von **ABGESCHLOSSEN** in **GEMEINSAM GENUTZT** geändert wird, wird diese Version in LCS veröffentlicht. Wenn eine Komponente in LCS veröffentlicht wurde, wird der Besitzer dieser Komponente ein Anbieter des Dienstes, und betreut diesen. Wenn beispielsweise diese Formatkomponente erstellt wurde, um ein elektronisches Dokument zu generieren, das gesetzlich obligatorisch ist (beispielsweise in Übereinstimmung mit dem Lokalisierungsszenario), wird vorausgesetzt, dass dieses Format mit den Gesetzesänderungen konform ist und der Anbieter neue Versionen der Komponente bereitstellt, sobald neue Gesetzgebungsanforderungen auftreten. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Upload einer Konfiguration nach Lifecycle Services** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importieren einer ER-Komponente aus LCS zur internen Nutzung

Mit ER können Sie ER-Komponenten aus LCS in die aktuelle Instanz importieren. Hierfür ist ein Repository des **LCS-Projekt**-Typs erforderlich. Wenn eine ER-Komponente aus LCS in die aktuelle Instanz importiert wurde, wird der Besitzer der Instanz ein Nutzer des Dienstes, der vom Besitzer der importierten Komponente (Autor) bereitgestellt wird. Wenn beispielsweise diese Formatkomponente entworfen wurde, um von der Anwendung ein bestimmtes elektronisches Dokument in einem bestimmten Länder-/Regionsformat zu generieren (Lokalisierungsszenario), wird davon ausgegangen, dass der Nutzer des Dienstes alle Aktualisierungen dieses Formats erhält, damit dieses weiter die Gesetzgebungsanforderungen erfüllt. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Import einer Konfiguration von Lifecycle Services** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Erstellen eines Formats, das ein anderes Format als Basis (Anpassung) auswählt

ER ermöglicht das Erstellen (Ableiten) einer neuen Komponente der aktuellen Komponentenversion (Basis), die aus LCS importiert wurde. Ein Benutzer möchte beispielsweise ein neues Format ableiten, um einige besonderen Anforderungen für ein elektronisches Dokument (wie ein zusätzliches Feld oder eine ausführliche Beschreibung) zu implementieren, die ein benutzerdefiniertes Szenario unterstützen. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Format durch Übernahme einer neuen zugehörigen Basisversion aktualisieren** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Aktualisieren eines Formats durch Auswählen einer neuen Basisformatversion (Rebasierung)

ER ermöglicht die automatische Übernahme von Änderungen der neuesten Version der Basiskomponente in die aktuelle Entwurfsversion der abgeleiteten Komponente. Dieser Prozess wird als *Rebasierung* bezeichnet. Beispielsweise können neue gesetzliche Änderungen, die in der neuesten Version der von LCS importierten Formatkomponente eingeführt wurden, automatisch in die eigene angepasste Version dieses elektronischen Dokumenteformats übernommen werden. Alle Änderungen, die nicht automatisch zusammengeführt werden können, werden als Konflikte betrachtet. Diese Konflikte werden zur manuellen Lösung im Designer-Tool für die entsprechende Komponente angezeigt. Um sich mit den Details dieses Szenarios vertraut zu machen, sehen Sie sich den Aufgabenleitfaden **ER Format-Upgrade durch Übernahme der neuen Basisversion dieses Formats** an (Teil des Geschäftsprozesses **7.5.5.3 Geänderte IT-Service-/Lösungskomponente erwerben/entwickeln (10683)**).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Liste der EB-Konfigurationen, die in Finance veröffentlicht wurden

Die Liste der EB-Konfigurationen für Finance wird ständig aktualisiert. Öffnen Sie das [globale Repository](er-download-configurations-global-repo.md), um die Liste der derzeit unterstützten EB-Konfigurationen zu überprüfen. Auf dem Inforegister **Details zur Einstellung** können Sie Informationen zu Konfigurationen überprüfen, die eingestellt wurden oder nicht mehr verwaltet werden. 

![Inhalt des globalen Repositorys auf der Konfigurationsrepository-Seite.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Eine Elektronische Berichterstellungskonfiguration (ER) erstellen](electronic-reporting-configuration.md)
- [Den Konfigurationslebenszyklus der elektronischen Berichterstellung (EB) verwalten](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
