---
title: Mobile Rechnungsgenehmigungen
description: "Mobile Funktionen in Microsoft Dynamics 365 können Arbeitsgänge für einen geschäftlichen Benutzer mobile Erfahrungen entwerfen. Bei Szenarien erweiterte ermöglicht die Plattform auch Entwickler die Funktionen erweitern, während sie möchten. Die letzten effektive Möglichkeit, einige der neuen Konzepten auf Datenschutzerklärung zu ermitteln ist, den Prozess der Entwurf mehrere Szenarios. durchzulaufen Dieses Thema soll bewirken, dass Feld einen Ansatz zum Entwerfen von Szenarien mobilen bereitzustellen, indem Sie für Kreditorenrechnungsgenehmigungen Mobile als Anwendungsfall wird. Dieses Thema helfen soll, andere der Abweichungen Szenarien zu entwerfen und kann auch anderen Szenarios auch angewendet werden, die nicht in den Kreditorenrechnungen zugeordnet werden."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobile Rechnungsgenehmigungen

Mobile Funktionen in Microsoft Dynamics 365 können Arbeitsgänge für einen geschäftlichen Benutzer mobile Erfahrungen entwerfen. Bei Szenarien erweiterte ermöglicht die Plattform auch Entwickler die Funktionen erweitern, während sie möchten. Die letzten effektive Möglichkeit, einige der neuen Konzepten auf Datenschutzerklärung zu ermitteln ist, den Prozess der Entwurf mehrere Szenarios. durchzulaufen Dieses Thema soll bewirken, dass Feld einen Ansatz zum Entwerfen von Szenarien mobilen bereitzustellen, indem Sie für Kreditorenrechnungsgenehmigungen Mobile als Anwendungsfall wird. Dieses Thema helfen soll, andere der Abweichungen Szenarien zu entwerfen und kann auch anderen Szenarios auch angewendet werden, die nicht in den Kreditorenrechnungen zugeordnet werden.

<a name="prerequisites"></a>Voraussetzungen
-------------

| Voraussetzung                                                                                            | Beschreibung                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobiles Handbuch Doppellese                                                                                |(/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                  |
| Dynamics 365 für Arbeitsgänge                                                                             | Eine Umgebung, zur Microsoft Dynamics 365 für Arbeitsgangsversion 1611 und Microsoft Dynamics for Arbeitsgangsplattformaktualisierung 3 (November 2016)                   |
| Richten Sie Hotfix 3204341 KB.                                                                              | Aufgabenaufzeichnung kann zwei Sie Befehle für Dropdowndialogfelder irrtümlich erfassen, die dieses in Dynamics 365 für Arbeitsgangsplattformaktualisierung 3 einbezogen ist (Aktualisierung )November 2016 |
| Richten Sie Hotfix 3207800 KB.                                                                              | Dieser Hotfix aktiviert die im Feld Mobilclienten angezeigt werden Anlagen, für den dieses in Dynamics 365 für Arbeitsgangsplattformaktualisierung 3 einbezogen ist (November 2016 Aktualisierung ).           |
| Richten Sie Hotfix 3208224 KB.                                                                              | Anwendungscode für die Kreditorenrechnungsgenehmigungsbewerbung mobile Dies ist in Microsoft Dynamics AX-Anwendung 7.0.1 einbezogen (Mai 2016 ).                          |
| Android oder ein IOS oder ein Windows-Gerät, das die mobile Zeit-App hat, wurden für Dynamics 365 für Arbeitsgänge | Suchen der Zeit-App im entsprechenden App-Shop.                                                                                                                     |

## <a name="introduction"></a>Einführung
Mobile Genehmigungen für Kreditorenrechnungen erfordern die drei Hotfixes, die im Abschnitt "Voraussetzungs" angegeben werden. Diese Hotfixes bieten einen Arbeitsbereich nicht für die Rechnungsgenehmigungen bereit. Um zu ermitteln was ein Arbeitsbereich im Rahmen des Mobiles ist, lesen Sie das Handbuch mobile das im Abschnitt "Voraussetzungs" angegeben ist. Der Rechnungsgenehmigungsarbeitsbereich muss so konzipiert werden. 

Jede Organisation definiert instrumentiert und seinen Geschäftsprozess für Kreditorenrechnungen anstatt. Bevor eine mobile Erfahrung für Kreditorenrechnungsgenehmigungen entwerfen, müssen Sie die folgenden Aspekte des Geschäftsprozesses wider. Der Grundgedanke ist, dieser Datenpunkten so weit wie möglich zu verwenden, um die Benutzerfreundlichkeit für das Gerät zu optimieren.

-   Welche Felder aus dem Rechnungskopf wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?
-   Welche Felder aus den Rechnungspositionen wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?
-   Wie viele Rechnungspositionen gibt es? in einer Rechnung Wenden Sie die Regel 80-20 hier an, und führen Sie das für 80 Prozent.
-   Möchten Benutzer Buchhaltungsverteilungen () im Feld Rechnungscodierung mobilen Gerät für die Schecks angezeigt? Wenn die Antwort zu dieser Frage ist dies, beachten Sie die folgenden Fragen:
    -   Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen, Teilungen, usw.) gibt es für eine Rechnungsposition? Wieder gelten Sie die Regel 80-20 angezeigt.
    -   Halten Rechnungen auch die Buchhaltungsverteilungen im Rechnungskopf? Falls ja besten diese Buchhaltungsverteilungen im Gerät verfügbar sein?

