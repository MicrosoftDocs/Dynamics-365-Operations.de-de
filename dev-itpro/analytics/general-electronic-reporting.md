---
title: "Überblick über die elektronische Berichterstellung"
description: "Dieser Artikel enthält Informationen über das elektronische Berichterstellungstool. Es umfasst Informationen über wesentliche Konzepte, vom ER unterstützte Szenarien und eine Liste der Formate, die im Rahmen der Lösung entwickelt und veröffentlicht wurden."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: abe9212372fb7429d68c1fb6b32ec1d15c20a6d7
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-reporting-overview"></a>Überblick über die elektronische Berichterstellung

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält Informationen über das elektronische Berichterstellungstool. Es umfasst Informationen über wesentliche Konzepte, vom ER unterstützte Szenarien und eine Liste der Formate, die im Rahmen der Lösung entwickelt und veröffentlicht wurden.

Die Elektronische Berichterstellung (ER/Electronic reporting) ist ein Tool, mit dem Sie Formate für elektronische Dokumente gemäß der gesetzlichen Vorschriften verschiedener Länder/Regionen konfigurieren können. ER ermöglicht Ihnen, diese Formate während ihres Lebenszyklus zu verwalten. Sie können z.B. neue gesetzliche Vorgaben übernehmen und Geschäftsdokumente im erforderlichen Format generieren, um Informationen elektronisch mit Regierungsstellen, Banken und anderen Parteien auszutauschen. Das ER-Modul ist für die Verwendung durch geschäftliche Benutzer anstatt Entwickler bestimmt. Da Sie Formate und keinen Code, konfigurieren, ist der Prozess des Erstellens und Anpassens von Formaten für elektronische Dokumente schneller und einfacher. ER unterstützt zurzeit TEXT, XML und OPENXML Arbeitsblatt-Formate. Allerdings unterstützt eine Erweiterungsschnittstelle auch weitere Formate.

## <a name="capabilities"></a>Funktionen
Das ER-Modul hat folgende Funktionen:

-   Es stellt ein einzelnes allgemeines Tool für elektronische Berichterstellung in verschiedenen Domänen dar, das mehr als 20 verschiedene Module, die einige Arten der elektronischen Berichterstellung von Microsoft Dynamics 365 for Operations ausführen, ersetzt.
-   Es erstellt ein Berichtsformat, das von der aktuellen Microsoft Dynamics 365 for Operations-Implementierung isoliert ist. (In anderen Worten, das Format gilt für verschiedene Versionen von Microsoft Dynamics 365 for Operations.)
-   Es unterstützt die Erstellung eines benutzerdefinierten Formats, das auf einem ursprünglichen Format basiert. Es umfasst Funktionen zum automatischen Aktualisieren von benutzerdefinierten Formaten, wenn am Originalformat Änderungen durch die Einführung von Lokalisierungs-/Anpassungsanforderungen entstehen.
-   Es wird das primäre Standardtool zur Unterstützung von Lokalisierungsanforderungen in der elektronischen Berichterstellung, sowohl für Microsoft als auch für MS-Partner.
-   Es unterstützt die Möglichkeit, Formate an Partner und Kunden über Microsoft Dynamics Lifecycle Services (LCS) zu verteilen.

## <a name="concepts"></a>Konzepte
### <a name="components"></a>Komponenten

ER unterstützt zwei Komponententypen: **Datenmodell**und **Format**.

#### <a name="data-model-components"></a>Datenmodellkomponenten

Eine Datenmodellkomponente ist eine abstrakte Darstellung einer Datenstruktur und wird zum Beschreiben bestimmter Geschäftsdomänenbereiche mit ausreichenden Details zum Erfüllen der Meldeanforderungen in dieser Domäne verwendet. Eine Datenmodellkomponente besteht aus den folgenden Teilen:

-   Ein Datenmodell als ein Satz domänenspezifischer Geschäftseinheiten und einer hierarchisch strukturierten Definition von Beziehungen zwischen diesen Einheiten
-   Eine Modellzuordnung, die ausgewählte Microsoft Dynamics 365 for Operations-Datenquellen mit einzelnen Elementen eines Datenmodells verknüpft, das zur Laufzeit den Datenfluss und die Regeln der Geschäftsdatenauffüllung zu einer Datenmodellkomponente angibt.

