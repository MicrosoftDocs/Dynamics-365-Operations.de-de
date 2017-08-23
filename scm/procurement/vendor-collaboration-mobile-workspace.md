---
title: "Mobiler Arbeitsbereich für Kreditorenzusammenarbeit"
description: "Dieses Thema enthält Informationen zur Lieferantenzusammenarbeit im mobilen Arbeitsbereich. Dieser Arbeitsbereich hilft Kreditoren, auf dem neuesten Stand der Bestellungen zu sein, die ihnen zur Genehmigung gesendet wurden. Sie können auch Informationen zu neuen und aktualisierten Bestellungen und Kontakten anzeigen."
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: fc8b7f6901ffd5c97fb864dbd3f87c5c70a31487
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-mobile-workspace"></a>Mobiler Arbeitsbereich für Kreditorenzusammenarbeit

[!include[banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur **Lieferantenzusammenarbeit** im mobilen Arbeitsbereich. Dieser Arbeitsbereich hilft Kreditoren, auf dem neuesten Stand der Bestellungen zu sein, die ihnen zur Genehmigung gesendet wurden. Sie können auch Informationen zu neuen und aktualisierten Bestellungen und Kontakten anzeigen.

Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden.

## <a name="overview"></a>Überblick 
Der Arbeitsbereich für die **Kreditor-Kooperation** hält Kreditoren über neue Bestellungen auf dem Laufenden, sodass diese neue Bestellungen im Webclient von Microsoft Dynamics 365 for Finance and Operations, Enterprise Wediton zu sehen ist. 

>[!NOTE]
> Der mobile Arbeitsbereich sollte als Ergänzung und nicht als Ersatz der Weboberfläche für die Kreditor-Kooperation eingesetzt werden. 

Mit dem mobilen Arbeitsbereich der **Kreditor-Kooperation** können Kreditoren neue Bestellungen anzeigen, die ihnen zur Genehmigung übermittelt wurden. Er zeigt Bestellinformationen wie Menge und Produkte sowie das angeforderte Versanddatum an. Preisangaben sind je nach Konfiguration für den jeweiligen Kreditor verfügbar. 

Wenn sich Benutzer als Kreditor anmelden, sehen sie, auf welche Bestellungen reagiert wurde und für welche Bestellungen noch Debitorenaktivitäten ausstehen. Der Kreditor hat möglicherweise ein anderes Lieferdatum vorgeschlagen, dem der Debitor noch nicht zugestimmt hat, sodass die Bestellung auf eine Debitorenaktivität wartet. Der Kreditor sieht auch eine Liste der Bestellungen, die bestätigt aber noch nicht geliefert wurden. 

Um auf eine Bestellung zu antworten, muss der Kreditor die Weboberfläche für die Kreditor-Kooperation verwenden, die im Webclient von Dynamics 365 for Operations verfügbar ist. Dort findet der Kreditor auch zusätzliche Informationen zum Auftrag, wie Dokumentanhänge, Lieferadresse pro Position sowie Zuschläge, die dem Kreditor zugeordnet wurden. 

Mit einer speziellen Sicherheitsrolle kann sich der Kreditor Kontaktpersonen anzeigen lassen, die für ein Kreditorenkonto registriert sind. Mit der gleichen Sicherheitsrolle kann der Kreditor den Status jeder Benutzeranforderung anzeigen, die gesendet wurde. 

Die Kreditorenzusammenarbeitsoberfläche im Webclienten muss verwendet werden, um zu neue Kontakte neue Benutzeranforderungen zu erstellen. 

Der mobile Arbeitsbereich **Kreditorenzusammenarbeit** ermöglicht einem Kreditor diese Aufgaben ausführen:

-   Neue Bestellungen anzeigen, die an den Kreditor gesendet wurden.
-   Bestellungen anzeigen, auf die der Kreditor reagiert hat und die auf eine Debitorenaktivität warten.
-   Bestellungen anzeigen, die bestätigt wurden aber noch nicht vollständig empfangen wurden.
-   Hier werden Kontaktpersoneninformationen angezeigt, die für das Kreditorenkonto erfasst wurden. (Diese Aufgabe ist eine zusätzliche Sicherheitsrolle.)
-   Informationen anzeigen und den Status einer Benutzeranforderung verfolgen, die vom Kreditor übermittelt wurde. (Diese Aufgabe ist eine zusätzliche Sicherheitsrolle.)

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, Update vom Juli 2017 verwenden 
Wenn das Update von Juli 2017 für Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition, für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Kreditor-Kooperation** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später verwenden.
Wenn Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3216943 KB muss implementiert werden, wenn Sie Plattformaktualisierung 3. verwenden.</td>
<td>Systemadministrator</td>
<td>3216943 KB ist eine binäre Aktualisierung, die erforderlich ist, wenn Sie Plattformaktualisierung 3. verwenden. Um diesen KB zu implementieren, muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li>Herunterladen von KB 3216943 von Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Binäre Aktualisierung instalieren, die zur Bereitstellung als geeignetes Paket geliefert wird. Informationen dazu, wie ein bereitgestelltes Paket übernommen wird, finden Sie unter<a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ein bereitgestelltes Paket anwenden</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>4013633 KB muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>4013633 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Lagerbestand</strong> enthält. Um KB 4013633 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Laden Sie den Metadatumenhotfix herunter</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadatenhotfix</a>.</li><li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das das <strong>SCMMobile</strong> Modell enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Das bereitstellbare Paket übernehmen</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Die <strong>Kreditoren-Kooperation</strong> mobiler Arbeitsbereich muss veröffentlicht werden.</td><td>Systemadministrator</td>
<td>Siehe <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
<tr class="even">
<td>Der Kreditorenbenutzer muss Zugriff auf die Weboberfläche für die Kreditor-Kooperation im Webclient haben und muss als Keditor-Kooperations-Benutzer eingerichtet werden.</td><td>Einkäufer und Systemadministrator</td>
<td>Führen Sie die Schritte, die in den folgenden Themen beschrieben werden, aus, um die Weboberfläche für die Kreditor-Kooperation einzurichten und mit dieser zu arbeiten.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Nutzen der Kreditor-Kooperation für die Zusammenarbeit mit externen Kreditoren</a></li>
<li><a href="manage-vendor-collaboration-users.md">Benutzer für Kreditor-Kooperationen verwalten</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Kreditorenzusammenarbeit einrichten und verwalten</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Verwenden der Kreditor-Kooperation für Kunden in Finance and Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App

Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:

-   [Für Androide-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die Microsoft Dynamics 365-URL ein.
4.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
5.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

    [![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Mobiler Arbeitsbereich für Kreditorenzusammenarbeit nutzen
Wenn Sie **Kreditorenzusammenarbeit** auswählen, finden Sie folgende Optionen.

![Mobiler Arbeitsbereich für Kreditorenzusammenarbeit](./media/vendor-collaboration-mobile-app.png)

Der Arbeitsbereich **Kreditorenzusammenarbeit** enthält die folgenden Seiten.

### <a name="contacts"></a>Kontakte
Auf der Seite **Kontakte** werden alle Kontakte angezeigt, die für das Kreditorenkonto eingerichtet wurden. Darin wird der Name der Kontaktperson, die primäre E-Mail-Adresse und den Benutzer auch angezeigt, wenn die Kontaktperson einen Alias hat. Diese Seite zeigt an, ob das Benutzerkonto der Kontaktperson aktiv ist. Wenn Sie einen Kontakt auswählen, sehen Sie Kontaktdetails, wie die juristische Personen, für die die Person als Kontakt fungiert. Sie sehen auch die Kontaktinformationen, beispielsweise Telefonnummer oder eine alternative E-Mail-Adresse.

### <a name="user-requests"></a>Benutzeranforderungen
Auf der Seite **Benutzeranforderungen** werden all die Benutzeranforderungen angezeigt, die Sie über die Weboberfläche der Kreditor-Kooperation übermittelt haben. Sie können auch den Status dieser Anfragen anzeigen. Wenn Sie eine Benutzeranforderung auswählen, wird angezeigt, was angefordert wurde. Sie können einen Benutzer hinzufügen oder deaktivieren, die Sicherheit ändern und anzeigen, welche Sicherheitsrollen für den Benutzer angefordert wurden.

### <a name="purchase-orders-ready-for-review"></a>Zur Überprüfung bereite Bestellungen
Auf der Seite **Zur Überprüfung bereite Bestellungen** werden alle Bestellungen angezeigt, die vom Debitor gesendet und noch nicht beantwortet wurden. Sie können ausgewählte Informationen zum Auftrag anzeigen, beispielsweise welche Produkte angefordert wurden und wann diese geliefert werden sollen. Preisangaben sind je nach Konfiguration für den jeweiligen Kreditor verfügbar.

Sie können anzeigen, ob zur Bestellung Hinweise oder Anhänge vorhanden sind. Um Hinweise und Zuordnungen zu öffnen, müssen Sie aber die Kreditorenzusammenarbeitweboberfläche im Webclienten verwenden. Wählen Sie **Bestellposition** aus, um alle Positionen mit Details anzuzeigen. Beachten Sie, dass ein Indikator für jede Position anzeigt, ob Hinweise oder Anhänge vorhanden sind und ob es eine Lieferadresse gibt, die sich von in der Kopfzeile angezeigten Informationen unterscheidet.

Um auf die Bestellung zu antworten, müssen Sie den Kreditor-Kollaboration-Webclient verwenden.

### <a name="awaiting-customer-action"></a>Debitorenaktivität ausstehend
Auf der Seite **Debitorenaktivität ausstehend** werden die Bestellungen angezeigt, auf die Sie oder jemand aus Ihrem Unternehmen mit Zugriff auf die Kreditor-Kollaboration geantwortet haben. Die Bestellungen werden in dieser Liste nur angezeigt, wenn der Debitor eine der folgenden Aktionen für die Bestellung ausführen muss.

-   Wenn die Bestellung abgelehnt wurde, muss der Debitor entweder den gesendeten Auftrag aktualisieren und erneut senden oder den Auftrag stornieren und erneut übermitteln. Wenn die Bestellung erneut übermittelt wird, wird sie nicht mehr auf der Seite **Debitorenaktivität ausstehend** angezeigt.
-   Wenn die Bestellung mit Änderungen akzeptiert wurde, muss der Debitor den ursprünglichen Auftrag aktualisieren und zur Überprüfung erneut einsenden oder diesen entsprechend der Änderungen aktualisieren und sofort bestätigen. In beiden Fällen wird die Bestellung nicht mehr länger auf der Seite **Debitorenaktivität ausstehend** angezeigt.
-   Wenn die Bestellung angenommen wurde und auf der Seite **Debitorenaktivität ausstehend** angezeigt wird, liegt das daran, dass die Bestellung nach dem Akzeptieren nicht automatisch bestätigt wurde. In diesem Fall muss der Einkäufer den Status des Auftrags in **Bestätigt** ändern. Normalerweise wird die Bestellung als eine Vereinbarung zwischen dem Debitor und dem Kreditor betrachtet, sobald der Kreditor den Auftrag annimmt. Daher wird die Aktualisierung auf den Status **Bestätigt** lediglich eine Formalität.

Indem die Bestellung ausgewählt wird, werden weitere zusätzliche Details zur Antwort angezeigt. Sie können die Positionsdetails und die Antworten für die einzelnen Positionen anzeigen. Der Positionsstatus gibt an, welche der folgenden Antworten gegeben wurden:

-   Angenommen
-   Verweigert
-   Mit Änderungen akzeptiert
-   Ersetzt/Ersatz
-   In Zeitplan aufgeteilt/Zeitplanposition

Beachten Sie, dass das Feld **Hier** entweder auf **Ja** oder auf **Nein** festgelegt ist, um anzugeben, ob die Positionen geliefert werden. Eine Position wird nicht geliefert werden aus folgenden Gründen:

- Anforderungsposition abgelehnt.
- Eine Gutschrift wurde vorgenommen und die ursprüngliche Position nicht wie erwartet geliefert.
- Die Position wurde in mehrere Zeitplanpositionen aufgeteilt, und die ursprüngliche Position wird nicht wie angefordert geliefert.

Sämtliche Änderungen, die in der Auftragspositionsantwort vorgenommen wurden, werden angezeigt. Allerdings werden hochgeladene Hinweise und Anhänge nicht angezeigt. Um Hinweise und Zuordnungen zu öffnen, müssen Sie aber die Kreditorenzusammenarbeitweboberfläche im Webclienten verwenden.

### <a name="open-confirmed-orders"></a>Offene bestätigte Aufträge
Wenn die Bestellung vom Debitor bestätigt wird (d. h. der Status des Auftrags, wird auf **Bestätigt** geändert), erscheint sie unter den offenen, bestätigten Aufträgen. Sie bleibt in der Liste, bis sie als vom Debitor empfangen registriert wird.

