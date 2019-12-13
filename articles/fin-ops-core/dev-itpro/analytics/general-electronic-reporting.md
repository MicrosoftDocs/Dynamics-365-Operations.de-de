---
title: Überblick über die elektronische Berichterstellung (Electronic reporting, ER)
description: Diese Thema bietet eine Übersicht zum elektronischen Berichterstellungstool. Es umfasst Informationen über wesentliche Konzepte, vom ER unterstützte Szenarien und eine Liste der Formate, die im Rahmen der Lösung entwickelt und veröffentlicht wurden.
author: NickSelin
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad6c1c7544f3c9d53b9d5759b246f81dae6cfe2c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771072"
---
# <a name="electronic-reporting-er-overview"></a>Überblick über die elektronische Berichterstellung (Electronic reporting, ER)

[!include [banner](../includes/banner.md)]

Diese Thema bietet eine Übersicht zum elektronischen Berichterstellungstool. Es umfasst Informationen über wesentliche Konzepte, vom ER unterstützte Szenarien und eine Liste der Formate, die im Rahmen der Lösung entwickelt und veröffentlicht wurden.

ER ist ein Tool, mit dem Sie Formate für eingehende und ausgehende elektronische Dokumente in Übereinstimmung mit den gesetzlichen Anforderungen verschiedener Länder/Regionen konfigurieren können. ER ermöglicht Ihnen, diese Formate während ihres Lebenszyklus zu verwalten. Sie können z.B. neue gesetzliche Vorgaben übernehmen und Geschäftsdokumente im erforderlichen Format generieren, um Informationen elektronisch mit Regierungsstellen, Banken und anderen Parteien auszutauschen.

Das ER-Modul ist für die Verwendung durch geschäftliche Benutzer anstatt Entwickler bestimmt. Da Sie Formate statt Code konfigurieren, ist der Prozess zum Erstellen und Anpassen von Formaten für elektronische Dokumente schneller und einfacher.

EB unterstützt zurzeit TEXT, XML, Microsoft Word-Dokumente und OPENXML-Arbeitsblattformate. Allerdings unterstützt eine Erweiterungsschnittstelle auch weitere Formate.

## <a name="capabilities"></a>Funktionen
Das ER-Modul hat folgende Funktionen:

- Es stellt ein einzelnes freigegebenes Tool für elektronische Berichterstellung in verschiedenen Domänen dar und ersetzt mehr als 20 verschiedene Module, die einige Arten der elektronischen Berichterstellung für Finance and Operations ausführen.
- Es erstellt ein Berichtsformat, das von der aktuellen Implementierung isoliert ist. Mit anderen Worten, das Format gilt für verschiedene Versionen.
- Es unterstützt die Erstellung eines benutzerdefinierten Formats, das auf einem ursprünglichen Format basiert. Es umfasst zudem Funktionen zum automatischen Aktualisieren von benutzerdefinierten Formaten, wenn am Originalformat Änderungen durch die Einführung von Lokalisierungs-/Anpassungsanforderungen entstehen.
- Es wird das primäre Standardtool zur Unterstützung von Lokalisierungsanforderungen in der elektronischen Berichterstellung, sowohl für Microsoft als auch für MS-Partner.
- Es unterstützt die Möglichkeit, Formate an Partner und Kunden über Microsoft Dynamics Lifecycle Services (LCS) zu verteilen.

## <a name="key-concepts"></a>Schlüsselkonzepte
### <a name="components"></a>Komponenten

ER unterstützt zwei Komponententypen: **Datenmodell** und **Format**.

#### <a name="data-model-components"></a>Datenmodellkomponenten

Eine Datenmodellkomponente ist eine abstrakte Darstellung der Datenstruktur. Es wird verwendet, um bestimmte Geschäftsdomänenbereiche mit ausreichend Details zu beschreiben, um die Berichtsanforderungen für diese Domäne zu erfüllen. Eine Datenmodellkomponente besteht aus den folgenden Teilen:

- Ein Datenmodell als ein Satz domänenspezifischer Geschäftseinheiten und einer hierarchisch strukturierten Definition von Beziehungen zwischen diesen Einheiten.
- Eine Modellzuordnung, die ausgewählte Anwendungsdatenquellen mit einzelnen Elementen eines Datenmodells verknüpft, das zur Laufzeit den Datenfluss und die Regeln der Geschäftsdatenauffüllung zu einer Datenmodellkomponente angibt.

