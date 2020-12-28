---
title: Mobile Rechnungsgenehmigungen
description: Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443528"
---
# <a name="mobile-invoice-approvals"></a>Mobile Rechnungsgenehmigungen

[!include [banner](../includes/banner.md)]

Mithilfe der mobilen Funktionen können Geschäftsbenutzer mobile Erfahrungen entwerfen. Bei erweiterten Szenarien ermöglicht die Plattform auch Entwickler die Funktionen zu erweitern. Die effektivste Möglichkeit, einige der neuen mobilen Konzepten kennenzulernen, ist, den Prozess des Entwurfs einiger Szenarios durchzulaufen. Dieses Thema soll einen praktischen Ansatz zum Entwerfen von mobilen Szenarien bereitstellen, indem es mobile Kreditorenrechnungsgenehmigungen als Anwendungsfall zeigt. Dieses Thema soll helfen, andere der Szenarien zu entwerfen und kann auch auf anderen Szenarios angewendet werden, die nicht den Kreditorenrechnungen zugeordnet werden.

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                                                            | Beschreibung                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vorbereitung                                                                                |[Mobile Plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | Eine Umgebung mit Version 1611 und Plattform-Update 3 (November 2016)                   |
| Hotfix KB 3204341 installieren.                                                                              | Die Aufgabenaufzeichnung kann fälschlicherweise zwei Scließen-Befehle für Dropdowndialogfelder erfassen, die in Plattform-Update 3 (November 2016) einbezogen sind |
| Hotfix KB 3207800 installieren.                                                                              | Dieser Hotfix ermöglicht das Anzeigen von Anhängen im mobilen Client, der in Plattform-Update 3 (November 2016) enthalten ist.           |
| Hotfix KB 3208224 installieren.                                                                              | Anwendungscode für die mobile Kreditorenrechnungs-Genehmigungsanwendung ist in der Version 7.0.1 (Mai 2016) enthalten.                          |
| Ein Android- oder iOS- oder Windows-Gerät, auf dem die mobile App installiert wurde. | Suchen Sie die App im entsprechenden App-Store.                                                                                                                     |

## <a name="introduction"></a>Einführung
Mobile Genehmigungen für Kreditorenrechnungen erfordern die drei Hotfixes, die im Abschnitt "Vorbereitung" angegeben werden. Diese Hotfixes bieten keinen Arbeitsbereich für die Rechnungsgenehmigungen. Um zu lernen, was ein Arbeitsbereich im Rahmen des mobilen Clients ist, lesen Sie das Handbuch aus dem Abschnitt "Vorbereitung". Der Rechnungsgenehmigungsarbeitsbereich muss konzipiert werden. 

Jede Organisation definiert und nutzt eigene Geschäftsprozesse für Kreditorenrechnungen. Bevor Sie eine mobile Erfahrung für Kreditorenrechnungsgenehmigungen entwerfen, müssen Sie die folgenden Aspekte des Geschäftsprozesses berücksichtigen. Der Grundgedanke ist, diese Datenpunkten so weit wie möglich zu verwenden, um die Benutzerfreundlichkeit für das Gerät zu optimieren.

-   Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?
-   Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?
-   Wie viele Rechnungspositionen gibt es in einer Rechnung? Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.
-   Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen? Wenn die Antwort zu dieser Frage ja ist, beachten Sie die folgenden Fragen:
    -   Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, Teilungen, usw.) gibt es für eine Rechnungsposition? Wieder gilt die Regel 80-20.
    -   Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf? Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?

    > [!NOTE]
    > In diesem Thema wird nicht erläutert, wie Sie Buchhaltungsverteilungen bearbeitet, da diese Funktion nicht aktuell für mobile Szenarios unterstützt werden.

-   Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?