> [!NOTE]
> In diesem Thema wird erläutert nicht, wie Sie Buchhaltungsverteilungen bearbeitet, da diese Funktion nicht aktuell für Szenarios mobile unterstützt werden.

-   Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?

Das Design der Erfahrung mobilen für Rechnungsgenehmigungen variiert, abhängig von den Antworten auf diese Fragen. Die Zielsetzung besteht, die Benutzerfreundlichkeit für den Geschäftsprozess auf Mobile in einer Organisation zu optimieren. Im Rest des Themas, beachten Sie zwei Szenarioabweichungen, die auf Grundlage unterschiedlicher Antworten auf Fragen vorhergehenden sind. 

Allgemeine Anleitung wenn mit dem mobilen Designer, vergewissern Sie sich, diese Änderungen veröffentlichen "Unternehmen", um zu verhindern Aktualisierungen.

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
<td>Welche Felder aus dem Rechnungskopf wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?</td>
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
<td>Welche Felder aus den Rechnungspositionen wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?</td>
<td><ol>
<li>Beschaffungskategorie</li>
<li>Leistung</li>
<li>Preis je Einheit</li>
<li>Nettobetrag der Position</li>
<li>Steuerbetrag (US 1099)</li>
</ol></td>
</tr>
<tr class="odd">
<td>Wie viele Rechnungspositionen gibt es? in einer Rechnung Wenden Sie die Regel 80-20 hier an, und führen Sie das für 80 Prozent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Möchten Benutzer Buchhaltungsverteilungen () im Feld Rechnungscodierung mobilen Gerät für die Schecks angezeigt?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen usw.), gibt es für eine Rechnungsposition? Wieder gelten Sie die Regel 80-20 angezeigt.</td>
<td>Erweiterter Preis: Mehrwertsteuer: 2 Zuschläge: 0 0</td>
</tr>
<tr class="even">
<td>Halten Rechnungen auch die Buchhaltungsverteilungen im Rechnungskopf? Falls ja besten diese Buchhaltungsverteilungen im Gerät verfügbar sein?</td>
<td>Nicht verwendet</td>
</tr>
<tr class="odd">
<td>Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Erstellen Sie des Arbeitsbereichs

1.  In einem Browser signieren offenes Dynamics 365 für Arbeitsgänge und unter.
2.  Nachdem Sie in signiert ist, legen Sie &mode=mobile ** ** der URL wie im folgenden Beispiel aussehen, anzeigen und aktualisieren Sie die Seite: https://yoururl/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**&lt;&gt;
3.  Klicken Sie auf Einstellungen ** ** (Gang) Schaltfläche in der oberen rechten Ecke der Seite und klicken dann ** mobile Zeit-App **. Der Anwendungs-Designer mobile muss zeigen, momentan Aufgabenaufzeichnung während verweist.
4.  ** Auf Hinzufügen ** um ein neuen Arbeitsbereich zu erstellen. In vorliegenden Beispiel Name die Verknüpfung ** meine Genehmigungen **.
5.  Geben Sie eine Beschreibung ein.
6.  Wählen Sie eine Arbeitsbereichfarbe aus. Die Arbeitsbereichfarbe wird für den Gesamtstil mobilen der Erfahrung für den Arbeitsbereich verwendet.
7.  Wählen Sie ein Symbol für den Arbeitsbereich aus.
8.  ** Ausgeführt ** auf
9.  ** Auf Veröffentlichen Arbeitsbereich ** um die Änderungen zu speichern

