---
title: "Mobilen Arbeitsbereich für die Kreditor-Kooperation für die Microsoft Dynamics 365 for Operations-App"
description: "Mit dem mobilen Arbeitsbereich für die Kreditor-Kooperation können Ihre Kreditoren hinsichtlich der Bestellungen auf dem Laufenden bleiben, die ihnen zur Genehmigung gesendet wurden und Informationen zu neuen und aktualisierten Bestellungen und Kontakten anzeigen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e19fee87dae6e5d425f36dac0db4ea89534a8510
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilen Arbeitsbereich für die Kreditor-Kooperation für die Microsoft Dynamics 365 for Operations-App

[!include[banner](../includes/banner.md)]


Mit dem mobilen Arbeitsbereich für die Kreditor-Kooperation können Ihre Kreditoren hinsichtlich der Bestellungen auf dem Laufenden bleiben, die ihnen zur Genehmigung gesendet wurden und Informationen zu neuen und aktualisierten Bestellungen und Kontakten anzeigen.

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
<td>Lesen Sie mehr über die Microsoft Dynamics 365 für operations mobile Plattform</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Mobile Plattform für Dynamics 365 for Operations</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Stellen Sie sicher, dass Sie eine Umgebung verwenden, die Microsoft Dynamics 365 for Operations Version 1611 und Microsoft Dynamics for Operations Platform Update 3 (November 2016) nutzen.</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Mobiles Gerät, auf dem die Dynamics 365 for Operations-App installiert ist</span></td>
<td><span style="color: #000000">Laden Sie die Dynamics 365 for Operations-App aus dem mobilen App Store herunter.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 4013633</td>
<td>Installieren Sie den Hotfix, um die Arbeitsbereiche zu aktivieren, die in Dynamics 365 for Operations bereitgestellt werden.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Hotfix KB 3216943</span> </span></td>
<td>Installieren Sie den Hotfix, um den mobilen Arbeitsbereich für die Kreditor-Kooperation zu aktivieren.</td>
</tr>
<tr class="even">
<td>Der Kreditorenbenutzer muss Zugriff auf die Weboberfläche für die Kreditor-Kooperation in Dynamics 365 for Operations haben und einen Keditor-Kooperationen-Benutzer einrichten.</td>
<td>Führen Sie die Schritte, die in den folgenden Themen beschrieben werden, aus, um die Weboberfläche für die Kreditor-Kooperation einzurichten und mit dieser zu arbeiten.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Nutzen der Kreditor-Kooperation für die Zusammenarbeit mit externen Kreditoren</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Benutzer für Kreditorenzusammenarbeit verwalten</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Kreditorenzusammenarbeit einrichten und verwalten</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Verwenden der Kreditor-Kooperation für Kunden in Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Überblick
Der Arbeitsbereich für die Kreditor-Kooperation hält Kreditoren über neue Bestellungen auf dem Laufenden, sodass diese neue Bestellungen im Webclient von Dynamics 365 for Operations sehen und auf diese reagieren können. 

**Hinweis:** Der mobile Arbeitsbereich sollte als Ergänzung und nicht als Ersatz der Weboberfläche für die Kreditor-Kooperation eingesetzt werden. 

Mit dem mobilen Arbeitsbereich der Kreditor-Kooperation können Kreditoren neue Bestellungen anzeigen, die ihnen zur Genehmigung übermittelt wurden. Er zeigt Bestellinformationen wie Menge und Produkte sowie das angeforderte Versanddatum an. Preisangaben sind je nach Konfiguration für den jeweiligen Kreditor verfügbar. 

Wenn sich Benutzer als Kreditor anmelden, sehen sie, auf welche Bestellungen reagiert wurde und für welche Bestellungen noch Debitorenaktivitäten ausstehen. Der Kreditor hat möglicherweise ein anderes Lieferdatum vorgeschlagen, dem der Debitor noch nicht zugestimmt hat, sodass die Bestellung auf eine Debitorenaktivität wartet. Der Kreditor sieht auch eine Liste der Bestellungen, die bestätigt aber noch nicht geliefert wurden. 

Um auf eine Bestellung zu antworten, muss der Kreditor die Weboberfläche für die Kreditor-Kooperation verwenden, die im Webclient von Dynamics 365 for Operations verfügbar ist. Dort findet der Kreditor auch zusätzliche Informationen zum Auftrag, wie Dokumentanhänge, Lieferadresse pro Position sowie Zuschläge, die dem Kreditor zugeordnet wurden. 