Das Design der mobilen Erfahrung für Rechnungsgenehmigungen variiert, abhängig von den Antworten auf diese Fragen. Die Zielsetzung ist, die Benutzerfreundlichkeit für den Geschäftsprozess auf Mobilgeräten in einer Organisation zu optimieren. Im Rest des Themas betrachten wir zwei Szenariovarianten die auf Grundlage unterschiedlicher Antworten auf Fragen vorhergehenden sind. 

Allgemeine, wenn mit dem mobilen Designer gearbeitet wird, vergewissern Sie sich, diese Änderungen veröffentlicht werden, um zu verhindern Aktualisierungen zu verlieren.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Entwerfen eines einfachen Rechnungsgenehmigungsszenarios für Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenarioattribut</th>
<th>Antwort</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</td>
<td><ol>
<li>Kreditorenname</li>
<li>Rechnungssumme</li>
<li>Rechnungskonto</li>
<li>Rechnungsnummer</li>
<li>Rechnungsdatum</li>
<li>Rechnungsbeschreibung</li>
<li>Fälligkeitsdatum</li>
<li>Rechnungswährung</li>
</ol></td>
</tr>
<tr class="even">
<td>Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</td>
<td><ol>
<li>Beschaffungskategorie</li>
<li>Leistung</li>
<li>Preis je Einheit</li>
<li>Nettobetrag der Position</li>
<li>Steuerbetrag (US 1099)</li>
</ol></td>
</tr>
<tr class="odd">
<td>Wie viele Rechnungspositionen gibt es in einer Rechnung? Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition? Wieder gilt die Regel 80-20.</td>
<td>Erweiterter Preis: 2 Mehrwertsteuer: 0 Zuschläge: 0</td>
</tr>
<tr class="even">
<td>Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf? Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</td>
<td>Nicht verwendet</td>
</tr>
<tr class="odd">
<td>Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Arbeitsbereich erstellen

1.  In einem Browser und melden Sie sich in der Anwendung an.
2.  Nachdem Sie angemeldet sind, hängen Sie **&mode=mobile** an die URL wie im folgenden Beispiel an und aktualisieren die Seite: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**. Der Designer für mobile Apps wird wie die Aufgabenaufzeichnung angezeigt.
4.  Klicken Sie auf **Hinzufügen** um einen neuen Arbeitsbereich zu erstellen Im vorliegenden Beispiel ist Name des Arbeitsbereichs **Meine Genehmigungen**.
5.  Geben Sie eine Beschreibung ein.
6.  Arbeitsbereichsfarbe auswählen. Die Arbeitsbereichfarbe wird für den Gesamtstil der mobilen Erfahrung für den Arbeitsbereich verwendet.
7.  Wählen Sie ein Symbol für den Arbeitsbereich aus.
8.  Klicken Sie auf **Fertig.**
9.  Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Änderungen zu speichern.

### <a name="vendor-invoices-assigned-to-me"></a>Mir zugewiesene Kreditorenrechnungen

Die erste mobile Seite soll die Liste der Rechnungen, die dem Benutzer zur Genehmigung zugewiesen werden zeigen. Um diese mobile Seite zu entwerfen verwenden Sie die **VendMobileInvoiceAssignedToMeListPage**-Seite. Bevor Sie dieses Verfahren ausführen, stellen Sie sicher, dass mindestens eine Kreditorenrechnung zur Prüfung Ihnen zugewiesen ist und die Rechnungsposition zwei Verteilungen hat. Diese Einstellung erfüllt die Bedingungen für dieses Szenarios.

