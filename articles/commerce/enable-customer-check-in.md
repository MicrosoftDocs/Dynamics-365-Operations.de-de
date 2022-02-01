---
title: Kunden-Check-in-Benachrichtigungen im Point of Sale (POS) aktivieren
description: Dieses Thema beschreibt, wie Sie in Point of Sale (POS) Microsoft Dynamics 365 Commerce Check-In-Benachrichtigungen für Debitor aktivieren können.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 95b4e3a1750cf072db919492f7445e87654701da
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983160"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Kunden-Check-in-Benachrichtigungen im Point of Sale (POS) aktivieren

[!include [banner](includes/banner.md)]

Dieses Thema beschreibt, wie Sie in Point of Sale (POS) Microsoft Dynamics 365 Commerce Check-In-Benachrichtigungen für Debitor aktivieren können.

Unternehmen können in ihren „Bestellung bereit zur Abholung“-E-Mails einen Link oder eine Schaltfläche bereitstellen, mit dem/der der Debitor dem Geschäft mitteilen kann, dass er auf dem Gelände ist und darauf wartet, dass sein Paket zu ihm gebracht wird. Der Debitor erhält dann eine Check-in-Bestätigung, und die Filiale erhält eine Benachrichtigung als Aufgabe in ihrer POS-Anwendung. Diese Aufgabe dient als Aufforderung an einen Vertriebsmitarbeiter, den Auftrag an das Fahrzeug des Debitors zu liefern. Daher muss der Debitor den Laden nicht betreten.

Der Workflow für das Einchecken des Debitors kann auch so konfiguriert werden, dass zusätzliche Informationen vom Debitor erfasst werden, z. B. die Parkplatznummer, Marke, Modell und Farbe des Fahrzeugs sowie Lieferanweisungen. Der Verkäufer kann diese Informationen verwenden, um die Auftragserfüllung zu erleichtern.

## <a name="enable-customer-check-in"></a>Aktivieren Sie den Kunden-Check-in

Wenn die Funktion zum Einchecken des Debitors eingeschaltet ist, generiert Commerce eine Auftragsbestätigungs-ID (auch bekannt als Kanalreferenz-ID). Es generiert auch Auftragsbestätigungs-IDs für Aufträge, die über Point of Sale (POS) oder Call-Center-Kanäle erstellt werden. 

Um die Funktion zum Einchecken von Debitor in der Commerce-Zentrale zu aktivieren, führen Sie diese Schritte aus.

1. Wechseln Sie zu **Arbeitsbereiche \> Verwaltung von Funktionen**.
2. Suchen Sie nach der Funktion **Kanalübergreifend ein konsistentes Kanalreferenz-ID-Format generieren**. 
3. Wählen Sie die Funktion aus und wählen Sie dann **Jetzt aktivieren** im Eigenschaftenfenster. 

## <a name="create-a-check-in-confirmation-page"></a>Erstellen Sie eine Check-in-Bestätigungsseite