### <a name="vendor-invoices-assigned-to-me"></a>Mir zugewiesene Kreditorenrechnungen

Die erste Seite, mobile vielfältige Art sollen, ist die Liste der Rechnungen, die dem Benutzer zur Genehmigung zugewiesen werden. Um diese Seite zu entwerfen mobile, verwenden Sie die VendMobileInvoiceAssignedToMeListPage ** ** Seite in Dynamics 365 für Arbeitsgänge. Bevor Sie dieses Verfahren ausführen, stellen Sie sicher, dass mindestens eine Kreditorenrechnung zur Prüfung Ihnen zugewiesen ist und die Rechnungsposition zwei Verteilungen hat. Diese Einstellung erfüllt die Bedingungen für dieses Szenarios.

1.  In Dynamics 365 für Arbeitsgänge URL, ersetzen Sie den Namen nach der Menüoption ** um die VendMobileInvoiceAssignedToMeListPage ** mobile Version der ** für die Kreditorenrechnungen Mir zugewiesene ** Listenseite im ** Kreditor ** Modul zu öffnen. Je nach der Anzahl von Rechnungen, die Sie in Ihrem System besitzen, das Ihnen zugeordnet ist, wird auf dieser Seite die Rechnungen angezeigt. Wenn Sie einen bestimmte Rechnung anzuzeigen, kann der Filter auf der linken Seite verwenden. Allerdings benötigen wir eine bestimmte Rechnung nicht für dieses Beispiel. Es benötigen derzeit eine Rechnung, die Ihnen zugewiesen ist, welches Sie ermöglichen, mobile um die Seite zu entwerfen. Die neuen Seiten, die verfügbar sind, ist insbesondere zum Entwickeln von mobilen Szenarien für Kreditorenrechnung entworfen wurde. Daher müssen Sie diesen Seiten. Die URL muss der folgenden URL ähneln, nachdem Sie ihn und eingeben, muss die Seite, die in der Abbildung dargestellt wird, angezeigt werden sollen: https://yourURL/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile &lt;&gt;[ausstehende Kreditorenrechnungen![Mir zugewiesene Seite] ". /media/mobile-invoice-approvals01-1024x281.png)]". /media/mobile-invoice-approvals01.png)
2.  Klickt auf ** ** Einstellungen (Gang) Schaltfläche in der oberen rechten Ecke der Seite und klicken dann ** mobile Zeit-App **
3.  Wählen Sie einen und Arbeitsbereich auf aus ** Bearbeiten **
4.  ** Fügen Sie auf Seite hinzu ** um die ersten mobilen Seite zu erstellen.
5.  Geben Sie einen Namen ein, z ** meine Kreditorenrechnungen ** und eine Beschreibung ein, z ** die Kreditorenrechnungen Mir zugewiesene ** zur Prüfung.
6.  Click **Done**.
7.  Im Designer mobilen ** ** Felder auf der Registerkarte auf, ** Felder ** wählen Sie aus. Die Spalten auf der Listenseite müssen der folgenden Abbildung ähneln. [![den Spalten der ausstehenden Kreditorenrechnungen Mir zugewiesene Seite] ". /media/mobile-invoice-approvals02-1024x117.png)]". /media/mobile-invoice-approvals02.png)
8.  Fügen Sie den erforderlichen Spalten von der Listenseite hinzu, die angezeigt werden muss Benutzern in der mobilen Seite. Die Reihenfolge, in dem Sie hinzufügen, entspricht der Reihenfolge, in der die Felder an Endbenutzer angezeigt werden. Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen. Basierend auf den Anforderungen für dieses Szenarios, sind die folgenden acht Felder obligatorisch. Allerdings behalten mehrere Benutzer acht Felder für zu viele Informationen, die auf einem mobilen Gerät zu haben. Daher Anzeigen wird nur die wichtigsten Felder in der Listenansicht mobilen angezeigt. Die übrigen Felder erscheinen in der Detailansicht, dass diese später entwerfen. Fürs anfänglichen fügen Sie die folgenden Felder hinzu. Klicken Sie auf das Pluszeichen (**+**) Spalten, der in diesen mobilen Seite hinzuzufügen.
    1.  Kreditorenname
    2.  Rechnungssumme
    3.  Rechnungskonto
    4.  Rechnungsnummer
    5.  Rechnungsdatum

    Nachdem die Felder hinzugefügt sind, muss die Seite mobile der folgenden Abbildung ähneln. [![Seite nach] (Felder hinzugefügt werden. /media/mobile-invoice-approvals03.png)]". /media/mobile-invoice-approvals03.png)
