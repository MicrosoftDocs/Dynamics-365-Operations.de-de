---
title: Änderungen an Verwaltung für technische Änderung verwalten
description: In diesem Thema finden Sie Informationen zur Verwaltung für technische Änderung. Die Verwaltung für technische Änderung bietet strukturierte Prozesse für die Verwaltung von Änderungen an technischen Produkten, vom Vorschlagen, Anfordern und Durchführen von Änderungen bis hin zum Überprüfen und Genehmigen von Änderungen, dem Beurteilen ihrer Auswirkungen auf bestehende Vorgänge und dem Nachverfolgen der Änderungen.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8ae97d0e6aac1b0961427bd73a37612020231a9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983799"
---
# <a name="manage-changes-to-engineering-products"></a>Änderungen an Verwaltung für technische Änderung verwalten

[!include [banner](../includes/banner.md)]

Die Verwaltung für technische Änderung bietet strukturierte Prozesse für die Verwaltung von Änderungen an technischen Produkten. Sie können den Prozess *Änderungsantrag* verwenden, um Änderungen vorzuschlagen und anzufordern, und dann den Prozess *Änderungsauftrag* verwenden, um diese Änderungen tatsächlich durchzuführen. Benutzer können Änderungsanträge oder Änderungsaufträge erstellen, und es gibt dann einen Prozess zur Überprüfung und Genehmigung, zur Bewertung der Auswirkungen auf bestehende Transaktionen und zum Nachverfolgen der Änderungen.

## <a name="engineering-change-requests"></a>Technische Änderungsanforderungen

Mit dem Prozess für technische Änderungsanfragen können Sie Änderungsanfragen von allen relevanten Abteilungen in Ihrem Unternehmen erfassen. Dabei spielt es keine Rolle, ob Sie als Ingenieur arbeiten oder in der Fertigungs-, Beschaffungs-, Lagerort- oder Vertriebsabteilung: Jeder kann einen Änderungsantrag verwenden, um eine Änderung zu beantragen. Diese Änderung kann eine Idee für ein neues Produkt sein, ein Problem, das Sie bei der Arbeit mit einem bestehenden Produkt entdeckt haben, ein Vorschlag zur Verbesserung eines bestehenden Produkts oder etwas anderes.

Nachdem jemand einen Änderungsantrag gesendet hat, wird der *Überprüfungs- und Genehmigungsprozess* durch einen Workflow gesteuert, der festlegt, wer die Änderung genehmigen muss (z. B. der Besitzer des Produkts).

Um einen Workflow für Entwicklungsänderungsaufträge oder -anfragen festzulegen, gehen Sie zu **Verwaltung für technische Änderung \> Entwicklungs-Workflows**. Wählen Sie **Neu**, wählen Sie, ob der Workflow für die Überprüfung von Änderungsaufträgen oder Änderungsanfragen verwendet werden soll, und konfigurieren Sie dann den Workflow.