Eine Geschäftseinheit eines Datenmodells wird als Container (Datensatz) dargestellt. Geschäftseinheitseigenschaften werden als Datenelemente (Felder) dargestellt. Jedes Datenelement hat eine(n) eindeutigen Namen, Beschriftung, Beschreibung und Wert. Der Wert jedes Datenelements kann so konzipiert werden, dass er als Zeichenfolge, Ganzzahl, Gleitkommazahl, Datum, Aufzählung, Boolesch, usw. erkannt wird. Außerdem kann er ein anderer Datensatz oder eine Datensatzliste sein.

Eine einzelne Datenmodellkomponente kann mehrere Hierarchien von domänenspezifischen Geschäftsentitäten enthalten. Sie kann auch Modellzuordnungen enthalten, die einen berichtspezifischen Datenfluss bei Laufzeit unterstützen. Die Hierarchien unterscheiden sich durch einen einzelnen Datensatz, der als Stamm zur Modellzuordnung ausgewählt wurde. Beispielsweise unterstützt das Datenmodell des Zahlungsdomänenbereichs möglicherweise die folgenden Zuordnungen:

- Unternehmen \> Kreditor \> Zahlungsbuchungen der Kreditorendomäne
- Debitor \> Unternehmen \> Zahlungsbuchungen der Debitorendomäne

Beachten Sie, dass Geschäftsentitäten (z. B. Unternehmens- und Zahlungstransaktionen) nur einmal erstellt werden. SIe werden von anderen Zuordnungen wiederverwendet.

Eine Modellzuordnung, die ausgehende elektronische Dokumente unterstützt, hat die folgenden Fähigkeiten:

- Sie kann verschiedene Datentypen als Datenquellen für ein Datenmodell verwenden. Beispielsweise kann sie Tabellen, Datenentitäten, Methoden oder Enumerationen verwenden.
- Sie unterstützt Benutzereingabeparameter, die als Datenquellen für ein Datenmodell definiert werden, wenn einige Daten in der Laufzeit angegeben werden müssen.
- Sie unterstützt die Umwandlung von Daten in die erforderlichen Gruppen. Sie können damit zudem Daten filtern, sortieren und zusammenfassen sowie logisch berechnete Felder anhängen, die mit Formeln entworfen werden, die Microsoft Excel-Formeln ähneln. Weitere Informationen finden Sie unter [Formuladesigner in der elektronischen Berichterstattung (ER)](general-electronic-reporting-formula-designer.md)).


Eine Zuordnung, die vorbildliche eingehende elektronische Dokumente unterstützt, umfasst die folgenden Funktionen:

- Sie kann unterschiedliche aktualisierbare Datenelemente als Ziele verwenden. Diese Datenelemente enthalten Tabellen, Datenentitäten und Ansichten. Die Daten kann mithilfe der Daten von eingehenden elektronischen Dokumenten aktualisiert werden. Mehrere Ziele können in einer einzelnen Modellzuordnung verwendet werden.
- Sie unterstützt Benutzereingabeparameter, die als Datenquellen für ein Datenmodell definiert werden, wenn einige Daten in der Laufzeit angegeben werden müssen.

Für jede Geschäftsdomäne wird eine Datenmodellkomponente entworfen, die als vereinheitlichte Datenquelle für die Berichtserstellung verwendet werden soll, und die die Berichtserstellung von der physischen Implementierung von Datenquellen isoliert. Sie stellt domänenspezifische Geschäftskonzepte und Funktionen in einem Formular dar, die den ersten Entwurf und die weitere Verwaltung eines Berichterstellungsformats effizienter macht.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenten für ausgehende elektronische Dokumente

Eine Formatkomponente ist das Schema der Berichtsausgabe, die zur Laufzeit generiert wird. Ein Schema besteht aus folgenden Elementen:

- Ein Format, das die Struktur und den Inhalt des zur Laufzeit generierten ausgehenden elektronischen Dokuments festlegt.
- Datenquellen als Satz von Benutzereingabeparametern und einem domänenspezifischen Datenmodell, das eine ausgewählte Modellzuordnung verwendet.
- Eine Formatzuordnung als Satz von Bindungen von Formatdatenquellen mit einzelnen Elementen des Formats, die den Datenfluss und die Regeln für Formatausgabegenerierung zur Laufzeit angeben.
- Eine Formatprüfung als Satz konfigurierbarer Regeln, die die Berichterstellung zur Laufzeit abhängig von ausgeführtem Kontext steuern. Beispielsweise könnte es eine Regel geben, die die ausgehende Generierung der Zahlungen eines Kreditors beendet und eine Ausnahme auslöst, wenn bestimmte Attribute des ausgewählten Kreditors fehlen, z. B: die Bankkontonummer.

Eine Formatkomponente unterstützt die folgenden Funktionen:

- Das Erstellen der Berichtsausgabe als individuelle Dateien in unterschiedlichen Formaten, wie Text, XML, Microsoft Word-Dokument oder Arbeitsblatt.
- Erstellen von mehreren Dateien getrennt sowie die Zusammenfassung von Dateien in Zip-Dateien.

Mit einer Formatkomponente können Sie bestimmte Dateien anzufügen, die in der Berichtsausgabe verwendet werden können:

- Excel-Arbeitsmappen, die Arbeitsblätter enthälten, die als Vorlage für Ausgaben im OPENXML-Arbeitsblattformat verwendet werden können
- Word-Dateien, die ein Dokument enthalten, das als Vorlage für Ausgaben im Microsoft Word-Dokumentformat verwendet werden kann
- Andere Dateien, die in die Ausgabe des Formats als vordefinierte Dateien übernommen werden können

Die folgende Abbildung zeigt, wie die Daten für diese Formate fließen.