9.  Sie müssen die folgenden Spalten nun auch hinzufügen, sodass wir Workflowaktivitäten später aktivieren können.
    1.  Vollständige Aufgabe der Spalte
    2.  Showdelegatenaufgabe
    3.  Es zurückrufen Aufgabe
    4.  Es weisen Aufgabe zurück
    5.  Showanforderungs-Abschlussaufgabe
    6.  Es Aufgabe erneut übermitteln

10. ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
11. ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
12. ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern.
13. Aktivieren Sie auf dem Anzeigenrechnungssumme ** Kreditorenrechnungsliste ** in der unter Kreditorparameterform ** ** Rechnung. Beachten Sie, dass, nur, indem Sie diesen Parameter aktiviert, Rechnungssummen berechnet werden, der auf Kreditorenrechnungslistenseite ausstehenden angezeigt werden. Dies ist eine neue Funktion als Teil des erforderlichen Hotfixes 3208224.

### <a name="vendor-invoice-details"></a>Kreditorenrechnungsdetails

Um die für Rechnungsdetailseite Datenschutzerklärung zu entwerfen, verwenden Sie die VendMobileInvoiceHeaderDetails ** ** Seite in Dynamics 365 für Arbeitsgänge. Beachten Sie diese, abhängig von der Anzahl der Rechnungen, die Sie in Ihrem System gibt, enthält dieser Seite die älteste Rechnung (die Rechnung, die zuerst erstellt wurde). Wenn Sie einen bestimmte Rechnung anzuzeigen, kann der Filter auf der linken Seite verwenden. Allerdings benötigen wir eine bestimmte Rechnung nicht für dieses Beispiel. Es müssen nur einige Rechnungsinformationen, sodass wir die mobile Seite zu entwerfen. ![Workflowseite( [] . /media/mobile-invoice-approvals04-1024x425.png)]". /media/mobile-invoice-approvals04.png)

1.  In Dynamics 365 für Arbeitsgänge URL, ersetzen den Namen nach der Menüoption ** VendMobileInvoiceHeaderDetails ** um das Formular zu öffnen
2.  Öffnen Sie den Designer von mobilen ** ** Einstellungen (Gang) Schaltfläche.
3.  Klicken Sie auf die ** Bearbeiten ** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.
4.  Wählen Sie die Kreditorenrechnungen ** meine ** Seite, die Sie eben erstellt haben, und klicken Sie dann ** Bearbeiten **.
5.  ** ** Felder auf der Registerkarte klicken Sie im Raster die ** ** Spaltenüberschrift.
6.  ** Auf Eigenschaften ** &gt; ** fügen Sie ** Seite hinzu. ** Hinweis: ** Wenn Sie auf das Raster ** ** Überschrift klicken und eine Seite hinzufügen, wird die Beziehung zur Detailseite automatisch bestimmt.
7.  Geben Sie einen Seitentitel, z ** Rechnungsdetails ** und einer Beschreibung, wie ein Ansichtsrechnungskopf ** und Positionsdetails **.
8.  ** Auf Felder ** wählen Sie aus. Notieren Sie das, die Reihenfolge, in der Sie von der Reihenfolge hinzufügen, in der die Felder an Endbenutzer angezeigt werden. Die einzige Methode, die Reihenfolge der Felder zu ändern ist, indem alle Felder erneut auswählen.
9.  Fügen Sie die folgenden Felder aus dem Auftragskopf, basierend auf den Anforderungen für dieses Szenarios hinzu:
    1.  Kreditorenname
    2.  Rechnungssumme
    3.  Rechnungskonto
    4.  Rechnungsnummer
    5.  Rechnungsdatum
    6.  Rechnungsbeschreibung
    7.  Fälligkeitsdatum
    8.  Rechnungswährung

10. Fügen Sie die folgenden Felder aus Positionsraster auf der Seite hinzu:
    1.  Beschaffungskategorie
    2.  Leistung
    3.  Preis je Einheit
    4.  Nettobetrag der Position
    5.  Steuerbetrag (US 1099)

