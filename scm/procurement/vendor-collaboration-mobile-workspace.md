---
title: "Mobiler Arbeitsbereich der Kreditorenzusammenarbeit für Microsoft Dynamics 365 für Arbeitsgangs-App"
description: "Mit dem Arbeitsbereich mobilen der Kreditoren zusammenarbeit können Ihre Kreditoren auf Bestellungen bleiben, die aktuell für die zur Genehmigung gesendet wurde und Informationen zur neuen und aktualisierten Bestellungen und die Kontakte angezeigt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiler Arbeitsbereich der Kreditorenzusammenarbeit für Microsoft Dynamics 365 für Arbeitsgangs-App

Mit dem Arbeitsbereich mobilen der Kreditoren zusammenarbeit können Ihre Kreditoren auf Bestellungen bleiben, die aktuell für die zur Genehmigung gesendet wurde und Informationen zur neuen und aktualisierten Bestellungen und die Kontakte angezeigt werden.

<a name="prerequisites"></a>Voraussetzungen
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lesen Sie zum Microsoft Dynamics 365 für Arbeitsgangsmobileplattform</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 für Arbeitsgangsmobileplattform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 für Arbeitsgänge</td>
<td>Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 für Arbeitsgangsversion 1611 und Microsoft Dynamics for Arbeitsgangsplattformaktualisierung 3 (November 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiles Gerät, das das Dynamics 365 für die Einstellungen Arbeitsgangs-App hat</span></td>
<td><span style="color: #000000;">Lädt die Dynamics 365 für Arbeitsgangs-App von Ihrem App-Shop mobilen herunter.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 3215650</td>
<td>Installieren des Hotfix, um die Arbeitsbereiche zu ermöglichen, die in Arbeitsgängen für Dynamics 365 bereitgestellt werden.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix KB 3216943</span></span></td>
<td>Installieren des Hotfix, um den Kreditorenzusammenarbeit-Mobilearbeitsbereich zu aktivieren.</td>
</tr>
<tr class="even">
<td>Der Kreditorenbenutzer muss Zugriff auf die Kreditorenzusammenarbeitweboberfläche in Dynamics 365 für Arbeitsgänge haben und einen Kreditorenzusammenarbeitbenutzer einrichten.</td>
<td>Führen Sie die Schritte, die in den folgenden Themen beschrieben werden, um mit der Kreditorenzusammenarbeitweboberfläche einzurichten und zu arbeiten.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Verwenden Sie Kreditorenzusammenarbeit, um mit externen Kreditoren zusammenarbeiten zu können</a></li>
<li><a href="manage-vendor-collaboration-users.md">Benutzer für Kreditor-Kooperationen verwalten</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Kreditammenarbeit einrichten und verwalten</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Verwenden Sie Kreditorenzusammenarbeit, um mit Debitoren in Dynamics 365 für Arbeitsgänge zu arbeiten</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Überblick
Der Arbeitsbereich mobile der Kreditoren zusammenarbeit enthält diese Kreditoren darüber zu informieren, sodass sie auf Bestellungen in Dynamics 365 für Arbeitsgangswebclienten anzeigen und eine Antwort können.  

** Hinweis: ** Der Arbeitsbereich mobile soll als Ergänzung der Kreditorenzusammenarbeitweboberfläche Ersetzung, aber nicht verwendet werden.  

Mit dem Arbeitsbereich mobilen der Kreditoren zusammenarbeit können Ihre Kreditoren diese anzeigen, die zur Genehmigung übermittelt werden. Sie enthält Bestellinformationen, wie Menge und Produkte, das angeforderte Versanddatum. Preisangaben sind, je nach Konfiguration für jeden Lieferanten verfügbar.  

Auf wenn ein Benutzer als Kreditor anmeldet, finden sie, welche Bestellungen beantwortet wurden oder welche Bestellungen Debitorenaktivität noch aussteht. Der Kreditor geschlagen ein anderes Lieferdatum vor, das noch nicht mit dem Debitor übereingestimmt wird, sodass die Bestellung Debitorenaktivität erwartet. Der Kreditor wird auch eine Liste der Bestellungen, die bestätigt wurden, jedoch noch nicht geliefert.  

Um auf eine Bestellung zu antworten, muss der Kreditor die Kreditorenzusammenarbeitweboberfläche verwenden die in Dynamics 365 für Arbeitsgangswebclienten verfügbar ist. Dies gilt auch, wo der Kreditor über zusätzliche Informationen zum Auftrag, wie Dokumentanhänge, Lieferadresse pro Position sowie Zuschläge abrufen, die dem Kreditor zugeordnet werden.  

Mit einer speziellen Sicherheitsrolle kann sich der Kreditor angezeigt, den Kontaktpersonen für ein Kreditorenkonto erfasst werden. Mit der gleichen Sicherheitsrolle kann der Kreditor den Status jeder Benutzeranforderung anzeigen, die gesendet wurde.  

Das Erstellen neuer Kontakten und zum Übermitteln von Benutzeranforderungen neuen müssen in der Kreditorenzusammenarbeitschnittstelle erfolgen, die im für Arbeitsgangswebclienten Dynamics 365 verfügbar ist.  

Mit dem Arbeitsbereich mobilen kann Ihr Kreditor:

-   Ansichtsneuanschaffungskaufaufträge an den Kreditor gesendet.
-   Ansichtsbestellungen, dass der Kreditor in reagiert hat und Debitorenaktivität erwarten.
-   Anzeigen von Bestellungen, die in ein bestätigtes Status besitzen und nicht vollständig eingegangen sind.
-   Hier werden Kontaktpersoneninformationen angezeigt, die für das Kreditorenkonto erfasst wird eine zusätzliche Sicherheitsrolle (erforderlich).
-   Hier können Sie Informationen zur und folgen Sie den Status einer Benutzeranforderung, die vom Kreditor übermittelt wird eine zusätzliche Sicherheitsrolle (erforderlich).

## <a name="get-started"></a>Erste Schritte
Klicken Sie auf dem mobiles Gerät anfangen:

1.  Auf dem App-Shop mobilen Hochladen der Dateien herunter und Einrichten des Microsoft Dynamics 365 für Arbeitsgangs-App.
2.  Starten der Zeit-App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen, um in zu signieren. Geben Sie beispielsweise ein USMF ** **.
5.  Das zum ersten Mal, in dem Sie gerade signieren, werden für Sie den Benutzernamen und das Kennwort für Ihr Microsoft Dynamics 365 für Arbeitsgangskonto aufgefordert. 

Nachdem Sie der Zeit-App anmelden, sind Keiner Arbeitsbereiche angezeigt. Um auf Arbeitsbereiche der Zeit-App mobilen anzuzeigen, müssen Sie die gewünschten Arbeitsbereiche dem Dynamics 365 für Arbeitsgangs-App zuerst veröffentlichen. Sie benötigen Systemverwaltungsberechtigung, den Arbeitsbereich zu veröffentlichen.

1.  Start Dynamics 365 für Arbeitsgänge.
2.  Wechseln ** Systemverwaltung ** &gt; ** Einstellungen ** &gt; ** Systemparameter **.
3.  Wählen Sie aus ** Verwalten mobile Zeit-App **.
4.  Wählen Sie den aus Kreditorenzusammenarbeit Arbeitsbereich ** ** die der mobilen Plattform zu veröffentlichen.
5.  Wählen Sie aus ** Veröffentlichen Arbeitsbereich **.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.
7.  Wählen Sie den Kreditorenzusammenarbeit ** ** Arbeitsbereich aus. Sie werden auf der nächsten Seite.

![Kreditor-Zusammenarbeit-MobileApp( [] . /media/vendor-collaboration-mobile-app.png)]". /media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakte
** Die Kontakte ** Seite können Sie alle Kontakte angezeigt, die für das Kreditorenkonto eingerichtet wurden. Sie gibt den Kontaktpersonennamen, E-Mail und die primäre der Benutzeralias an, falls verfügbar. Sie enthält außerdem an, ob das aktiv Benutzerkonto der Kontaktperson ist. Für wenn Sie einen Kontakt aus, finden Sie Kontaktdetails, wie juristischen Personen die Person ein Kontakt ist, und Kontaktinformationen wie Telefonnummer oder eine andere E-Mail-Adresse.

## <a name="user-requests"></a>Benutzeranforderungen
** Die Benutzeranforderungen ** Seite können Sie alle Benutzeranforderungen finden, die Sie zur Kreditorenzusammenarbeitweboberfläche übermittelt wurde und dem Status folgen. Wenn Sie eine Benutzeranforderung auswählen, wird angezeigt, was angefordert wurde, hinzufügen oder einen Benutzer deaktivieren, ändern und Sicherheit finden, welche für den Benutzer Sicherheitsrollen angefordert wurden.

## <a name="purchase-orders-ready-for-review"></a>Bestellungen werden zur Prüfung
** Die Bestellungen zur Prüfung bereit ** Seite können Sie alle Bestellungen anzeigen, die vom Debitor gesendet wurden und nicht beantwortet wurden. Sie können ausgewählte Informationen zum Auftrag, z den Produkte angefordert wurden und wann anzeigen enthält. Preisangaben sind nur verfügbar, wenn dieses für den Lieferanten konfiguriert ist.  

Sie können anzeigen, ob die Bestellung Hinweise oder Anhänge hat. Wenn Sie Anlagen zu öffnen, müssen Sie Kreditorenzusammenarbeit im Webclienten verwenden. Wählen Sie aus ** ** Bestellposition um alle Positionen mit Details anzuzeigen. Notieren Sie das für jede Position, stellt ein Indikator angezeigt, ob es Hinweise oder Anhänge gibt, oder wenn es gibt eine Lieferadresse, die von der abweicht, der im Kopf wird angezeigt.  

Um auf die Bestellung zu antworten, müssen Sie den Kreditorenzusammenarbeitwebclienten verwenden.

## <a name="awaiting-customer-action"></a>Debitorenaktivität ausstehend
** Die zu Debitorenaktivität ** Seite können Sie Bestellungen suchen, die Sie einer oder in Ihrem Unternehmen, das auch Zugriff der Kreditoren, an zusammenarbeit hat geantwortet wurde. Die Bestellungen sind in dieser Liste nur angezeigt, wenn der Debitor eine der folgenden Aktionen auf der Bestellung ausgeführt werden muss.

-   Wenn die Bestellung abgelehnt wurde, übersteigt der entweder den Debitor übermittelten Auftrag aktualisieren und erneut übermitteln müssen, oder ziehen Sie den Auftrag storniert und übermitteln Sie erneut. Wenn die Bestellung erneut übermittelt wird, wird sie von der Debitorenaktivität ** zu ** Seite.
-   Wenn die Bestellung mit Änderungen akzeptiert wurde, übersteigt der Debitor den ursprünglichen Auftrag aktualisieren und erneut zur Prüfung übermittelt werden müssen, oder aktualisieren Sie diese über den die Änderungen und bestätigen Sie sie sofort. In beiden Fällen wird die Bestellung vom Debitorenaktivität ** zu ** Seite.
-   Wenn die Bestellung wurde angenommen und in der Debitorenaktivität ** zu ** Seite erscheint, ist sie, da die Bestellung automatisch nicht bestätigt wurde, als das Akzeptieren ausgeführt wurde. Es wurde ein Einkaufsvertreter wird, um den Auftrag auf den Status "Bestätigt" zu ändern. Normalerweise wird die Bestellung als eine Vereinbarung zwischen dem Debitor und dem Kreditor betrachtet, sobald der Kreditor den Auftrag zulässig ist. Die Bestellung dem bestätigten Bundesland zu verschieben kann eine Formalität sein.

Indem die Bestellung auszuwählen, werden zusätzliche Details zur Antwort. Sie können die und Positionsdetails die Antwort für jede Position anzeigen. Der Positionsstatus erfahren hier, welcher der folgenden Antworten gegeben war.

-   Angenommen
-   Verweigert
-   Mit Änderungen akzeptiert
-   Ersetzt/Ersatz
-   Teilen in Planung/in Planung position

Beachten Sie, dass ein Indikator ** liefernd ** =yes/no anzeigt, das verwendet wird, um anzugeben, dass die Positionen nicht geliefert werden. Hierbei kann, da die Position wurde abgelehnt, oder ersetzt, woher die ursprünglichen Positionen nicht erwartet werden zu liefernde, oder eine Position, die in mehreren Zeitplanpositionen und in die ursprüngliche Position aufgeteilt wurde, wird nicht erwartet, geliefert werden, z in eingegangenen Auftrag angefordert wurde.  

Sämtliche Änderungen, die der Auftragspositionsantwort vorgenommen werden, werden, mit Ausnahme hochgeladenen und Hinweisen den Anlagen angezeigt, die Sie sehen können, indem Sie die Kreditorenzusammenarbeitweboberfläche verwenden.

## <a name="open-confirmed-orders"></a>Open bestätigte Aufträge
Wenn die Bestellung vom Debitor bestätigt wird, bedeutet, der der Bestellung dem bestätigten Bundesland geändert wird, wird sie in offenen bestätigten Auftrag. Sie muss in der Liste, bis sie registriert ist, wenn dies vom Debitor erhalten.