Eine Geschäftseinheit eines Datenmodells wird als Container (Datensatz) dargestellt. Geschäftseinheitseigenschaften werden als Datenelemente (Felder) dargestellt. Jedes Datenelement hat eine(n) eindeutigen Namen, Beschriftung, Beschreibung und Wert. Der Wert jedes Datenelements kann so konzipiert werden, dass er als Zeichenfolge, Ganzzahl, Gleitkommazahl, Datum, Aufzählung, Boolesch, u.s.w. erkannt wird. Außerdem kann er ein anderer Datensatz oder eine Datensatzliste sein. Eine einzelne Datenmodellkomponente kann mehrere Hierarchien domänenspezifischer Geschäftseinheiten sowie Modellzuordnungen, die einen bestimmten berichtsspezifischen Datenfluss zur Laufzeit unterstützen, beinhalten. Die Hierarchien unterscheiden sich durch einen einzelnen Datensatz, der als Stamm zur Modellzuordnung ausgewählt wurde. Beispielsweise unterstützt das Datenmodell des Zahlungsdomänenbereichs möglicherweise die folgenden Zuordnungen:

-   Unternehmen -&gt; Kreditor -&gt; Zahlungsbuchungen der Kreditorendomäne
-   Debitor -&gt; Unternehmen -&gt; Zahlungsbuchungen der Debitorendomäne

Beachten Sie, dass Geschäftsentitäten (z. B. Unternehmens- und Zahlungstransaktionen) nur einmal erstellt werden. SIe werden von anderen Zuordnungen wiederverwendet. Eine Modellzuordnung hat folgende Funktionen:

-   Sie kann verschiedene Datentypen von Dynamics 365 for Operations als Datenquellen für ein Datenmodell verwenden. Beispielsweise kann sie Tabellen, Datenentitäten, Methoden oder Enumerationen verwenden.
-   Sie unterstützt Benutzereingabeparameter, die als Datenquellen für ein Datenmodell definiert werden, wenn einige Daten in der Laufzeit angegeben werden müssen.
-   Sie unterstützt die Umwandlung von Dynamics 365 for Operations-Daten in erforderlichen Gruppen, das Filtern, Sortieren und Summieren von Daten sowie das Anfügen logisch berechneter Felder, die mit Microsoft Excel-ähnlichen Formeln entworfen wurden (Weitere Informationen finden Sie unter [Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)).