11. Schließlich sind die Felder aus früheren zwei Schritte auf, der hinzugefügt wurden ** ** ausgeführt. Die Seite muss der folgenden Abbildung ähneln. [![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
13. ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
14. ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern

### <a name="workflow-actions"></a>Workflowaktivitäten

Um Workflowaktivitäten hinzuzufügen, verwenden Sie die VendMobileInvoiceHeaderDetails ** ** Seite in Dynamics 365 für Arbeitsgänge. Um diese Seite zu öffnen, ersetzen Sie Name der Menüoption in die URL, wie Sie eben geschehen ist. Öffnen Sie den Designer von mobilen ** ** Einstellungen (Gang) Schaltfläche. Gehen Sie folgendermaßen vor, um die Detailseite auf Workflowaktivitäten hinzuzufügen.

1.  Klicken Sie auf die ** Bearbeiten ** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.
2.  Wählen Sie die Rechnungsdetails ** ** Seite, die Sie eben erstellt haben, und klicken Sie dann ** Bearbeiten **.
3.  Wählen Sie auf der Registerkarte auf Aktivitäten ** ** ** fügen Sie ** Aktivität hinzufügen.
4.  Geben Sie einen Aktivitätstitel, z ** Genehmigen ** und eine Beschreibung ein, z ** Genehmigen ** Rechnung. Beachten Sie, dass der Aktivitätstitel, den Sie hier eingeben, der Name der Aktivität ist, den Benutzer in der Zeit-App mobilen die angezeigt wird.
5.  Click **Done**.
6.  ** Auf Felder ** wählen Sie aus.
7.  Führen des Workflowprozesses auf der VendMobileInvoiceHeaderDetails ** ** Seite durch, und schließen Sie die Aktivität aus, die Sie erfassen. Ihren Planungen zufolge Überprüfen Sie, ob Sie Workflowkommentare während dieses Vorgangs ein eingegeben werden, damit auch im Kommentarfeld mobilen Erfahrung enthalten ist.
8.  Nachdem die Workflowaktivität ausgeführt ist, klicken Sie zunächst ** ** um die Auswählensfeldaufgabe abzuschließen.
9.  ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
10. ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
11. ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern
12. Wiederholen Sie die Schritte 3 bis 11, um alle erforderlichen Workflowaktivitäten zu erfassen. Notieren Sie das, es ist eine Anforderung, die Rechnungen anzuzeigen, die Ihnen zugewiesen sind, die in einen Status besitzen, um der Arbeitsplanaktivitäten des Katalogs für Sie, dass Sie für entwerfen werden.
13. Öffnen Sie oder Editor Microsoft Visual Studio, und fügen Sie den folgenden Code ein. Speichern Sie die Datei als JS-Datei. Dieser Code mit zwei Elementen:
    1.  Er blendet die zusätzlichen workflowbezogenen Spalten aus, die wir früher mobilen auf der Listenseite hinzugefügt. Es werden diesen Spalten hinzufügen, sodass der Zeit-App dass Informationen im Zusammenhang hat und die nächsten Schritt ausführen kann.
    2.  Anhand des Workflowschritt, die aktiv ist, wendet sie Logik, um nur die Vorgänge anzeigen.

Beachten Sie, das den Namen der Seiten und anderen Steuerelemente im JS-Code müssen identisch dem Arbeitsbereich sein.

1.  Funktionshauptleitung (metadataService, dataService, cacheService, $q) {Rücklieferung {appInit: Funktion "appMetadata) {//-, die Fellkontrollen vorhanden sein müssen, sichtbares jedoch nicht metadataService.configureControl (" Mein-Kreditor-Rechnungen ", "ShowAccept" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowApprove" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowReject" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowDelegate" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowRequestChange" {, ausgeblendet: true});              metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowRecall" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowComplete" {, ausgeblendet: true});            metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowResubmit" {, ausgeblendet: true});            }, pageInit: Funktion "pageMetadata, Parameter) {wenn pageMetadata.Name-== ("") Rechnung-Details //-{angezeigt bzw. -fellworkflowaktivitäten Workflowschritt auf Grundlage metadataService.configureAction (" angezeigt, Sie nehmen "{angezeigt: true});                    metadataService.configureAction ("Genehmigen" {, angezeigt: true});                    ("metadataService.configureAction Ablehnen" zurück, {angezeigt: true});                    ("metadataService.configureAction Stellvertreter" {, angezeigt: true});                    metadataService.configureAction (", Anforderung-Änderung" {angezeigt: true});                    metadataService.configureAction ("erhalten Sie erneut auf," {angezeigt: true});                    metadataService.configureAction ("Schließen" {ab, angezeigt: true});                    ("metadataService.configureAction erneutes Absenden" {, erneut angezeigt: true});

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

2.  Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie die Logik ** ** Registerkarte auswählen
3.  ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
4.  ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
5.  ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern

### <a name="vendor-invoice-attachments"></a>Kreditorenrechnungsanhänge

1.  Klickt auf ** ** Einstellungen (Gang) Schaltfläche in der oberen rechten Ecke der Seite und klicken dann ** mobile Zeit-App **
2.  Klicken Sie auf die ** Bearbeiten ** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten.
3.  Wählen Sie die Rechnungsdetails ** ** Seite, die Sie eben erstellt haben, und klicken Sie dann ** Bearbeiten **.
4.  Legen Sie die Dokumentverwaltung ** ** ** Option Ja ** wie weiter unten) fest. ** Hinweis: ** Wenn keine Anforderungen gibt, Zuordnungen im mobilen Gerät angezeigt werden, können Sie diese Option aktiviert ** no lassen **, mit der die Standardeinstellung ist.
5.  ![docmanagement ([]. /media/docmanagement-216x300.png)]". /media/docmanagement.png)
6.  ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
7.  ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
8.  ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern

### <a name="vendor-invoice-line-distributions"></a>Kreditorenrechnungspositionsverteilungen

Die Anforderungen für dieses Szenarios bestätigen, dass nur Verteilungen auf Positionsebene sind und dass eine Rechnung immer nur eine Position ist. Da dieses Szenario ist einfach, muss die Benutzerfreundlichkeit auf dem auch einfach mobilen Gerät genug sein, dem der Benutzer nicht mehrere Ebenen muss Detailinformationen anzeigen, damit die Verteilungen anzuzeigen. Kreditorenrechnungen in Dynamics 365 für Arbeitsgänge umfassen die Option des Anzeigens aller Verteilungen aus dem Rechnungskopf. Diese ist Erfahrung, die wir für das mobile Szenario müssen. Daher verwenden Sie die VendMobileInvoiceAllDistributionTree ** ** Seite, um diesen Teil des mobilen Szenarios zu entwerfen. 

> [!NOTE] 
> Das Kennen der Anforderungen können uns, entscheiden, die die betreffende genau zu verwenden Seite, und wie die mobile Erfahrung des Benutzers optimiert, wenn Sie das Szenario entwerfen. Im zweiten Szenario können wir eine andere Seite, damit die Verteilungen anzuzeigen, weil die Anforderungen für dieses Szenarios unterscheiden.

1.  In der URL ersetzen Sie den Namen der Menüoption, wie Sie vorab geschehen ist. Die Seite, die angezeigt wird, sollte der folgenden Abbildung ähneln. [![alle Verteilungsseite]" . /media/mobile-invoice-approvals06.png)]". /media/mobile-invoice-approvals06.png)
2.  Öffnen Sie den Designer von mobilen ** ** Einstellungen (Gang) Schaltfläche.
3.  Klicken Sie auf die ** Bearbeiten ** Schaltfläche, um im Bearbeitungsmodus Arbeitsbereich zu starten. ** Hinweis: ** Sie sehen, dass zwei neue Seiten automatisch erstellt wurden. Das System diese Seiten erstellt, da Sie die Dokumentverwaltung im vorherigen Abschnitt einschalteten. Sie können diese Seiten neuen ignorieren.
4.  ** Fügen Sie auf Seite hinzu **.
5.  Geben Sie einen Seitentitel, wie Ansichtsbuchhaltung ** ** und eine Beschreibung ein, z ** die Ansicht, welche die Rechnung für **.
6.  Click **Done**.
7.  ** Felder ** Auf der Registerkarte wählen Sie ** Wählen Sie Felder aus **, die folgenden Felder aus der Verteilungsseite aus und klicken dann ** getan **:
    1.  Betrag
    2.  Währung
    3.  Sachkonto

> [!NOTE] 
> Es können die Beschreibung nicht ** ** Spalte im Verteilungsraster aus, weil die Anforderungen für dieses Szenarios bestätigten, dass der erweiterte Preis der einzige Betrag ist, dass für Verteilungen gibt. Daher fordert der Benutzer kein anderes Feld, den Betragstyp festzustellen, ob die Verteilung für ist. Allerdings im folgenden Szenario verwenden, wir ** ** werden Sie diese Informationen, weil die Anforderungen für dieses Szenarios angeben, dass andere Betragsart Verteilungen haben (z, Mehrwertsteuer).
8.  ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
9.  ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
10. ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern

** Hinweis: ** Die Ansichtsbuchhaltung ** ** mobile Seite wird der derzeit keinem mobilen Seiten verknüpft, die wir Monatsbeginn entworfen haben. Da der Benutzer in der Lage sein soll, die Ansichtsbuchhaltung ** ** Seite aus der ** Rechnungsdetails ** Seite im mobilen Gerät zu navigieren, müssen Sie zuvor aus der ** Rechnungsdetails ** Seite der Ansichtsbuchhaltung ** ** Seite bereitstellen. Wir legen die Navigationsverknüpfung ein, indem wir Zusatzlogik zu JavaScript verwenden.

1.  Öffnen Sie die JS-Datei, die Sie eben erstellt haben, und fügen Sie die Positionen hinzu, die im folgenden Code hervorgehoben werden. Dieser Code mit zwei Elementen:
    1.  Er wird sichergestellt, dass Benutzer nicht direkt über der Arbeitsbereich ** Ansichtsbuchhaltung ** Seite Navigation können.
    2.  Er wird ein Navigationssteuerelement der ** Rechnungsdetails ** Seite der Ansichtsbuchhaltung ** ** Seite ein.

> [!NOTE] 
> Der Name der Seiten und anderen Steuerelemente im JS-Code muss dem dem Arbeitsbereich sein.

1.  Funktionshauptleitung (metadataService, dataService, cacheService, $q) {Rücklieferung {appInit: Funktion "appMetadata) {//-, die Fellkontrollen vorhanden sein müssen, sichtbares jedoch nicht metadataService.configureControl (" Mein-Kreditor-Rechnungen ", "ShowAccept" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowApprove" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowReject" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowDelegate" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowRequestChange" {, ausgeblendet: true});              metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowRecall" {, ausgeblendet: true});                metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowComplete" {, ausgeblendet: true});            metadataService.configureControl ("Mein-Kreditor-Rechnungen", "ShowResubmit" {, ausgeblendet: true});                //-Fellseiten nicht verfügbar für Stammnavigation metadataService.hideNavigation (" ")Ansicht-Buchhaltung;                //Link, um metadataService.addLink berechnenden ("Rechnung-Details", "Ansicht-Buchhaltung", "Ansicht-Buchhaltung-NAV-Steuerelement", "Ansichtsbuchhaltung " true,) anzuzeigen;            }, pageInit: Funktion "pageMetadata, Parameter) {wenn pageMetadata.Name-== ("") Rechnung-Details //-{angezeigt bzw. -fellworkflowaktivitäten Workflowschritt auf Grundlage metadataService.configureAction (" angezeigt, Sie nehmen "{angezeigt: true});                    metadataService.configureAction ("Genehmigen" {, angezeigt: true});                    ("metadataService.configureAction Ablehnen" zurück, {angezeigt: true});                    ("metadataService.configureAction Stellvertreter" {, angezeigt: true});                    metadataService.configureAction (", Anforderung-Änderung" {angezeigt: true});                    metadataService.configureAction ("erhalten Sie erneut auf," {angezeigt: true});                    metadataService.configureAction ("Schließen" {ab, angezeigt: true});                    ("metadataService.configureAction erneutes Absenden" {, erneut angezeigt: true});

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

2.  Laden Sie die Codedatei dem Arbeitsbereich hohe, indem Sie aktivieren die Logik ** ** vorherigen Registerkarte, um den Code zu überschreiben
3.  ** Auf erfolgt ** um den Bearbeitungsmodus auszusteigen.
4.  ** Auf Zurück ** und ** getan ** den Arbeitsbereich dann beendet
5.  ** Auf Veröffentlichen Arbeitsbereich ** um die Arbeit zu speichern

### <a name="validation"></a>Prüfung

In Ihrem mobilen Gerät Öffnen der Zeit-App und Verbinden mit Ihr Dynamics 365 für Arbeitsgangsinstanz angezeigt. Überprüfen Sie, ob Sie in das Unternehmen ein, in dem Kreditorenrechnungen Ihnen zur Prüfung zugewiesen werden. Sie sollten in der Lage sein, die folgenden Aktionen ausführen:

-   Siehe den ** meine Genehmigungen ** Arbeitsbereich.
-   Drillvorgang in den ** meine Genehmigungen ** Arbeitsbereich und erscheinen die ** meine Kreditorenrechnungen ** Seite.
-   Drillvorgang in die ** meine Kreditorenrechnungen ** Seite und erscheinen die Liste der Rechnungen, die Ihnen zugewiesen sind.
-   Drillvorgang in eine der Rechnungen und die Rechnungskopfdetails finden und -Positionsdetails.
-   Auf der Detailseite finden Sie einen Link zu den Anlagen, und verwenden Sie diesen Link, die der Anhangliste zu navigieren und die Anhänge anzeigen.
-   Auf der Detailseite finden Sie einen Link zu der Ansichtsbuchhaltung ** ** Seite, und verwenden Sie diesen Link, die der Verteilungsseite zu navigieren und Vertriebsmengen anzeigen.
-   Auf der Detailseite klicken Sie auf das Menü ** Aktivitäten ** unten, und lassen Workflowaktivitäten aus, die z Workflowschritt gültig sind.

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
<td>Welche Felder aus dem Rechnungskopf wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?</td>
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
<td>Welche Felder aus den Rechnungspositionen wünscht der Benutzer in mobilen finden, der Erfahrung und in welcher Reihenfolge?</td>
<td><ol>
<li>Beschaffungskategorie</li>
<li>Leistung</li>
<li>Preis je Einheit</li>
<li>Nettobetrag der Position</li>
<li>Steuerbetrag (US 1099)</li>
</ol></td>
</tr>
<tr class="odd">
<td>Wie viele Rechnungspositionen gibt es? in einer Rechnung Wenden Sie die Regel 80-20 hier an, und führen Sie das für 80 Prozent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Möchten Benutzer Buchhaltungsverteilungen () im Feld Rechnungscodierung mobilen Gerät für die Schecks angezeigt?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Wie viele Buchhaltungsverteilungen (erweiterte Preis, Mehrwertsteuer, Belastungen usw.), gibt es für eine Rechnungsposition? Wieder gelten Sie die Regel 80-20 angezeigt.</td>
<td>Erweiterter Preis: Mehrwertsteuer: 2 Zuschläge: 2 2</td>
</tr>
<tr class="even">
<td>Halten Rechnungen auch die Buchhaltungsverteilungen im Rechnungskopf? Falls ja besten diese Buchhaltungsverteilungen im Gerät verfügbar sein?</td>
<td>Nicht verwendet</td>
</tr>
<tr class="odd">
<td>Möchten Benutzer Anhänge für die Rechnung auf dem Gerät angezeigt?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Übung

Die Abweichungen können folgenden Szenario für 1, basierend auf den Anforderungen für Szenario 2.) erfolgen. Verwenden Sie diesen Bereich als Übung, die Sie für das Ausgeben zu Berichtszwecken abschließen können.

1.  Da weitere Rechnungspositionen in Szenario 2 erwartet werden, können folgende Änderungen zum Entwurf, die Benutzererfahrung im mobilen Gerät zu optimieren:
    1.  Anstelle der Betrachtungsrechnungspositionen auf Detailseite der (z in Szenario kann 1), Benutzer festlegen, dass Positionen einer separaten mobilen Seite anzeigen.
    2.  Da mehrere Rechnungsposition in diesem Szenario erwartet wird, wenn die VendMobileInvoiceAllDistributionTree ** ** Seite verwendet wird, um die Verteilungsseite für Datenschutzerklärung zu entwerfen (wie in Szenario 1), kann es verwirrend, damit der Benutzer Positionen mit Verteilungen aufeinander umfasst. Daher verwenden Sie die VendMobileInvoiceLineDistributionTree ** ** Seite, um die Verteilungsseite zu entwerfen.
    3.  Im Idealfall sollten die Verteilungen im Kontext einer Rechnungsposition in diesem Szenario angezeigt werden. Daher müssen Sie unbedingt, ob der Benutzer in einer Position richten bohren kann, um die Verteilungsseite anzuzeigen. Verwenden Sie die Seitenlinkfunktion, den Drillthrough einzurichten, wie Sie für den Kopf und die Detailseiten in Szenario 1. ".

2.  Da mehrere ein Betragsart für die Verteilungen in Szenario 2 ", Mehrwertsteuer, Belastungen usw.) erwartet wird, ist es hilfreich, die Beschreibung des Betrags Typ anzeigen. (Wir können diese Informationen in Szenario 1) auf.

## <a name="conclusion"></a>Schlussfolgerung
Die mobile Plattform und die Anwendungsfunktionen lassen Sie entwerfen mobile Szenarien, die für eine Benutzerbasis in einer Organisation optimiert werden. Anhand der Beispiele, die in diesem Thema zur Verfügung stehen, können Sie versuchen verschiedene andere Abweichungen und Erfahrungen erstellen, die eine bestimmte Anforderungen erfüllen.