Auf Ihrer E-Commerce-Site müssen Sie eine neue Seite erstellen, die als Check-in-Bestätigung dienen soll. Durch zusätzliche Konfiguration kann die Seite auch ein Formular enthalten, das zusätzliche Informationen vom Debitor sammelt, um die Auftragsabwicklung zu erleichtern. Informationen zum Festlegen der Seite und des Moduls finden Sie unter [Modul zum Einchecken von Kunden](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Konfigurieren Sie die E-Mail-Vorlage für die Transaktion

Sie müssen einen **Ich bin hier**-Link oder eine Schaltfläche in die Vorlage für die Transaktions-E-Mail einfügen, die Debitor erhält, wenn seine Bestellung zur Abholung bereit ist. Über diesen Link oder diese Schaltfläche benachrichtigt der Debitor die Filiale, dass er angekommen ist, um seine Bestellung zu entnehmen. 

Fügen Sie der Vorlage den Link oder die Schaltfläche hinzu, der/die dem Meldungstyp **Verpackung abgeschlossen** und der Lieferart zugeordnet ist, die Sie für die Auftragsabwicklung an der Bordsteinkante verwenden. Erstellen Sie in der Vorlage einen HTML-Link oder eine Schaltfläche, die auf die URL der von Ihnen erstellten Check-in-Bestätigungsseite verweist und die Parameternamen und -werte enthält, wie im folgenden Beispiel gezeigt.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Weitere Informationen zur Konfiguration von E-Mail-Vorlagen finden Sie unter [Anpassen von Transaktions-E-Mails nach Versandart](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Eine Check-in-Bestätigungsaufgabe wird in POS erstellt

Nachdem ein Kunde dem Geschäft mitgeteilt hat, dass er zur Abholung anwesend ist, zeigt die Check-in-Seite eine Bestätigungsnachricht und einen optionalen QR-Code an, der die Bestellbestätigungs-ID des Kunden enthält. Gleichzeitig wird in der Aufgabenliste im POS eine Aufgabe für die Filiale erstellt, in der der Kunde die Bestellung abholt. Diese Aufgabe enthält alle Debitor- und Auftragsinformationen, die zur Erfüllung des Auftrags erforderlich sind. Das Anleitungsfeld der Aufgabe zeigt alle Informationen an, die vom Debitor über das Formular für zusätzliche Informationen erfasst wurden.

## <a name="end-to-end-testing"></a>End-to-End-Tests

Für den Kunden-Check-in müssen bestimmte Parameter und Werte an die Check-in-Seite und dann an die Kunden-Check-in-API übergeben werden. Daher ist es am einfachsten, die Funktion in einer Umgebung zu testen, in der eine Testbestellung erstellt und gepackt werden kann. Auf diese Weise kann eine „Bestellung bereit zur Abholung“-E-Mail generiert werden, die eine URL enthält, die die erforderlichen Parameternamen und -werte enthält.

Gehen Sie folgendermaßen vor, um die Kunden-Check-in-Funktion zu testen.

1. Erstellen Sie die Kunden-Check-in-Seite, und fügen Sie dann das Kunden-Check-in-Modul hinzu und konfigurieren Sie es. Weitere Informationen finden Sie unter [Check-in für das Pickup-Modul](check-in-pickup-module.md). 
1. Laden Sie die Seite hoch, aber veröffentlichen Sie sie nicht.
1. Fügen Sie den folgenden Link zu einer E-Mail-Vorlage hinzu, die von der Benachrichtigungsart „Verpackung abgeschlossen“ für die Abholungslieferart aufgerufen wird. Weitere Informationen finden Sie unter [E-Mail-Vorlagen für Transaktionsereignisse erstellen](email-templates-transactions.md).

    - **Für Vorproduktionsumgebungen (UAT):** Fügen Sie den Codeausschnitt aus dem Abschnitt [Konfigurieren der Transaktions-E-Mail-Vorlage](#configure-the-transactional-email-template) weiter oben in diesem Thema hinzu.
    - **Für Produktionsumgebungen:** Fügen Sie den folgenden kommentierten Code hinzu, damit bestehende Kunden nicht betroffen sind.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Erstellen Sie eine Bestellung, in der die Abholungslieferart angegeben ist.
1. Wenn Sie die E-Mail erhalten, die durch den Benachrichtigungstyp „Verpackung abgeschlossen“ ausgelöst wird, testen Sie den Check-in-Vorgang, indem Sie die Check-in-Seite öffnen, die die zuvor hinzugefügte URL enthält. Da die URL die `&preview=inprogress`-Markierung enthält, werden Sie aufgefordert, sich zu authentifizieren, bevor Sie die Seite anzeigen können.
1. Geben Sie eine beliebige zusätzliche Information ein, die erforderlich ist, um das Modul zu konfigurieren.
1. Vergewissern Sie sich, dass die Ansicht der Check-in-Bestätigung richtig angezeigt wird.
1. Öffnen Sie ein POS-Terminal für den Shop, bei dem die Bestellung abgeholt wird.
1. Wählen Sie die Kachel **Bestellungen zum Abholen** aus, und überprüfen Sie, ob die Bestellung angezeigt wird.
1. Stellen Sie sicher, dass alle zusätzlichen Informationen, die im Check-in-Modul konfiguriert wurden, im Detailbereich angezeigt werden.

Nachdem Sie sich vergewissert haben, dass die Kunden-Check-in-Funktion vollständig funktioniert, führen Sie diese Schritte aus.

1. Veröffentlichen Sie die Check-in-Seite.
1. Wenn Sie in einer Produktionsumgebung testen, kommentieren Sie die URL in der E-Mail-Vorlage „Bestellung bereit zur Abholung“ aus, damit der **Ich bin hier**-Link oder die Schaltfläche angezeigt wird. Laden Sie dann die Vorlage erneut hoch.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Scheck für Abholmodul](check-in-pickup-module.md)

[Transaktions-E-Mails nach Lieferart anpassen](customize-email-delivery-mode.md)

[Mail-Vorlagen für Transaktionsereignisse erstellen](email-templates-transactions.md)