[![Datenfluss für ausgehende Formatkomponenten](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Um eine einzelne ER-Formatkonfiguration ausführen und ein ausgehendes elektronisches Dokument zu generieren, müssen Sie die Zuordnung der Formatkonfiguration identifizieren.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formatkomponenten für eingehende elektronische Dokumente
Eine Formatkomponente ist das Schema des eingehenden Dokuments, das zur Laufzeit importiert wird. Ein Schema besteht aus folgenden Elementen:

- Ein Format, das die Struktur und den Inhalt des zur Laufzeit importierten eingehenden elektronischen Dokuments festlegt, das Daten enthält. Eine Formatkomponente wird verwendet, um ein eingehendes Dokument in verschiedenen Formaten, z. B. Text und XML, zu analysieren.
- Eine Formatzuordnung, die einzelne Formatelemente an die Elemente eines domänenspezifischen Datenmodells bindet. Zur Laufzeit geben die Elemente im Datenmodell den Datenfluss und die Regeln für das Importieren von Daten von einem eingehenden Dokument an und speichern die Daten anschließend in einem Datenmodell.
- Eine Formatprüfung als Satz konfigurierbarer Regeln, die den Datenimport zur Laufzeit abhängig von ausgeführtem Kontext steuern. Beispielsweise könnte es eine Regel geben, die den Datenimport eines Bankauszugs mit einer Kreditorzahlung beendet und eine Ausnahme auslöst, wenn die Attribute eines bestimmten Kreditors fehlen, z. B: der Lieferantenidentifizierungscode.

Die folgende Abbildung zeigt, wie die Daten für diese Formate fließen.

[![Datenfluss für eingehende Formatkomponenten](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Um eine einzelne ER-Formatkonfiguration auszuführen, um Daten von einem eingehenden elektronischen Dokument zu importieren, müssen Sie die gewünschte Zuordnung einer Formatkonfiguration und auch den Integrationspunkt einer Modellzuordnung identifizieren. Sie können dieselbe Modellzuordnung und Ziele zusammen mit verschiedenen Formaten für unterschiedliche Arten von eingehenden Dokumenten verwenden.

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

#### <a name="configuration"></a>Konfiguration

Eine ER-Konfiguration ist der Wrapper einer bestimmten ER-Komponente. Diese Komponente kann entweder eine Datenmodellkomponente oder eine Formatkomponente sein. Eine Konfiguration kann unterschiedliche Versionen einer ER-Komponente beinhalten. Jede Konfiguration wird markiert als im Besitz von einem bestimmten Konfigurationsanbieter. Die **Entwurf**-Version einer Konfigurationskomponente kann bearbeitet werden, wenn der Besitzer einer Konfiguration als aktiver Anbieter in den ER-Einstellungen in der Anwendung ausgewählt wurde.

Jede Modellkonfiguration enthält eine Datenmodell-Komponente. Eine neue Format-Konfiguration kann von einer bestimmten Datenmodellkonfiguration abgeleitet sein. In der Konfigurationsstruktur wird die erstellte Formatkonfiguration als untergeordnetes Element der ursprünglichen Modellkonfiguration aufgeführt.

Die erstellte Formatkonfiguration enthält eine Format Komponente. Die Datenmodell-Komponente der ursprünglichen Modellkonfiguration wird automatisch in die Format -Komponente der untergeordneten Formatkonfiguration als Standard-Datenquelle eingefügt.

Eine ER-Konfiguration wird für Anwendungs-Unternehmen gemeinsam genutzt.

#### <a name="provider"></a>Anbieter

Der ER-Anbieter ist der Bezeichner einer Partei, die verwendet wird, um den Autor (Besitzer) jeder einzelnen ER-Konfiguration anzugeben. ER ermöglicht die Verwaltung einer Liste von Konfigurationsanbietern. Formatkonfigurationen, die als Teil der Finance and Operations-Lösung für elektronische Dokumente freigegeben sind, werden als Eigentum des **Microsoft**-Konfigurationsanbieters gekennzeichnet.

Informationen zum Registrieren eines neuen ER-Anbieters enthält der Aufgabenleitfaden **ER – Konfigurationsanbieter erstellen und als aktiv markieren** (Teil des Geschäftsprozesses **7.5.4.3 Erwerben/Entwickeln von IT-Service-/-Lösungskomponenten (10677)**).

#### <a name="repository"></a>Repository

Ein ER-Repository speichert ER-Konfigurationen. Folgende Typen von ER-Repositorys werden derzeit unterstützt: 

- Gemeinsame LCS-Bibliothek
- LCS-Projekt
- Systemdatei
- Regulatory Configuration Services (RCS)
- Betriebliche Ressourcen


Ein **LCS-freigegebene Bibliothek** Repository bietet Zugriff auf die Liste der Konfigurationen innerhalb der freigegebenen Anlagebibilothek in den Lifecycle Services (LCS). Dieser Typ von ER-Repository kann nur für den Microsoft-Anbieter erfasst werden. Von der Bibliothek LCS-freigegebener Anlage können Sie die neuesten Versionen von ER-Konfigurationen in die aktuelle Instanz importieren.

Ein **LCS-Projekt**-Repository bietet Zugriff auf die Konfigurationsliste eines bestimmten LCS-Projekts (LCS-Projektanlagenbibliothek), das in dem Repository-Registrierungsstadium ausgewählt wurde. ER ermöglicht Ihnen, freigegebene Konfigurationen von der aktuellen Instanz in ein spezifisches **LCS-Projekt**-Repository hochzuladen. Sie können auch Konfigurationen aus einem **LCS-Projekt**-Repository in die aktuelle Finance and Operations-Instanz importieren.

Ein **Dateisystem**-Repository bietet Zugriff auf die Liste von Konfigurationen, die sich als XML-Dateien im speziellen Ordner des lokalen Dateisystems des Computer befinden, auf dem der AOS-Dienst gehostet wird. Obligatorischer Ordner wird in der Repositoryregistrierungsphase ausgewählt. Sie können Konfigurationen aus einem **Dateisystem**-Repository in die aktuelle Instanz importieren. 

Beachten Sie, dass auf diesen Repositorytyp in die folgenden Umgebungen zugegriffen werden kann:

- Cloud gehostete Umgebungen, die für Entwicklungszwecke bereitgestellt werden (enthalten Testmodelle eingeschlossener Suiten)
- Lokal bereitgestellte Umgebungen (on-premises)

Weitere Informationen finden Sie unter [Elektronische Berichterstellungskonfigurationen (ER) importieren](./electronic-reporting-import-ger-configurations.md).

Ein **RCS-Instanz**-Repository bietet Zugriff auf die Konfigurationsliste einer bestimmten RCS-Instanz, die in der Repository-Registrierungsphase ausgewählt wurde. Mithilfe von EB können Sie abgeschlossene oder geteilte Konfigurationen aus der ausgewählten RCS-Instanz in die aktuelle Instanz importieren, damit Sie sie für die elektronische Berichterstellung verwenden können.

Weitere Informationen unter [Importieren von elektronischen Berichtstellungskonfigurationen (ER) aus den Regulatory Configuration Services (RCS)](./rcs-download-configurations.md).

Ein **Betrieblichees Ressourcen**Repository bietet Zugriff auf die Liste der Konfigurationen, die Microsoft als ER-Konfigurationsanbieter bereitstellt, die ursprünglich als Teil der Anwendungslösung freigegeben wurden. Diese Konfigurationen können in die aktuelle Instanz importiert und für die elektronische Berichtserstellung verwendet werden oder als Muster-Aufgabenleitfaden abgespielt werden. Sie können auch für zusätzliche Lokalisierungen und Anpassungen verwendet werden. Beachten Sie, dass die neuesten Versionen, die von der Microsoft ER Konfigurationen bereitgestellt werden, von der Bibliothek der LCS-freigegebenen  Anlagen importiert werden müssen, indem das ER-Repository entsprechend verwendet wird.

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

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Erstellen einer Konfiguration für Berichte im OPENXML-Format** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder. Als Teil des Schritts für das Importieren einer Vorlage im Aufgabenleitfaden, verwenden Sie die [Vorlage des Zahlungsberichts (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)-Excel-Datei als Vorlage.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Erstellen einer Konfiguration, um elektronische Dokumente in einem Word-Dokumentformat zu generieren
Der ER-Formatdesigner kann zum Erstellen eines elektronischen Dokuments in einem Word-Dokumentformat verwendet werden. Die folgende Abbildung zeigt ein Beispiel für diesen Formattyp. Beachten Sie, dass dieses Format die vorhandene ER-Konfiguration erneut verwendet, die ursprünglich entworfen wurde, um die Berichtsausgabe im OPENXML-Format zu generieren.

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden ER Design einer Konfiguration zur Generierung von Berichten im Microsoft-WORD-Format (Teil des 7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)-Geschäftsprozesses) wieder. Als Teil des Schritts für das Importieren einer Vorlage im Aufgabenleitfaden verwenden Sie die folgenden Word-Dateien als Vorlagen für das ER-Format:

- [Vorlage eines Zahlungsberichtes (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Begrenzte Vorlage eines Zahlungsberichtes (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Erstellen einer Konfiguration, um Daten von eingehenden elektronischen Dokumenten zu importieren
Der ER-Format-Designer kann verwendet werden, um ein elektronisches Dokument zu beschreiben, für das Datenimport in XML- oder Textformat geplant wird. Das entworfene Format wird verwendet, um ein eingehendes Dokument zu analysieren. Der ER-Formatzuordnungsdesigner kann verwendet werden, um die Bindung der Elemente des entworfenen Formats zum Datenmodell zu definieren. 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden " Erforderliche ER-Konfigurationen zum Import von Daten aus einer externen Datei erstellen" (Teil des Geschäftsprozesses 7.5.4.3 Anschaffen/Entwickeln von IT-Dienstleistungs-/-Lösungskomponenten (10677)) wieder. Verwenden Sie die folgenden Dateien, um diesem Leitfaden wiederzugeben:

- [ER-Datenmodellkonfiguration (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER-Formatkonfiguration (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Beispiel eines eingehenden Dokuments im XML-Format (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Beispiel der Arbeitsmappe zur Verwaltung von Daten aus eingehenden Dokumenten (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

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

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-application"></a>Eine Liste von ER-Konfigurationen, die in der Finance-Anwendung bereitgestellt werden.

| Domänenspezifische Datenmodellkonfigurationen: Titel | Domäne                | Datenmodellabhängige Formatkonfigurationen: Titel | Beschreibung                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Protokolldateimodell                                 | Finanzprüfung       |                                                   |                                                                    |
|                                                  |                       | Protokolldatei (NL)                                   | Protokolldateiformat für Niederlande                                  |
| BAS-Modell                                        | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | Australischer Geschäftsvorgangsbericht (Business Activity Statement - BAS)                                          | Geschäftsvorgangsberichtsformat für Australien                                           |
| Bauindustrie-Schemamodell               | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | CIS monatlicher Umsatz (Großbritannien)                           | CIS Monatliches Umsatzformat für Großbritannien                   |
| Mahnschreibenmodell                          | elektronische Rechnungsstellung  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-Mahnschreiben (DK)                     | OIOUBL-Mahnschreibenformat für Dänemark                        |
| Elektronisches Sachkontomodell (MX)          | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | Hilfs-Sachkonto XML (MX)                         | "Hilfs-Sachkontenbuchungen pro Konto"-Berichtformat für Mexiko |
|                                                  |                       | Kontenplan XML (MX)                         | Kontenplan-Berichtsformat für Mexiko                          |
|                                                  |                       | Erfassungen XML (MX)                                 | Erfassungsbuchungen-Berichtsformat für Mexiko                      |
|                                                  |                       | Zwischenbilanz XML (MX)                            | Zwischenbilanz-Berichtformat für Mexiko                             |
| Elster-Modell                                     | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-Format für Deutschland                                          |
| Modell für zusammenfassende Meldung                              | Handelsbericht       |                                                   |                                                                    |
|                                                  |                       | Zusammenfassende Meldung (DE)                                | Zusammenfassende Meldung TXT-Format für Deutschland                               |
|                                                  |                       | Zusammenfassende Meldung (DK)                                | Zusammenfassende Meldung TXT-Format für Dänemark                               |
|                                                  |                       | Zusammenfassende Meldung (FR)                                | Zusammenfassende Meldung XML-Format für Frankreich                                |
|                                                  |                       | Zusammenfassende Meldung (NL)                                | Zusammenfassende Meldung XML-Format für Niederlande                           |
|                                                  |                       | Zusammenfassende Meldung (UK)                            | Zusammenfassende Meldung TXT-Format für Großbritannien                    |
|                                                  |                       | Zusammenfassende Meldung XML (UK)                            | Zusammenfassende Meldung XML-Format für Großbritannien                    |
|                                                  |                       | Bericht "Zusammenfassende Meldung nach Spalten"                   | Bericht "Zusammenfassende Meldung nach Spalten"                                    |
|                                                  |                       | Bericht "Zusammenfassende Meldung nach Zeilen"                      | Bericht "Zusammenfassende Meldung nach Zeilen"                                       |
| FEC-Buchhaltungsmodel (FR)                        | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | FEC-Buchhaltungsdaten XML (FR)                      | FEC-Buchhaltungsdatenexport XML-Format für Frankreich                   |
| Deutsche Protokolldatei                                | Finanzprüfung       |                                                   |                                                                    |
|                                                  |                       | Deutsche Ausgabeprotokolldatei                          | Ausgabeprotokolldatei für Deutschland und Österreich                          |
| Intrastat-Modell                                  | Handelsbericht       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat-Format für Deutschland                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat-Format für Dänemark                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM-Format für Frankreich                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC-Format für Frankreich                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat-Format für die Niederlande                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastat-Format für Großbritannien                            |
|                                                  |                       | Intrastat-Bericht                                  | Intrastat Excel Kontrollbericht                                     |
| Debitorenrechnungsmodell                           | elektronische Rechnungsstellung  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Projekt Gutschrift (DK)                   | OIOUBL Projekt Gutschrift-Format für Dänemark                      |
|                                                  |                       | OIOUBL Projektrechnung (DK)                       | OIOUBL Projektrechnung-Format für Dänemark                          |
|                                                  |                       | OIOUBL Verkaufsgutschrift (DK)                     | OIOUBL Verkaufsgutschrift-Format für Dänemark                        |
|                                                  |                       | OIOUBL Verkaufsrechnung (DK)                         | OIOUBL Verkaufsrechnungsformat für Dänemark                            |
| OB-Meldungsmodell                             | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | OB-Meldung (NL)                               | OB-Meldungsformat für die Niederlande                          |
| Zahlungsmodell                                    | Zahlungen              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice-Zahlungsformat für Dänemark                        |
|                                                  |                       | Wechselrimesse (FR)                  | Wechselrimesseformat für Frankreich                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91-Kreditorenzahlungsformat für die Niederlande                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB-Direktbelastungsformat für Frankreich                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB- inländische Kreditorenzahlung für Frankreich                    |
|                                                  |                       | Nordea Kreditor (DK)                                | Nordea Corporate Netbank Kreditorenzahlungsformat für Dänemark         |
|                                                  |                       | ANZ Direktkredit-Service (AU)                    | ANZ Direktkredit-Serviceformat für Australien                 |
|                                                  |                       | CBA Direktkredit-Service (AU)                    | CBA Direktkredit-Serviceformat für Australien                 |
|                                                  |                       | NAB Direktkredit-Service (AU)                    | NAB Direktkredit-Serviceformat für Australien                 |
|                                                  |                       | STG Direktkredit-Service (AU)                    | STG Direktkredit-Serviceformat für Australien                 |
|                                                  |                       | WBC Direkteingabe-System (AU)                      | WBC Direkteingabe-Systemformat für Australien                   |
|                                                  |                       | DirectLink (NZ)                                   | DirectLink-Format für Neuseeland                              |
|                                                  |                       | JBA-Zahlungsdatei (JP)                             | JBA Zahlungsformat für Japan                                       |
|                                                  |                       | Kreditübertragung (ISO20022)                          | SEPA Kreditübertragungsformat für Europa                             |
|                                                  |                       | Kreditübertragung (ISO20022) (FR)                     | SEPA Kreditübertragungsformat für Frankreich                             |
|                                                  |                       | Kreditübertragung (ISO20022) (DE)                     | SEPA Kreditübertragungsformat für Deutschland                            |
|                                                  |                       | Kreditübertragung (ISO20022) (NL)                     | SEPA Kreditübertragungsformat für die Niederlande                    |
|                                                  |                       | Bankeinzug (ISO20022)                             | SEPA Bankeinzugsformat für Europa                                |
|                                                  |                       | Bankeinzug (ISO20022) (FR)                        | SEPA Bankeinzugsformat für Frankreich                                |
|                                                  |                       | Bankeinzug (ISO20022) (DE)                        | SEPA Bankeinzugsformat für Deutschland                               |
|                                                  |                       | Bankeinzug (ISO20022) (NL)                        | SEPA Bankeinzugsformat für die Niederlande                       |
|                                                  |                       | BACS (UK)                                         | BACS Kreditorenzahlungsformat für Großbritannien                  |
| Verlagerung der Steuerschuld                                   | Steuererklärung         |                                                   |                                                                    |
|                                                  |                       | Verkaufsliste für Verlagerungen der Steuerschuld                         | Verkaufslistenformat für Verlagerungen der Steuerschuld                                   |
| Niederländisches XBRL-Integrationsmodell                     | XBRL-Berichtstellung        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL-Exportformat für die Niederlande                    |
| GAF-Modell (MY)                                   | Finanzprüfung       |                                                   |                                                                    |
|                                                  |                       | GAF-Datei (MY)                                     | GAF-Format für Malaysia                                         |
| Kreditoren-Fälligkeitsbericht (CN)                         | Kreditoren-Datenanalyse |                                                   |                                                                    |
|                                                  |                       | Format "Kreditorenfälligkeitsbericht" (CN)                   | Format "Kreditorenfälligkeitsbericht" für China                               |
| Kreditorenrechnungserklärung-Model                 | Kreditoren-Datenanalyse |                                                   |                                                                    |
|                                                  |                       | Kreditorenrechnungserklärung (IS)                   | "Kreditorenrechnungserklärung"-Format für Island                      |
|                                                  |                       | Bericht 'Kreditorenrechnungserklärung' (IS)            | "Kreditorenrechnungserklärung"-Bericht für Island                      |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Erstellen von Konfigurationen für elektronische Meldungen (ER) ](electronic-reporting-configuration.md)
- [Den Konfigurationslebenszyklus der elektronischen Berichterstellung (EB) verwalten](general-electronic-reporting-manage-configuration-lifecycle.md)