Mit einer speziellen Sicherheitsrolle kann sich der Kreditor Kontaktpersonen anzeigen lassen, die für ein Kreditorenkonto registriert sind. Mit der gleichen Sicherheitsrolle kann der Kreditor den Status jeder Benutzeranforderung anzeigen, die gesendet wurde. 

Das Erstellen neuer Kontakte und das Übermitteln von neuen Benutzeranforderungen muss über die Weboberfläche für die Kreditor-Kooperation erfolgen, die im Webclient von Dynamics 365 for Operations verfügbar ist. 

Mit dem mobilen Arbeitsbereich kann der Kreditor folgende Aktionen durchführen:

-   Neue Bestellungen anzeigen, die an den Kreditor gesendet wurden.
-   Bestellungen anzeigen, auf die der Kreditor reagiert hat und die auf eine Debitorenaktivität warten.
-   Bestellungen anzeigen, die bestätigt wurden aber noch nicht vollständig empfangen wurden.
-   Kontaktpersoneninformationen anzeigen, die für das Kreditorenkonto erfasst wurden (erfordert eine zusätzliche Sicherheitsrolle).
-   Informationen anzeigen und den Status einer Benutzeranforderung verfolgen, die vom Kreditor übermittelt wurde (zusätzliche Sicherheitsrolle erforderlich).

## <a name="get-started"></a>Erste Schritte
Erste Schritte auf dem mobiles Gerät:

1.  Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.
2.  Starten Sie die App auf Ihrem Gerät.
3.  Geben Sie die URL Dynamics 365 ein.
4.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
5.  Wenn Sie sich zum ersten Mal anmelden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt.

Nach der Anmeldung bei der App wird kein Arbeitsbereich angezeigt. Um die Arbeitsbereiche auf der mobilen App zu sehen, müssen Sie zuerst die gewünschten Arbeitsbereiche in Dynamics 365 for Operations-App veröffentlichen. Sie benötigen eine Systemverwaltungsberechtigung, um den Arbeitsbereich zu veröffentlichen.