[![Excel-Formeleditor](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Eine Datenmodellkomponente wird für jede Geschäftsdomäne entworfen, die als einheitliche Datenquelle für die Berichterstellung verwendet werden soll, die die Berichterstellung von der physischen Implementierung der Microsoft Dynamics 365 for Operations-Datenquellen isoliert und domänenspezifische Geschäftskonzepte und Funktionen in einer Form darstellt, die den ursprünglichen Entwurf und die weitere Verwaltung der Berichterstellungsformate effizienter macht.

#### <a name="format-components"></a>Formatkomponenten

Eine Formatkomponente ist das Schema der Berichtsausgabe, die zur Laufzeit generiert wird. Ein Schema besteht aus folgenden Elementen:

-   Ein Format, das die Struktur und den Inhalt des zur Laufzeit generierten elektronischen Berichtsdokuments festlegt
-   Datenquellen als Satz von Benutzereingabeparametern und einem domänenspezifischen Datenmodell, das eine ausgewählte Modellzuordnung verwendet
-   Eine Formatzuordnung als Satz von Bindungen von Formatdatenquellen mit einzelnen Elementen des Formats, die den Datenfluss und die Regeln der Formatausgabegenerierung zur Laufzeit angeben
-   Eine Formatprüfung als Satz konfigurierbarer Regeln, die die Berichterstellung zur Laufzeit abhängig vom ausgeführten Kontext steuern (z. B. eine Regel, die die Ausgabegenerierung einer Kreditorenzahlung beendet und eine Ausnahme auslöst, wenn bestimmte Attribute des ausgewählten Kreditors fehlen, wie z. B. die Kontonummer).

Eine Formatkomponente unterstützt die folgenden Funktionen:

-   Erstellen von Berichtsausgaben als einzelne Dateien in unterschiedlichen Formaten: Text, XML oder Arbeitsblatt
-   Erstellen von mehreren Dateien getrennt sowie die Zusammenfassung von Dateien in Zip-Dateien

Eine Formatkomponente bietet die Möglichkeit, bestimmte Dateien anzufügen, die in der Berichtsausgabe verwendet werden können:

-   Excel-Arbeitsmappen, die Arbeitsblätter enthälten, die als Vorlage für Ausgaben im OPENXML-Arbeitsblattformat verwendet werden können
-   Andere Dateien, die in die Ausgabe des Formats als vordefinierte Dateien übernommen werden können

#### <a name="component-versioning"></a>Teilversionsverwaltung

Die Versionsverwaltung wird für ER-Komponenten unterstützt. Der folgende Workflow wird für die Verwaltung von Änderungen in ER-Komponenten bereitgestellt:

-   Die Version, die ursprünglich erstellt wurde, ist als **ENTWURF**-Version gekennzeichnet. Diese Version kann bearbeitet werden und ist für Testläufe verfügbar.
-   Die**ENTWURF**-Version kann in eine **ABGESCHLOSSEN**-Version konvertiert werden. Diese Version kann in lokalen Berichtsprozessen verwendet werden.
-   Die **ABGESCHLOSSEN**-Version kann in eine **FREIGEGEBEN**-Version konvertiert werden. Diese Version wird im LCS veröffentlicht und kann in den globalen Berichterstellungsprozessen verwendet werden.
-   Die **GEMEINSAM GENUTZT**-Version kann in eine **EINGESTELLT**-Version konvertiert werden. Diese Version kann anschließend gelöscht werden.

Versionen in einem **ABGESCHLOSSEN** oder **GEMEINSAM**-Status sind für anderen Datenaustausch verfügbar. Für eine Komponente mit diesen Status können folgende Aktionen ausgeführt werden:

-   Sie können im XML-Format serialisiert und als Datei im XML-Format in Dynamics 365 for Operations exportiert werden.
-   Sie können aus einer XML-Datei neu serialisiert und in Dynamics 365 for Operations als neue Version einer ER-Komponente importiert werden.

#### <a name="component-date-effectivity"></a>Teildatumswirksamkeit

ER-Komponentenversionen haben ein Gültigkeitsdatum. Das**Gültig ab**-Datum kann für eine ER-Komponente definiert werden, um das Datum anzugeben, ab dem diese Komponente für Berichtsprozesse wirksam wird. Das Microsoft Dynamics 365 for Operations-Sitzungsdatum wird verwendet, um zu definieren, ob eine Komponente für die Ausführung gültig ist. Wenn mehrere Versionen für ein bestimmtes Datum gültig sind, wird die aktuellste Version für die Berichterstattung verwendet.

#### <a name="component-access"></a>Teilzugriff

Der Zugriff auf ER-Formatkomponenten hängt von den Einstellungen des ISO-Länder-/Regionscode ab. Wenn diese Einstellung für eine ausgewählte Version einer Format-Konfiguration leer ist, kann ein Zugriff auf eine Format-Komponente von jedem Dynamics 365 for Operations-Unternehmen zur Laufzeit erfolgen. Wenn diese Einstellung ISO-Länder-/Regionscodes enthält, ist eine Formatkomponente nur bei Microsoft Dynamics 365 for Operations-Unternehmen verfügbar, deren primäre Adresse für einen der ISO Länder-/Regionscodes diser Formatkomponente definiert ist. Für unterschiedliche Versionen einer Datenformatkomponente kann es verschiedene Einstellungen von ISO-Länder-/Regionscodes geben.

#### <a name="configuration"></a>Konfiguration

Eine ER-Konfiguration ist der Wrapper einer bestimmten ER-Komponente, entweder **Datenmodell**oder **Format**. Eine Konfiguration kann unterschiedliche Versionen einer bestimmten ER-Komponente beinhalten. Jede Konfiguration wird markiert als im Besitz von einem bestimmten Konfigurationsanbieter. Die **ENTWURF**-Version einer Konfigurationskomponente kann bearbeitet werden, wenn der Besitzer einer Konfiguration als aktiver Anbieter in den ER-Einstellungen in Microsoft Dynamics 365 for Operations ausgewählt wurde. Jede Modellkonfiguration enthält eine **Datenmodell**-Komponente. Eine neue Format-Konfiguration kann von einer bestimmten Datenmodellkonfiguration stammen (abgeleitet sein). Die erstellte Formatkonfiguration wird in der Konfigurationsstruktur als untergeordnetes Element der ursprünglichen Modellkonfiguration aufgeführt. Die erstellte Formatkonfiguration enthält eine **Format**Komponente. Die **Datenmodell**-Komponente der ursprünglichen Modellkonfiguration wird automatisch in die **Format**-Komponente der untergeordneten Formatkonfiguration als Standard-Datenquelle eingefügt. Eine ER-Konfiguration wird für Dynamics 365 for Operations-Unternehmen gemeinsam genutzt.

#### <a name="provider"></a>Anbieter

Der ER-Anbieter ist der Bezeichner einer Partei, die verwendet wird, um den Autor (Besitzer) jeder einzelnen ER-Konfiguration anzugeben. ER ermöglicht die Verwaltung einer Liste von Konfigurationsanbietern. Die Formatkonfigurationen, die als Teil der Dynamics 365 for Operations-Lösung für elektronische Dokumente freigegeben werden, sind als dem **Microsoft**-Konfigurationsanbieter zugehörig gekennzeichnet.

#### <a name="repository"></a>Repository

Ein ER-Repository speichert ER-Konfigurationen. Folgende Typen von ER-Repositorys werden derzeit unterstützt: **Operations-Ressourcen**und **LCS-Projekt**. Ein **Operations-Ressourcen**-Repository bietet Zugriff auf die Konfigurationsliste, die als Teil der Dynamics 365 for Operations-Lösung von Microsoft als ER-Konfigurationsanbieter freigegeben werden. Diese Konfigurationen können in die aktuelle Dynamics 365 for Operations-Instanz importiert und für elektronische Berichterstellung verwendet werden. Sie können auch für zusätzliche Lokalisierungen/Anpassungen verwendet werden. Ein **LCS-Projekt**-Repository bietet Zugriff auf die Konfigurationsliste eines bestimmten LCS-Projekts (LCS-Projektanlagenbibliothek), das in dem Repository-Registrierungsstadium ausgewählt wurde. ER ermöglicht das Hochladen freigegebener Konfigurationen aus der aktuellen Dynamics 365 for Operations-Instanz zu einem bestimmten **LCS-Projekt**-Repository. Sie können auch Konfigurationen aus einem bestimmten **LCS-Projekt**-Repository in die aktuelle Dynamics 365 for Operations-Instanz importerien. Erforderliche **LCS-Projekt**-Repositorys können für jeden Konfigurationsanbieter der aktuellen Dynamics 365 for Operations-Instanz einzeln erfasst werden. Jedes Repository kann für einen bestimmten Konfigurationsanbieter dediziert werden.

## <a name="supported-scenarios"></a>Unterstützte Szenarien
### <a name="building-a-data-model"></a>Erstellen eines Datenmodells

ER bietet einen Modell-Designer an, den Sie verwenden können, um ein Datenmodell für eine bestimmte Geschäftsdomäne zu erstellen. Alle domänenspezifischen Geschäftsentitäten und deren Beziehungen untereinander, können in einem Datenmodell als hierarchische Struktur dargestellt werden. Die folgende Abbildung zeigt ein Beispiel für diesen Datenmodelltyp (das Zahlungsdomänendatenmodell). [![Beispiel zu Datenmodell](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Datenmodell entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="translating-data-model-content"></a>Übersetzen von Datenmodellinhalten

Ein Datenmodellinhalt (Etiketten und Beschreibungen) kann in andere Sprachen übersetzt werden, die von Dynamics 365 for Operations unterstützt werden. Sie möchten möglicherweise Datenmodellinhalte aus folgenden Gründen übersetzen:

-   Um Inhalte für fremdsprachige Formatdesigner, die ein Datenmodell zur Datenzuordnung von Formatkomponenten verwenden, zur Entwurfszeit verständlicher zu machen
-   Um Inhalte zur Laufzeit benutzerfreundlicher zu machen, indem Befehle und Hilfen für Laufzeitparameter sowie konfigurierte Prüfungsnachrichten (Fehler und Warnungen) in der bevorzugten Sprache des angemeldeten Dynamics 365 for Operations-Benutzers angezeigt werden.

Die folgende Abbildung zeigt ein Beispiel, wie Datenmodellinhalte von Englisch auf Japanisch übersetzt werden können. [![Datenmodellinhalt auf Englisch](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Datenmodellinhalt übersetzt in Japanisch](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Konfigurieren von Datenmodellzuordnungen

ER stellt einen Modellzuordnungsdesigner bereit, mit dem der Benutzer Datenmodelle, die zu bestimmten Dynamics 365 for Operations-Datenquellen erstellt wurden, zuordnen kann. Die folgende Abbildung zeigt ein Beispiel einer solchen Typs der Datenmodellzuordnung (die **Kreditübertragung (SEPA)**-Modellzuordnung des Zahlungsdomänendatenmodells). [![Beispiel der Datenmodellzuordnung](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Definieren der Modellzuordnung und Auswählen von Datenquellen** und **ER-Datenmodell den ausgewählten Datenquellen zuordnen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Speichern einer entworfenen Modellkomponente als Modellkonfiguration

Mit ER kann ein entworfenes Datenmodell zusammen mit den entsprechenden Datenzuordnungen als Modellkonfiguration der aktuellen Dynamics 365 for Operations-Instanz gespeichert werden. Die folgende Abbildung zeigt ein Beispiel für diesen Typ der Datenmodellkonfiguration (die Zahlungsmodellkonfiguration). [![Beispiel zu Datenmodellkonfiguration ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Datenmodell entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Erstellen eines Formats, das ein Datenmodell als Basis verwendet

ER unterstützt einen Formatdesigner, um ein Format eines bestimmten elektronischen Dokuments für eine ausgewählte Geschäftsdomäne herzustellen, durch Auswählen der Modellkomponente als Basis. Der gleiche ER-Formatdesigner ermöglicht die Zuordnung eines erstellen Formats zu einer Datenmodellzuordnung einer ausgewählten Domäne als Datenquelle. Die folgende Abbildung zeigt ein Beispiel für diesen Formattyp (die Formatkonfiguration, die das **BACS**-Zahlungsformat für Großbritannien unterstützt). [![Beispiel zu einem Format, dass ein Datenmodel als Basis hat](./media/pic-format-1024x690.png)](./media/pic-format.png) Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Datenmodell Format** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Erstellen einer Konfiguration, um elektronische Dokumente im OPENXML-Arbeitsblattformat zu generieren

Der ER-Formatdesigner kann zum Erstellen eines bestimmten elektronischen Dokuments im OPENXML-Arbeitsblattformat verwendet werden. Die folgende Abbildung zeigt ein Beispiel des Formats dieses Typs angeben "eine Formatkonfiguration, um von OPENXML-Arbeitsblatt mit Details einer ausgewählten Zahlungserfassung zu generieren: [![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Mit dem mit den Details dieses Szenarios vertraut werden, geben Sie den **ER Erstellen einer Konfiguration für Berichte in OPENXML-Format** erneut Aufgabenleitfaden wieder (Teil **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677**)-Geschäftsprozesses). Verwenden Sie die unten genannte Excel-Datei als Vorlage zum Entwerfen eines ER-Formates um den Schritt zum Importieren einer Formatvorlage dieses Handbuchs abzuschließen: [Vorlage Zahlungsbericht (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Speichern einer entworfenen Formatkomponente in der Formatkonfiguration

Mit ER kann ein entworfenes Format zusammen mit den konfigurierten Datenzuordnungen als Formatkonfiguration der aktuellen Dynamics 365 for Operations-Instanz gespeichert werden. Die vorherige Abbildung zeigt ein Beispiel für diesen Formatkonfigurationstyp (**BACS (UK)**, der der **Zahlungsmodell**-Konfiguration untergeordnet ist). Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Domänenspezifisches Format entwerfen** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Dynamics 365 for Operations konfigurieren, um mit der internen Verwendung eines erstellten Formats zu beginnen

Dynamics 365 for Operations kann so konfiguriert werden, dass die elektronische Berichtsgenerierung unter Verwendung eines erstellten Formats gestartet wird. Der Verweis auf die erstellte Formatkonfiguration sollte in den Einstellungen einer spezifischen Domäne definiert sein. Wenn Sie beispielsweise eine ER-Formatkonfigurierung für elektronische Kreditorenzahlungen im BACS-Format verwenden wollen, sollte auf die Formatkonfiguration in bestimmten Zahlungsmethoden verwiesen werden, wie in den folgenden Abbildungen gezeigt 

[![BACS (Großbritannien ) Formatkonfiguration](media/ger-bacs-uk-format-configuration.png) 

[![Auf das BACS (Großbritannien) Format in einer Zahlungsmethode verweisen](media/ger-bacs-uk-format-method.png) 

Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Format zum Erstellen elektronischer Zahlungsdokumente verwenden** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

## <a name="handling-er-components"></a>ER-Komponenten handhaben
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Veröffentlichen einer ER-Komponente in LCS, um diese extern anzubieten (Lokalisierung)

Der Eigentümer einer erstellten Komponente (Modell oder Format) kann ER zum Veröffentlichen der abgeschlossenen Version dieser Komponente in LCS verwenden. HIerfür ist ein Repository des **LCS-Projekt**-Typs für den aktuellen ER-Konfigurationsanbieter erforderlich. Wenn der Status der abgeschlossenen Version einer Komponente von **ABGESCHLOSSEN** in **GEMEINSAM GENUTZT** geändert wird, wird diese Version in LCS veröffentlicht. Wenn eine Komponente in LCS veröffentlicht wurde, wird der Besitzer dieser Komponente ein Anbieter des Dienstes, und betreut diesen. Wenn beispielsweise diese Formatkomponente erstellt wurde, um ein elektronisches Dokument zu generieren, das gesetzlich obligatorisch ist (beispielsweise in Übereinstimmung mit dem Lokalisierungsszenario), wird vorausgesetzt, dass dieses Format mit den Gesetzesänderungen konform ist und der Anbieter neue Versionen der Komponente bereitstellt, sobald neue Gesetzgebungsanforderungen auftreten. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Upload einer Konfiguration nach Lifecycle Services**(Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importieren einer ER-Komponente aus LCS zur internen Nutzung

Mit ER können Sie ER-Komponenten aus LCS in die aktuelle Dynamics 365 for Operations-Instanz importieren. Hierfür ist ein Repository des **LCS-Projekt**-Typs erforderlich. Wenn eine ER-Komponente aus LCS in die aktuelle Dynamics 365 for Operations-Instanz importiert wurde, wird der Besitzer der Instanz ein Nutzer des Dienstes, der vom Besitzer der importierten Komponente (Autor) bereitgestellt wird. Wenn beispielsweise diese Formatkomponente entworfen wurde, um von Dynamics 365 for Operations ein bestimmtes elektronisches Dokument in einem bestimmten Länder-/Regionsformat zu generieren (Lokalisierungsszenario), wird davon ausgegangen, dass der Nutzer des Dienstes alle Aktualisierungen dieses Formats erhält, damit dieses weiter die Gesetzgebungsanforderungen erfüllt. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Import einer Konfiguration von Lifecycle Services** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Erstellen eines Formats, das ein anderes Format als Basis (Anpassung) auswählt

ER ermöglicht das Erstellen (Ableiten) einer neuen Komponente der aktuellen Komponentenversion (Basis), die aus LCS importiert wurde. Ein Benutzer möchte beispielsweise ein neues Format ableiten, um einige besonderen Anforderungen für ein elektronisches Dokument (wie ein zusätzliches Feld oder eine ausführliche Beschreibung) zu implementieren, die ein benutzerdefiniertes Szenario unterstützen. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Format durch Übernahme einer neuen zugehörigen Basisversion aktualisieren** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Aktualisieren eines Formats durch Auswählen einer neuen Basisformatversion (Rebasierung)

ER ermöglicht die automatische Übernahme von Änderungen der neuesten Version der Basiskomponente in die aktuelle Entwurfsversion der abgeleiteten Komponente. Dieser Prozess wird als *Rebasierung* bezeichnet. Beispielsweise können neue gesetzliche Änderungen, die in der neuesten Version der von LCS importierten Formatkomponente eingeführt wurden, automatisch in die eigene angepasste Version dieses elektronischen Dokumenteformats übernommen werden. Alle Änderungen, die nicht automatisch zusammengeführt werden können, werden als Konflikte betrachtet. Diese Konflikte werden zur manuellen Lösung im Designer-Tool für die entsprechende Komponente angezeigt. Um sich mit den Details dieses Szenarios vertraut zu machen, geben Sie den Aufgabenleitfaden **ER Format durch Übernahme einer neuen zugehörigen Basisversion aktualisieren** (Teil des **7.5.4.3 IT-Dienstleistungs-/-Lösungskomponenten anschaffen/entwickeln (10677)**-Geschäftsprozesses) wieder.

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Eine Liste von ER-Konfigurationen, die in der Dynamics 365 for Operations-Lösung bereitgestellt werden.
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



<a name="see-also"></a>Siehe auch
--------

[Lokalisierungsanforderungen – Erstellen einer elektronischen Berichtskonfiguration](electronic-reporting-configuration.md)

[Verwalten des Lebenszyklus der elektronischen Berichterstellung](general-electronic-reporting-manage-configuration-lifecycle.md)




