---
title: Kunden-Check-in-Benachrichtigungen im Point of Sale (POS) aktivieren
description: Dieses Thema beschreibt, wie Sie in Point of Sale (POS) Microsoft Dynamics 365 Commerce Check-In-Benachrichtigungen für Debitor aktivieren können.
author: bicyclingfool
ms.date: 04/23/2021
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
ms.openlocfilehash: cf9331e1da54520787686a3f190e2ef6d150c0c10bd521919407f5e6c74551d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774582"
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

Fügen Sie der Vorlage den Link oder die Schaltfläche hinzu, der/die dem Meldungstyp **Verpackung abgeschlossen** und der Lieferart zugeordnet ist, die Sie für die Auftragsabwicklung an der Bordsteinkante verwenden. Erstellen Sie in der Vorlage einen HTML-Link oder eine Schaltfläche, die auf die URL der von Ihnen erstellten Check-in-Bestätigungsseite verweist. Hier ist ein Beispiel.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Weitere Informationen zur Konfiguration von E-Mail-Vorlagen finden Sie unter [Anpassen von Transaktions-E-Mails nach Versandart](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Eine Check-in-Bestätigungsaufgabe wird in POS erstellt

Nachdem ein Kunde die Filiale benachrichtigt hat, dass er zur Abholung anwesend ist, erhält er eine Eincheck-Bestätigung und es wird eine Aufgabe in der Aufgabenliste in POS für die Filiale erstellt, in der der Kunde die Bestellung abholt. Die Aufgabe enthält alle Debitor- und Auftragsinformationen, die zur Erfüllung des Auftrags erforderlich sind. In der Aufgabe zeigt das Anleitungsfeld alle Informationen an, die vom Debitor über das Formular für zusätzliche Informationen erfasst wurden. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Scheck für Abholmodul](check-in-pickup-module.md)