1.  Starten Sie Dynamics 365 for Operations.
2.  Gehen Sie zu **ystemadministration**&gt; **Einrichten** &gt; **Systemparameter**.
3.  Wählen Sie **Mobile App verwalten**.
4.  Wählen Sie den Arbeitsbereich **Kreditor-Kooperation** für eine Veröffentlichung auf der mobilen Plattform.
5.  Wählen Sie **Arbeitsbereich veröffentlichen**.
6.  Aktualisieren Sie das Gerät, um die veröffentlichten Arbeitsbereiche anzuzeigen.
7.  Wählen Sie den Arbeitsbereich **Kreditor-Kooperation**. Sie sehen die nächste Seite.

    [![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontakte
Auf der Seite **Kontakte** werden alle Kontakte angezeigt, die für das Kreditorenkonto eingerichtet wurden. Sie zeigt den Kontaktpersonennamen, die primäre E-Mail-Adresse und den Benutzeralias an, falls verfügbar. Sie gibt zudem an, ob das Benutzerkonto der Kontaktperson aktiv ist. Wenn Sie einen Kontakt auswählen, sehen Sie Kontaktdetails, beispielsweise für welche juristischen Personen diese Person ein Kontakt ist. Zudem werden Kontaktinformationen wie Telefonnummer oder eine alternative E-Mail-Adresse angezeigt.

## <a name="user-requests"></a>Benutzeranforderungen
Auf der Seite **Benutzeranforderungen** werden all die Benutzeranforderungen angezeigt, die Sie über die Weboberfläche der Kreditor-Kooperation übermittelt haben. Sie können deren Status nachverfolgen. Wenn Sie eine Benutzeranforderung auswählen, wird angezeigt, was angefordert wurde. Sie können einen Benutzer hinzufügen oder deaktivieren, die Sicherheit ändern und anzeigen, welche Sicherheitsrollen für den Benutzer angefordert wurden.

## <a name="purchase-orders-ready-for-review"></a>Zur Überprüfung bereite Bestellungen
Auf der Seite für **Zur Überprüfung bereite Bestellungen** werden alle Bestellungen angezeigt, die vom Debitor gesendet und noch nicht beantwortet wurden. Sie können ausgewählte Informationen zum Auftrag anzeigen, beispielsweise welche Produkte angefordert wurden und wann diese geliefert werden sollen. Preisangaben sind nur verfügbar, wenn dies für den Kreditor konfiguriert ist. Sie können anzeigen, ob zur Bestellung Hinweise oder Anhänge vorhanden sind. Zum Öffnen von Anhängen müssen Sie die Kreditor-Kollaboration im Webclient verwenden. Wählen Sie **Bestellposition** aus, um alle Positionen mit Details anzuzeigen. Beachten Sie, dass ein Indikator für jede Position anzeigt, ob Hinweise oder Anhänge vorhanden sind und ob es eine Lieferadresse gibt, die sich von in der Kopfzeile angezeigten Informationen unterscheidet. Um auf die Bestellung zu antworten, müssen Sie den Kreditor-Kollaboration-Webclient verwenden.

## <a name="awaiting-customer-action"></a>Debitorenaktivität ausstehend
Auf der Seite **Debitorenaktivität ausstehend** werden die Bestellungen angezeigt, auf die Sie oder jemand aus Ihrem Unternehmen mit Zugriff auf die Kreditor-Kollaboration geantwortet haben. Die Bestellungen werden in dieser Liste nur angezeigt, wenn der Debitor eine der folgenden Aktionen für die Bestellung ausführen muss.

-   Wenn die Bestellung abgelehnt wurde, muss der Debitor entweder den gesendeten Auftrag aktualisieren und erneut senden oder den Auftrag stornieren und erneut übermitteln. Wenn die Bestellung erneut übermittelt wird, wird sie nicht mehr auf der Seite **Debitorenaktivität ausstehend** angezeigt.
-   Wenn die Bestellung mit Änderungen akzeptiert wurde, muss der Debitor den ursprünglichen Auftrag aktualisieren und zur Überprüfung erneut einsenden oder diesen entsprechend der Änderungen aktualisieren und sofort bestätigen. In beiden Fällen wird die Bestellung nicht mehr länger auf der Seite **Debitorenaktivität ausstehend** angezeigt.
-   Wenn die Bestellung angenommen wurde und auf der Seite **Debitorenaktivität ausstehend** angezeigt wird, liegt das daran, dass die Bestellung nach dem Akzeptieren nicht automatisch bestätigt wurde. In diesem Fall muss der Einkäufer den Status des Auftrags in "Bestätigt" ändern. Normalerweise wird die Bestellung als eine Vereinbarung zwischen dem Debitor und dem Kreditor betrachtet, sobald der Kreditor den Auftrag annimmt. Die Bestellung auf den Status "Bestätigt" setzen wäre reine Formsache.

Indem die Bestellung ausgewählt wird, werden weitere zusätzliche Details zur Antwort angezeigt. Sie können die Positionsdetails und die Antworten für die einzelnen Positionen anzeigen. Der Positionsstatus gibt an, welche der folgenden Antworten gegeben wurden.

-   Angenommen
-   Verweigert
-   Mit Änderungen akzeptiert
-   Ersetzt/Ersatz
-   In Zeitplan aufgeteilt/Zeitplanposition

Beachten Sie, dass ein Indikator **Wird geliefert**=ja/nein anzeigt, um anzugeben, dass die Positionen nicht geliefert werden. Ein Grund dafür kann sein, dass die Position abgelehnt wurde oder ersetzt und die ursprünglichen Positionen vermutlich nicht geliefert werden. Es kann auch sein, dass eine Position in mehrere Zeitplanpositionen aufgeteilt wurde und davon ausgegangen wird, dass die ursprüngliche Position nicht geliefert wird, so wie im empfangenen Auftrag angegeben. Sämtliche Änderungen, die an der Bestellantwortposition vorgenommen wurden, werden angezeigt. Davon ausgenommen sind hochgeladene Hinweise und Anhänge, die Sie über die Kreditor-Kollaboration-Weboberfläche anzeigen können.

## <a name="open-confirmed-orders"></a>Offene, bestätigte Aufträge
Wenn die Bestellung vom Debitor bestätigt wird und sich somit der Status in "Bestätigt" ändert, wird sie als offener, bestätigter Auftrag angezeigt. Sie bleibt in der Liste, bis sie als vom Debitor empfangen registriert wird.