Weitere Informationen über Workflows finden Sie unter [Workflow-Systemübersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Weitere Informationen über Produktbesitzer finden Sie unter [Produktbesitzer](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Neue technische Änderungsanforderung erstellen

Um einen Änderungsantrag zu erstellen, führen Sie einen der folgenden Schritte aus.

- Gehen Sie zu **Verwaltung für technische Änderung \> Allgemein \> Änderungsverwaltung \> Änderungsanträge**, und wählen Sie dann **Neu** im Aktivitätsbereich.
- Öffnen Sie die Seite **Produktdetails** für ein bestehendes Engineering-Produkt. Wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Entwickler** in der Gruppe **Verwaltung für technische Änderung** die Option **Entwicklungsänderungsantrag \> Neuer Entwicklungsänderungsantrag**.

Ein neuer Änderungsauftrag wird erstellt. Sie können nun die Felder auf jedem Inforegister festlegen, wie in den folgenden Unterabschnitten beschrieben.

#### <a name="general-fasttab"></a>Allgemeines Inforegister

Auf der Inforegisterkarte **Allgemein** können Sie eine grundlegende Beschreibung der Änderungsanforderung angeben. Die folgende Tabelle beschreibt die Felder auf dieser Registerkarte.

| Feld | Beschreibung |
|---|---|
| Änderungsanforderung | Geben Sie einen Namen für die Änderungsanforderung ein. |
| Titel | Geben Sie einen Text ein, der die Änderungen in der Anfrage kurz beschreibt oder identifiziert. |
| Priorität | Wählen Sie einen Wert, um anzugeben, wie hoch die Priorität der Änderung ist. Sie können die verfügbaren Werte nach Bedarf für Ihr Unternehmen anpassen. (Weitere Informationen finden Sie unter [Einrichten allgemeiner Werte für die Verwaltung für technische Änderung](engineering-change-management-setup.md).) |
| Kategorie | Wählen Sie einen Wert, um die Art der Änderung zu beschreiben, die Sie beantragen. Sie können die verfügbaren Werte nach Bedarf für Ihr Unternehmen anpassen. (Weitere Informationen finden Sie unter [Einrichten allgemeiner Werte für die Verwaltung für technische Änderung](engineering-change-management-setup.md).) |
| Wichtigkeit | Wählen Sie einen Wert, um den Schweregrad des Problems anzugeben, das durch die Implementierung der Anforderung behoben werden soll. Sie können die verfügbaren Werte nach Bedarf für Ihr Unternehmen anpassen. (Weitere Informationen finden Sie unter [Einrichten allgemeiner Werte für die Verwaltung für technische Änderung](engineering-change-management-setup.md).) |
| Angefordert von | Der Name des Benutzers, der die Anfrage erstellt hat. |
| Bei | Das Datum, an dem die Anfrage erstellt wurde. |
| Status | Der Status der Anfrage. Wenn eine Anfrage zum ersten Mal erstellt wird, ist der Status *Erstellt*. Wenn die Anfrage genehmigt wird, ändert sich der Status auf *Genehmigt*. Wenn ein zugehöriger Änderungsauftrag für die Anfrage erstellt wurde, ändert sich der Status auf *Nachverfolgt*. |
| Änderungsauftrag | Die Änderungsauftragsnummer, wenn die Änderungsanforderung über einen Änderungsauftrag nachverfolgt wurde. |

#### <a name="information-fasttab"></a>Inforegister Informationen

Das Inforegister **Information** ermöglicht es Ihnen, weitere Informationen über die Anfrage hinzuzufügen.

Um dem Raster eine Zeile hinzuzufügen, wählen Sie **Neu** in der Symbolleiste über dem Raster und wählen dann eine der folgenden Optionen:

- **Datei** - Laden Sie eine Datei hoch.
- **Bild** - Laden Sie eine Bilddatei hoch.
- **Notiz** - Geben Sie eine Notiz direkt in das Raster ein.
- **URL** - Geben Sie eine URL direkt in das Raster ein.

Die folgende Tabelle beschreibt die Felder in jeder Zeile.

| Feld | Beschreibung |
|---|---|
| Datum und Uhrzeit der Erstellung | Das Datum und die Uhrzeit, zu der die Zeile erstellt wurde. |
| Typ | Die Art der Information, für die die Zeile erstellt wurde (Datei, Bild, Notiz oder URL). |
| Beschreibung | Geben Sie eine Beschreibung für die Zeile ein. |
| Einschränkung | Ein Wert, der angibt, ob die hinzugefügte Information aus einer internen oder externen Quelle stammt. |
| Zugeordnet | Ein markiertes Kontrollkästchen zeigt an, dass die Zeile einen Anhang (Datei oder Bild) enthält. Um den Anhang herunterzuladen, wählen Sie die Zeile aus und wählen dann **Öffnen** in der Symbolleiste über dem Raster. |

#### <a name="products-fasttab"></a>Inforegister Produkte

Im Inforegister **Produkte** können Sie jedes Produkt auflisten, das von der Änderungsanfrage betroffen ist. Sie können die Schaltflächen in der Symbolleiste verwenden, um Produkte zum Raster hinzuzufügen oder um Produkte zu entfernen.

Diese Liste dient nur zu Informationszwecken. Daher können Sie so viele verwandte Produkte hinzufügen, wie Sie für relevant halten. Wenn Sie eine Änderungsanfrage von der Seite **Produktdetails** für ein bestehendes Produkt erstellen, sollte dieses Produkt auf der Inforegister-Seite **Produkte** aufgeführt werden, nachdem Sie den Anfragedatensatz gespeichert haben.

#### <a name="source-fasttab"></a>Inforegister Quelle

Mit dem **Inforegister Quelle** können Sie den Startpunkt der Änderungsanforderung verfolgen. Es ist nützlich, wenn Sie z.B. sehen wollen, ob die Änderungsanforderung aus einem Verkaufsauftrag erstellt wurde, wer sie erstellt hat und in welcher Firma sie erstellt wurde.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Bewerten Sie die geschäftlichen Auswirkungen einer Änderungsanforderung

Wenn Sie eine Änderungsanforderung überprüfen, können Sie nach Abhängigkeiten suchen. Auf diese Weise können Sie die Auswirkungen der angeforderten Änderung auf offene Transaktionen, wie z. B. Verkaufsaufträge, Produktionsaufträge und den Bestand, beurteilen.

1. Gehen Sie zu **Verwaltung für technische Änderung \> Allgemein \> Verwaltung für technische Änderung \> Entwicklungsänderungsanträge**.
1. Öffnen Sie entweder eine bestehende Änderungsanforderung oder wählen Sie **Neu** im Aktivitätsbereich, um eine neue Änderungsanforderung zu erstellen.
1. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Änderungsanforderung** in der Gruppe **Geschäftliche Auswirkung** eine der folgenden Schaltflächen:

    - **Suchen** - Durchsucht alle offenen Transaktionen und öffnet dann die Dialogbox **Geschäftsauswirkungen auf offene Transaktionen**, die alle Transaktionen auflistet, die von der Änderung betroffen sind.
    - **Vorherige Suche anzeigen** - Öffnet das Dialogfeld **Auswirkungen auf offene Transaktionen**, in dem die Ergebnisse der vorherigen Suche aufgelistet sind. (Eine neue Suche wird nicht durchgeführt.)

1. Wenn das Problem, das eine Änderung erfordert, als kritisch eingestuft wird, können Sie die offenen Transaktionen sperren oder den verantwortlichen Benutzer benachrichtigen, indem Sie die Schaltflächen auf der Symbolleiste im Dialogfeld **Geschäftsauswirkungen auf offene Transaktionen** verwenden.

### <a name="create-a-change-order-from-a-change-request"></a>Erzeugen eines Änderungsauftrags aus einer Änderungsanforderung

Ein Ingenieur, der eine Änderungsanforderung prüft, kann einen Änderungsauftrag direkt von der Seite **Änderungsanforderungen** aus erstellen. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Änderungsanfrage** in der Gruppe **Änderungsauftrag** die Option **Verbindung und Produkte kopieren**.

## <a name="engineering-change-orders"></a>Technische Änderungsaufträge

Engineering-Änderungsaufträge bieten einen strukturierten Prozess für die Durchführung von Änderungen an Engineering-Produkten. Sie schlagen Änderungen vor, indem Sie eine Kopie der Engineering-relevanten Daten verwenden. Die eigentlichen Stammdaten sind davon nicht betroffen. Weitere Informationen über Engineering-relevante Daten finden Sie unter [Engineering-Versionen und Engineering-Produktkategorien](engineering-versions-product-category.md).

Sie können einen Änderungsauftrag erstellen, der auf einem genehmigten Änderungsantrag basiert. Ingenieure können auch Änderungsaufträge von Grund auf erstellen. Sie können mehrere Produkte in einen einzigen Änderungsauftrag aufnehmen, indem Sie einen der folgenden Schritte ausführen:

- Wählen Sie manuell Produkte aus.
- Verwenden Sie die Stückliste, um Produkte einzuschließen, die in der Produktstruktur niedriger sind (d.h. untergeordnete Elemente).
- Verwenden Sie eine Verwendungsnachweis-Suche, um Produkte einzuschließen, die in der Produktstruktur höher sind (d.h. übergeordnete Produkte).

Nachdem der Vorschlag für Änderungen abgeschlossen ist, wird der Überprüfungs- und Genehmigungsprozess durch einen Workflow abgewickelt. Sie können verschiedene Workflows festlegen, basierend auf Priorität und Schweregrad.

Um einen Workflow für Entwicklungsänderungsaufträge oder -anfragen festzulegen, gehen Sie zu **Verwaltung für technische Änderung \> Entwicklungs-Workflows**. Wählen Sie **Neu**, wählen Sie, ob der Workflow für die Überprüfung von Änderungsaufträgen oder Änderungsanfragen verwendet werden soll, und konfigurieren Sie dann den Workflow.

Weitere Informationen über Workflows finden Sie unter [Workflow-Systemübersicht](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Hier sind einige typische Beteiligte, die einen Änderungsauftrag genehmigen müssen:

- **Produktbesitzer** - Weitere Informationen über Produktbesitzer finden Sie unter [Produktbesitzer](product-owner.md).
- **Verantwortlicher Teamleiter** - Das Feld **Ingenieur** in der Ansicht **Kopf** des Änderungsauftrags zeigt den Ingenieur an, der den Änderungsauftrag erstellt hat. Wenn der Ingenieur zu einem Team gehört, das im System definiert ist, zeigt das Feld **Verantwortlicher** den Leiter dieses Teams an.
- **Finanzabteilung** - Die Finance-Abteilung muss eventuell Fälle prüfen, in denen die Änderung mit hohen Kosten verbunden ist.

Sie können wählen, ob der Änderungsauftrag direkt nach der Genehmigung als Teil des Workflows bearbeitet werden soll, oder ob die Bearbeitung später als manueller Schritt erfolgen soll. Während der Bearbeitung eines Änderungsauftrags werden die technischen Daten des eigentlichen Produkts aktualisiert.

Während Sie einen Änderungsantrag prüfen, wählen Sie im Aktivitätsbereich auf der Registerkarte **Änderungsantrag** in der Gruppe **Auswirkungen auf den Geschäftsbetrieb** die Option **Suchen**, um die Auswirkungen der vorgeschlagenen Änderung auf offene Transaktionen wie Verkaufsaufträge, Produktionsaufträge und den Bestand zu beurteilen. Die Ergebnisse werden im Dialogfeld **Auswirkungen auf offene Transaktionen** angezeigt, in dem Sie betroffene Transaktionen auswählen und dann Befehle in der Symbolleiste verwenden können, um weitere Informationen anzuzeigen, den zuständigen Benutzer zu benachrichtigen oder die Transaktion zu sperren.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Änderungsaufträge in Ingenieurbüros oder Betriebsgesellschaften

Wie in [Ingenieurunternehmen und Dateneigentumsregeln](engineering-org-data-ownership-rules.md) beschrieben, variieren die Produktdaten, die Sie bearbeiten können, je nach Art der juristischen Entität, in der Sie arbeiten (ein Ingenieurunternehmen oder ein operatives Unternehmen). Die Dateneigentumsregeln werden auch auf Änderungsaufträge angewendet. Abhängig von der juristischen Entität, in der Sie einen Änderungsauftrag erstellen, können daher unterschiedliche Arten von Änderungen vorgenommen werden. Im Folgenden finden Sie einige Beispiele hierfür:

- Bei Änderungsaufträgen in einer **Ingenieurgesellschaft** können Sie grundlegende Änderungen an den Engineering-Daten vornehmen. Sie können z. B. neue Versionen eines Produkts erstellen, die Struktur eines Produkts über die Stückliste ändern und Engineering-Attributwerte ändern. Wählen Sie für jedes betroffene Produkt einen der folgenden Werte im Feld **Auswirkung**:

    - **Keine** - Aktualisieren Sie die vorhandene Produktversion (In-Versions-Update).
    - **Neue Version** - Erzeugt eine neue Version, die auf der ausgewählten Produktversion basiert.
    - **Neues Produkt** - Ein komplett neues Produkt oder eine Produktvariante erstellen, die auf der gewählten Produktversion basiert.

- Bei Änderungsaufträgen in einer **Betriebsgesellschaft** können Sie die logistischen Daten des Produkts ändern. Sie können z.B. die bestehende Stückliste mit Einstellungen für die Bezugsquellenfindung anreichern, lokale Arbeitspläne oder lokale Stücklisten hinzufügen und sogar eine Stückliste anreichern, indem Sie neue Stücklistenzeilen für lokale Verpackungsmaterialien, Schmiermittel oder Anweisungen in der Landessprache hinzufügen. Anreicherungen, die Benutzer in der operativen Firma vornehmen, bleiben erhalten, wenn neue Updates von der technischen Firma gesendet werden. Weitere Informationen finden Sie unter [Engineering-Unternehmen und Dateneigentumsregeln](engineering-org-data-ownership-rules.md).

    Wenn Änderungsaufträge in der Engineering-Firma bearbeitet werden, werden die Produkte nur in der Engineering-Firma erstellt und/oder aktualisiert. Wenn also auch die Produktstammdaten aktualisiert werden sollen, müssen Sie die Produkte auch für Betriebsgesellschaften freigeben.

- Sie können Produkte direkt aus Änderungsaufträgen für das Engineering freigeben. Öffnen Sie den Änderungsauftrag, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Änderungsauftrag** in der Gruppe **Produktfreigaben** die Option **Produktstruktur freigeben**. Der Vorgang funktioniert genauso, wie wenn Sie Produkte von der Seite **Freigegebene Produkte** aus freigeben. Weitere Informationen finden Sie unter [Produktstrukturen freigeben](release-product-structure.md).
- Sie können Produkte aus Änderungsaufträgen automatisch freigeben lassen, basierend auf den folgenden Faktoren:

    - Wiederfreigaben an Firmen, in denen Produkte zuvor freigegeben wurden. Wählen Sie **Suchen**, um alle früheren Freigaben zu durchsuchen, und wählen Sie dann **Anzeigen**, um die Ergebnisse anzuzeigen. Die Seite **Ansicht** zeigt die früheren Produktfreigaben an, und Sie können auswählen, welche Produkte Sie neu freigeben möchten. Schließen Sie dann die Seite **Ansicht** und wählen Sie **Bearbeiten**, um die ausgewählten Produkte neu freizugeben.
    - Automatische Freigabeeinstellungen in der Freigabesteuerung der Engineering-Produktkategorie. Sie können diese Freigabe als Teil des Workflows durchführen. Wenn der Block **Freigabevorschlag sammeln** verwendet wird, wird der Freigabevorschlag mit Wiederfreigabevorschlägen gefüllt (siehe vorheriges Element der Liste), und die Produkte werden an Firmen freigegeben, wenn das Kontrollkästchen **Automatische Freigabe** in der Freigabesteuerung der Engineering-Produktkategorie aktiviert ist. Sie können **Anzeigen** wählen, um die Ergebnisse zu sehen, wie im vorherigen Listenelement beschrieben. Die Produkte werden auch freigegeben, wenn der Block **Freigabevorschlag verarbeiten** verwendet wird. Wenn Sie sich dafür entscheiden, nur den Freigabevorschlag als Teil des Workflows zu sammeln, können Sie die Freigabe manuell starten, indem Sie **Vorgang** wählen, wie im vorherigen Listenelement beschrieben.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Nachverfolgen eines Änderungsantrags über einen Änderungsauftrag

Sobald ein Änderungsantrag genehmigt ist, können Sie ihn über einen Änderungsauftrag nachverfolgen. Sie können mehrere Änderungsanträge in einem einzigen Änderungsauftrag zusammenfassen. Ein einzelner Änderungsauftrag kann sogar mehrere Produkte umfassen. (Normalerweise verwenden Sie diesen Ansatz, wenn dieselbe Änderung auf mehrere Produkte angewendet werden muss). Sie können jedoch nicht mehrere Änderungsaufträge aus einer einzigen Änderungsanforderung erstellen.

Um eine Änderungsanforderung über einen Änderungsauftrag nachzuverfolgen, öffnen Sie die Änderungsanforderung und wählen dann im Aktivitätsbereich auf der Registerkarte **Änderungsauftrag** in der Gruppe **Änderungsauftrag** die Option **Verbindung und Produkte kopieren**. Sie können dann einen bestehenden Änderungsauftrag auswählen, um die Änderungsanforderung damit zu verbinden, oder Sie können einen neuen Änderungsauftrag für diese spezielle Anforderung erstellen.

## <a name="engineering-change-order-report"></a>Bericht zum technischen Änderungsauftrag

Änderungsauftragsberichte beschreiben die Änderungen, die in einem Änderungsauftrag vorgenommen wurden. Sie sind sowohl während als auch nach dem Überprüfungs- und Genehmigungsprozess nützlich.

Um einen Änderungsauftragsbericht anzuzeigen, öffnen Sie den entsprechenden Änderungsauftrag und wählen dann im Aktivitätsbereich auf der Registerkarte **Änderungsauftrag** in der Gruppe **Ansicht** die Option **Änderungsauftragsbericht**.

## <a name="fields-on-an-engineering-change-order"></a>Felder in einem Änderungsauftrag

Die meisten Felder auf Änderungsaufträgen sind die gleichen wie die Felder für freigegebene Produkte, Engineering-Versionen, Dokumente, Stücklisten (Zeilen) und Arbeitspläne (Vorgänge). Die Felder in der folgenden Tabelle sind jedoch nur für Änderungsaufträge vorgesehen.

| Feld | Beschreibung |
|---|---|
| Gründe für technische Änderung | Wählen Sie den Grund für die Änderung des betroffenen Produkts. |
| Änderungsbeschreibung | Geben Sie eine Beschreibung der Änderung ein. |
| Erforderliche Spezialwerkzeuge | Geben Sie an, ob ein spezielles Tool erforderlich ist, um die Änderung anzuwenden. |
| Technische Materialdisposition | Wählen Sie einen Materialdispositionscode für Abfälle, die bei der Anwendung der Änderung anfallen. |
| Debitorengenehmigung erforderlich | Geben Sie an, ob eine Kundengenehmigung erforderlich ist, bevor die Änderung angewendet werden kann. |
| Empfangene Debitorengenehmigung | Geben Sie den Status der Kundengenehmigung an. |
| Umwelt- und Arbeitsschutz | Geben Sie an, ob Umwelt- und Sicherheitsvorschriften auf die Änderung anwendbar sind. Wenn dies der Fall ist, können Sie die anwendbaren Regeln auswählen. |

Mit der Schaltfläche **Änderungsinformationen beibehalten/kopieren** können Sie Änderungsinformationen zwischen betroffenen Produkten kopieren.