1.  In der URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceAssignedToMeListPage**, um die mobile Version der Listenseite **Ausstehende Kreditorenrechnungen – mir zugewiesen** im **Kreditor**-Modul zu öffnen. Je nach der Anzahl von Rechnungen, die Sie in Ihrem System besitzen, das Ihnen zugeordnet ist, wird auf dieser Seite die Rechnungen angezeigt. Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen. Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel. Es benötigen nur eine Rechnung, die Ihnen zugewiesen ist. Die neuen Seiten, die verfügbar sind, wurden insbesondere zum Entwickeln von mobilen Szenarien für Kreditorenrechnung entworfen. Daher müssen Sie diesen Seiten nutzen. Die URL muss der folgenden URL ähneln. Nachdem Sie sie eingeben haben, muss die Seite, die in der Abbildung dargestellt wird, angezeigt werden: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![Seite „Ausstehende Kreditorenrechnungen – mir zugewiesen“](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.
3.  Wählen Sie einen und Arbeitsbereich aus und klicken sie **Bearbeiten**
4.  Klicken Sie auf **Seite hinzufügen**, um die ersten mobilen Seite zu erstellen.
5.  Geben Sie einen Namen ein, z.B. meine **Meine Kreditorrechungen** und eine Beschreibung ein, z.B. **Mir zur Genehmigung zugeweisene Kreditorenrechnungen**.
6.  Klicken Sie auf **Fertig**.
7.  Im mobilen Designer auf der Registerkarte **Felder** klicken Sie auf **Felder wählen**. Die Spalten auf der Listenseite müssen der folgenden Abbildung ähneln. 

    [![Spalten auf der Seite "Mir zugeweisene ausstehenden Kreditorenrechnungen"](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  Fügen Sie die erforderlichen Spalten von der Listenseite hinzu, die für Benutzern in der mobilen Seite angezeigt werden. Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden. Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen. Basierend auf den Anforderungen für dieses Szenarios, sind die folgenden acht Felder obligatorisch. Allerdings erachten mehrere Benutzer acht Felder für zu viele Informationen, die auf einem mobilen Gerät zu haben. Daher werden nur die wichtigsten Felder in der mobilen Listenansicht angezeigt. Die übrigen Felder erscheinen in der Detailansicht, die Sie später entwerfen. Jetzt fügen Sie nur die folgenden Felder hinzu. Klicken Sie auf das Pluszeichen (**+**) in den Spalten die Sie zum mobilen Seite hinzuzufügen wollen.
    - Kreditorenname
    - Rechnungssumme
    - Rechnungskonto
    - Rechnungsnummer
    - Rechnungsdatum

    Nachdem die Felder hinzugefügt sind, muss die mobile Seite der folgenden Abbildung ähneln. 
    
    [![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  Sie müssen außerdem die folgenden Spalten hinzufügen, sodass wir Workflowaktivitäten später aktivieren können.
    - Abgeschlossene Aufgabe anzeigen
    - Delegataufgabe anzeigen
    - Zurückrufene Aufgabe anzeigen
    - Abgelehnte Aufgabe anzeigen
    - Abschlussanforderung Aufgabe anzeigen
    - Aufgabe erneut übermitteln anzeigen

10. Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.
11. Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden
12. Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.
13. Aktivieren Sie **Rechnungssumme in Kreditorenrechnungsliste anzeigen** im Formular Kreditorparameter unter **Rechnung**. Beachten Sie, dass, nur, indem Sie diesen Parameter aktiviert, Rechnungssummen berechnet werden, der auf Kreditorenrechnungslistenseite ausstehenden angezeigt werden. Dies ist eine neue Funktion als Teil des erforderlichen Hotfixes 3208224.

### <a name="vendor-invoice-details"></a>Details der Kreditorenrechnung

Um die Rechnungsdetailseite für die mobile App zu entwerfen, verwenden Sie die **VendMobileInvoiceHeaderDetails**-Seite. Beachten Sie diese, abhängig von der Anzahl der Rechnungen, die Sie in Ihrem System gibt, enthält dieser Seite die älteste Rechnung (die Rechnung, die zuerst erstellt wurde). Sie können den Filter links verwenden um eine bestimmte Rechnung zu suchen. Allerdings benötigen wir keine bestimmte Rechnung für dieses Beispiel. Es müssen nur einige Rechnungsinformationen, sodass wir die mobile Seite zu entwerfen. 

[![Workflowseite](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. In der URL ersetzen Sie den Namen der Menüoption durch **VendMobileInvoiceHeaderDetails**, um das Formular zu öffnen

2. Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.

3. Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.

4. Wählen Sie die Seite **Meine Kreditorenrechnungen** aus, die Sie zuvor erstellt haben, und klicken Sie dann auf **Bearbeiten**.

5. Auf der **Felder** Registerkarte klicken Sie auf die Spaltenüberschrift **Raster**

6. Klicken Sie auf **Eigenschaften &gt; Seite hinzufügen**. **Hinweis:** Wenn Sie auf das **Raster** Überschrift klicken und eine Seite hinzufügen, wird die Beziehung zur Detailseite automatisch bestimmt.

7. Geben Sie einen Seitentitel, z.B. **Rechnungsdetails** und einer Beschreibung, wie ein **Ansichtsrechnungskopf und Positionsdetails**.

8. Klicken Sie auf **Felder auswählen**. Die Reihenfolge, in der Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden. Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen. 

9. Fügen Sie die folgenden Felder aus dem Auftragskopf, basierend auf den Anforderungen für dieses Szenarios hinzu:
   - Kreditorenname
   - Rechnungssumme
   - Rechnungskonto
   - Rechnungsnummer
   - Rechnungsdatum
   - Rechnungsbeschreibung
   - Fälligkeitsdatum
   - Rechnungswährung

10. Fügen Sie die folgenden Felder aus Positionsraster auf der Seite hinzu:
    - Beschaffungskategorie
    - Leistung
    - Preis je Einheit
    - Nettobetrag der Position
    - Steuerbetrag (US 1099)

11. Nachdem alle Felder aus den früheren zwei Schritten hinzugefügt wurden, klicken Sie auf **Fertig**. Die müssen der folgenden Abbildung ähneln.
    
    [![Seite nach Felder hinzugefügt](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.

13. Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden

14. Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.

### <a name="workflow-actions"></a>Workflowaktivitäten

Um Workflow-Aktionen hinzuzufügen, verwenden Sie die Seite **VendMobileInvoiceHeaderDetails**. Um diese Seite zu öffnen, ersetzen Sie Name der Menüoption in die URL, wie Sie eben geschehen ist. Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche. Gehen Sie folgendermaßen vor, um die Detailseite auf Workflowaktivitäten hinzuzufügen. Sie müssen Rechnungen haben, die Ihnen zugewiesen wurden, die sich in einem angemessenen Status befinden, damit Ihnen die Workflowaktivitäten zur Verfügung stehen, für die Sie entwerfen möchten.

#### <a name="record-workflow-actions"></a>Workflowaktivitäten erfassen
1.  Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.
2.  Wählen Sie die **Rechnungsdetails** Seite, die Sie eben erstellt haben, und klicken Sie dann **Bearbeiten**.
3.  Klicken Sie auf der Registerkarte **Aktionen** auf **Aktion hinzufügen**.
4.  Geben Sie einen Aktivitätstitel, z. B. **Genehmigen** und eine Beschreibung ein, z.B. **Rechnung genehmigen**. Beachten Sie, dass der Aktivitätstitel, den Sie hier eingeben, der Name der Aktivität ist, den Benutzer in der Zeit-App mobilen die angezeigt wird.
5.  Klicken Sie auf **Fertig**.
6.  Klicken Sie auf **Felder auswählen**.
7.  Führen des Workflowprozesses auf der **VendMobileInvoiceHeaderDetails** Seite durch, und schließen Sie die Aktivität aus, die Sie erfassen. Ihren Planungen zufolge Überprüfen Sie, ob Sie Workflowkommentare während dieses Vorgangs ein eingegeben werden, damit auch im Kommentarfeld mobilen Erfahrung enthalten ist.
8.  Nachdem die Workflowaktivität ausgeführt ist, klicken Sie auf **Fertig**, um die Felder auswählen-Aufgabe abzuschließen.
9.  Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.
10. Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden
11. Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.
12. Wiederholen Sie die vorherigen Schritte, um alle erforderlichen Workflowaktivitäten zu erfassen. 

#### <a name="create-a-js-file"></a>Erstellen Sie eine JS-Datei.
1. Öffnen Sie den Editor oder Microsoft Visual Studio, und fügen Sie den folgenden Code ein. Speichern Sie die Datei als .js-Datei. Diese Code bewirkt Folgendes:
    - Er blendet die zusätzlichen workflowbezogenen Spalten aus, die wir früher mobilen auf der Listenseite hinzugefügt. Es werden diesen Spalten hinzufügen, sodass der Zeit-App dass Informationen im Zusammenhang hat und die nächsten Schritt ausführen kann.
    - Anhand des Workflowschritt, die aktiv ist, wendet sie Logik, um nur die Vorgänge anzeigen.

    > [!NOTE]
    > Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte auswählen
3.  Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.
4.  Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden
5.  Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.

### <a name="vendor-invoice-attachments"></a>Kreditorenrechungsanhänge

1. Klicken Sie auf **Einstellungen** (Zahnrad) in der oberen rechten Ecke der Seite und klicken dann auf **Mobile App**.

2. Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.

3. Wählen Sie die Seite <strong>Rechnungsdetails **aus, die Sie zuvor erstellt haben, und klicken Sie dann auf** Bearbeiten</strong>.

4. Legen Sie die **Dokumentverwaltung** Option **Ja** wie weiter unten fest. **Hinweis:** Wenn keine Anforderungen gibt, Zuordnungen im mobilen Gerät angezeigt werden, können Sie diese Option **Nein**, mit der die Standardeinstellung ist.
   
   ![Dokumentverwaltung](./media/docmanagement-216x300.png)

5. Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.

6. Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden

7. Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.

### <a name="vendor-invoice-line-distributions"></a>Kreditorrechungspositionsverteilungen

Die Anforderungen für dieses Szenarios bestätigen, dass nur Verteilungen auf Positionsebene sind und dass eine Rechnung immer nur eine Position ist. Da dieses Szenario ist einfach, muss die Benutzerfreundlichkeit auf dem auch einfach mobilen Gerät genug sein, dem der Benutzer nicht mehrere Ebenen muss Detailinformationen anzeigen, damit die Verteilungen anzuzeigen. Kreditorenrechnungen enthalten die Option des Anzeigens aller Verteilungen aus dem Rechnungskopf. Diese Umgebung ist was wir für das mobile Szenario benötigen. Daher verwenden Sie die **VendMobileInvoiceAllDistributionTree** Seite, um diesen Teil des mobilen Szenarios zu entwerfen. 

> [!NOTE] 
> Das Kennen der Anforderungen können uns, entscheiden, die die betreffende genau zu verwenden Seite, und wie die mobile Erfahrung des Benutzers optimiert, wenn Sie das Szenario entwerfen. Im zweiten Szenario können wir eine andere Seite, damit die Verteilungen anzuzeigen, weil die Anforderungen für dieses Szenarios unterscheiden.

1.  In der URL ersetzten Sie den Name der Menüoption. Die Seite, die angezeigt wird, sollte der folgenden Abbildung ähneln.

    [![Alle Verteilungen-Seite](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  Öffnen Sie den Designer von mobilen **Einstellungen** (Zahnrad) Schaltfläche.

3.  Klicken Sie auf die **Bearbeiten** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten. **Hinweis:** Sie sehen, dass zwei neue Seiten automatisch erstellt wurden. Das System diese Seiten erstellt, da Sie die Dokumentverwaltung im vorherigen Abschnitt einschalteten. Sie können diese Seiten neuen ignorieren.

4.  Klicken Sie auf **Seite hinzufügen.**

5.  Geben Sie einen Seitentitel, wie **Ansichtsbuchhaltung** und eine Beschreibung ein, z.B. **Ansicht für die Rechnung** ein.

6.  Klicken Sie auf **Fertig**.

7.  Auf der Registerkarte **Felder** wählen Sie **Felder auswählen**, die folgenden Felder aus der Verteilungsseite aus und klicken dann **Fertig**.
    1.  Betrag
    2.  Währung
    3.  Sachkonto

    > [!NOTE] 
    > Es können die **Beschreibung** Spalte im Verteilungsraster aus, weil die Anforderungen für dieses Szenarios bestätigten, dass der erweiterte Preis der einzige Betrag ist, dass für Verteilungen gibt. Daher fordert der Benutzer kein anderes Feld, den Betragstyp festzustellen, ob die Verteilung für ist. Allerdings im folgenden Szenario verwenden, wir **werden** Sie diese Informationen, weil die Anforderungen für dieses Szenarios angeben, dass andere Betragsart Verteilungen haben (z, Mehrwertsteuer).

8.  Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.

9.  Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden

10. Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.

#### <a name="adding-navigation-to-view-accounting-page"></a>Hinzufügen der Navigation zur Seite „Buchhaltung anzeigen“.

Die mobile Seite **Buchhaltung anzeigen** ist derzeit mit keiner mobilen Seiten verknüpft, die wir bisher entworfen haben. Da der Benutzer in der Lage sein soll, die Seite **Buchhaltung anzeigen** aus der **Rechnungsdetails** Seite im mobilen Gerät zu navigieren, müssen Sie zuvor aus der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite bereitstellen. Wir legen die Navigationsverknüpfung ein, indem wir Zusatzlogik zu JavaScript verwenden.

1.  Öffnen Sie die JS-Datei, die Sie eben erstellt haben, und fügen Sie die Positionen hinzu, die im folgenden Code hervorgehoben werden. Dieser Code mach zwei Dinge:
    1.  Er wird sichergestellt, dass Benutzer nicht direkt über der Arbeitsbereich **Buchhaltung anzeigen** Seite Navigation können.
    2.  Er wird ein Navigationssteuerelement der **Rechnungsdetails** Seite der **Buchhaltung anzeigen** Seite ein.

    > [!NOTE] 
    > Die Namen der Seiten und andere Steuerelemente im Code müssen mit den Namen im Arbeitsbereich identisch sein.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die **Logik** Registerkarte zum Überschreiben des Codes auswählen
3.  Klicken Sie auf **Fertig**, um den Bearbeitungsmodus zu verlassen.
4.  Klicken Sie auf **Zurück** und **Fertig**, um den Arbeitsbereich zu beenden
5.  Klicken Sie auf **Arbeitsbereich veröffentlichen**, um die Arbeit zu speichern.

### <a name="validation"></a>Überprüfung

Öffnen Sie auf Ihrem mobilen Gerät die App, und stellen Sie eine Verbindung mit Ihrer Instanz her. Überprüfen Sie, ob Sie in das Unternehmen ein, in dem Kreditorenrechnungen Ihnen zur Prüfung zugewiesen werden. Sie sollten in der Lage sein, die folgenden Aktionen ausführen:

-   Siehe den **Meine Genehmigungen** Arbeitsbereich.
-   Öffnen Sie den **Meine Genehmigungen** Arbeitsbereich und sehen Sie die **Meine Kreditorenrechnungen** Seite.
-   Öffnen Sie die **Meine Kreditorenrechnungen** Seite und erscheinen die Liste der Rechnungen, die Ihnen zugewiesen sind.
-   Öffnen Sie eine der Rechnungen und die Rechnungskopfdetails finden und -Positionsdetails.
-   Auf der Detailseite finden Sie einen Link zu den Anlagen, und verwenden Sie diesen Link, die der Anhangliste zu navigieren und die Anhänge anzeigen.
-   Auf der Detailseite finden Sie einen Link zur Seite **Buchhaltung anzeigen** und verwenden Sie diesen Link, um zur Verteilungsseite zu navigieren.
-   Auf der Detailseite klicken Sie auf das Menü **Aktivitäten** unten, und lassen Workflowaktivitäten aus, die z Workflowschritt gültig sind.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Entwerfen eines komplexen Rechnungsgenehmigungsszenarios für Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Szenarioattribut</th>
<th>Antwort</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Welche Felder aus dem Rechnungskopf wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</td>
<td><ol>
<li>Kreditorenname</li>
<li>Rechnungsbetrag</li>
<li>Rechnungskonto</li>
<li>Rechnungsnummer</li>
<li>Rechnungsdatum</li>
<li>Rechnungsbeschreibung</li>
<li>Fälligkeitsdatum</li>
<li>Rechnungswährung</li>
</ol></td>
</tr>
<tr class="even">
<td>Welche Felder aus den Rechnungsposition wünschen die Benutzer in mobilen Umgebungen und in welcher Reihenfolge?</td>
<td><ol>
<li>Beschaffungskategorie</li>
<li>Leistung</li>
<li>Preis je Einheit</li>
<li>Nettobetrag der Position</li>
<li>Steuerbetrag (US 1099)</li>
</ol></td>
</tr>
<tr class="odd">
<td>Wie viele Rechnungspositionen gibt es in einer Rechnung? Wenden Sie die 80-20-Regel hier an, und optimieren Sie für 80 Prozent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Möchten Benutzer Buchhaltungsverteilungen (Rechnungscodierung) auf dem mobilen Gerät sehen?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, usw.) gibt es für eine Rechnungsposition? Wieder gilt die Regel 80-20.</td>
<td>Erweiterter Preis: 2 Mehrwertsteuer: 2 Zuschläge: 2</td>
</tr>
<tr class="even">
<td>Haben Rechnungen auch Buchhaltungsverteilungen im Rechnungskopf? Falls ja sollen diese Buchhaltungsverteilungen im Gerät verfügbar sein?</td>
<td>Nicht verwendet</td>
</tr>
<tr class="odd">
<td>Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Nächste Schritte

Die folgenden Abweichungen für Szenario 1, basierend auf den Anforderungen für Szenario 2. Sie können in diesem Bereich verwenden, um Ihre Erfahrung mit der mobilen App zu verbessern.

1.  Da weitere Rechnungspositionen in Szenario 2 erwartet werden, können folgende Änderungen zum Entwurf, die Benutzererfahrung im mobilen Gerät zu optimieren:
    1.  Anstelle der Betrachtungsrechnungspositionen auf Detailseite der (z.B. in Szenario 1), Benutzer festlegen, dass Positionen einer separaten mobilen Seite anzeigen.
    2.  Da mehrere Rechnungsposition in diesem Szenario erwartet wird, wenn die **VendMobileInvoiceAllDistributionTree** Seite verwendet wird, um die Verteilungsseite für Datenschutzerklärung zu entwerfen (wie in Szenario 1), kann es verwirrend, damit der Benutzer Positionen mit Verteilungen aufeinander umfasst. Daher verwenden Sie die **VendMobileInvoiceLineDistributionTree** Seite, um die Verteilungsseite zu entwerfen.
    3.  Im Idealfall sollten die Verteilungen im Kontext einer Rechnungsposition in diesem Szenario angezeigt werden. Daher müssen Sie unbedingt, ob der Benutzer in einer Position richten bohren kann, um die Verteilungsseite anzuzeigen. Verwenden Sie die Seitenlinkfunktion, den Drillthrough einzurichten, wie Sie für den Kopf und die Detailseiten in Szenario 1. ".

2.  Da mehrere ein Betragsart für die Verteilungen in Szenario 2 (Mehrwertsteuer, Belastungen usw.) erwartet wird, ist es hilfreich, die Beschreibung des Betrags Typ anzeigen. (Wir haben diese Informationen in Szenario 1 ausgelassen.)




