---
title: Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen
description: In diesem Thema wird beschrieben, wie Sie eine Excel-Arbeitsmappe erstellen, damit Sie Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten können.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 73a3387d1e7251168002ff683b5b58e0c82a620c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965376"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen erstellen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Excel-Arbeitsmappe erstellen, damit Sie Einzelhandelstransaktionen in Microsoft Dynamics 365 Commerce bearbeiten können.

## <a name="overview"></a>Übersicht

Es gibt eine vordefinierte Excel-Vorlage, auf die Debitoren von verschiedenen Bereichen des Systems aus zugreifen und zum Bearbeiten und Prüfen von Einzelhandelstransaktionen verwenden können. Zu diesem Zweck können Debitoren aber auch eine benutzerdefinierte Excel-Arbeitsmappe erstellen.

## <a name="create-and-configure-an-excel-workbook"></a>Excel-Arbeitsmappe erstellen und konfigurieren

Führen Sie die folgenden Schritte aus, um eine Excel-Arbeitsmappe zu erstellen und zu konfigurieren, damit Sie Einzelhandelstransaktionen bearbeiten können.

1. Öffnen Sie Excel, und erstellen Sie eine leere Arbeitsmappe.
1. Wählen Sie auf der Registerkarte **Einfügen** **Meine Add-Ins** aus.
1. Wählen Sie im rechten Bereich den Link **Serverinformationen hinzufügen** aus.
1. Geben Sie die Server-URL ein, und wählen Sie **OK** aus.
1. Wenn die Fehlermeldung „Keine Applet-Registrierungen gefunden“ erscheint, führen Sie die folgenden Schritte aus, um das Problem zu beheben:

    1. Rufen Sie in Commerce **Systemadministration \> Setup \> Office-App-Parameter** auf.
    1. Wählen Sie im Inforegister **App-Parameter** **App-Parameter initialisieren** aus.
    1. Wählen Sie im Benachrichtigungsfeld **OK** aus.
    1. Wählen Sie im Inforegister **Registrierte Applets** **Applet-Registrierung initialisieren** aus.
    1. Wiederholen Sie bei Bedarf diese drei Schritte.

1. Wählen Sie **Entwerfen** und anschließend **Tabelle hinzufügen** aus.
1. Wählen Sie basierend auf den Daten, die geändert werden müssen, die Entitäten aus, die der Excel-Arbeitsmappe zur Bearbeitung hinzugefügt werden müssen. Verwenden Sie die folgende Tabelle als Referenz.

    | Transaktionstyp | Zu verwendende Datenentitäten |
    |------------------|----------------------|
    | Abholungstransaktionen, Onlineaufträge, asynchrone Debitorenaufträge, asynchrone Debitorenangebote | Transaktion (prüfbar), Verkaufstransaktion (prüfbar), Zahlungstransaktionen (prüfbar), Steuertransaktionen (prüfbar), Rabatttransaktionen (prüfbar), Belastungstransaktionen (prüfbar) |
    | Bankeinzahlung | Transaktion (prüfbar), Zahlungsmittelbuchungen (Bank, prüfbar) |
    | Sichere Einzahlung | Transaktion (prüfbar), sichere Zahlungsmittelbuchungen (prüfbar) |
    | Zahlungsmitteldeklaration | Transaktion (prüfbar), Zahlungsmitteldeklarationsbuchungen (prüfbar) |
    | Einnahmen, Ausgaben | Transaktion (prüfbar), Einnahmen/Ausgaben-Transaktionen (prüfbar), Zahlungstransaktionen (prüfbar) |
    | Startbetrag angeben, Zahlungsmittel entfernen, Mittelzugang, Zahlungsmittel ändern, Rechnungszahlung, Debitoreneinzahlung | Transaktion (prüfbar), Zahlungstransaktionen (prüfbar) |

    > [!NOTE]
    > Es ist wichtig, dass Sie jeder Excel-Arbeitsmappe nur eine Datenentität hinzufügen. Zusätzlich müssen alle Felder, die durch ein Schlüsselsymbol gekennzeichnet sind, der entsprechenden Arbeitsmappe hinzugefügt werden.

1. Wenden Sie nach der Konfiguration der Arbeitsmappe die erforderlichen Filter an. Vergewissern Sie sich, dass Sie auf alle Arbeitsblätter in der Datei dieselben Filter anwenden. Vermeiden Sie das Laden sehr großer Datenmengen in die Excel-Datei. Andernfalls kann die Leistung beeinträchtigt sein, sodass Excel und Ihr System möglicherweise langsamer werden. Wir empfehlen, immer „Unternehmen“ und entweder „Kontoauszugsnummer“ oder „Buchungsnummer“ als Filter für Ihre Datei zu verwenden.
1. Sobald Sie die Filter konfiguriert haben, wählen Sie **Aktualisieren** aus, um die Daten zu laden.
1. Bearbeiten Sie die erforderlichen Daten, und veröffentlichen Sie sie anschließend. Wenn die Schaltfläche **Veröffentlichen** nicht verfügbar ist, wurden der Excel-Arbeitsmappe wahrscheinlich einige Schlüsselfelder nicht hinzugefügt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Abholungs- und Bargeldverwaltungstransaktionen bearbeiten und prüfen](edit-cash-trans.md)

[Onlineauftrag und asynchrone Debitorenauftragstransaktionen bearbeiten und prüfen](edit-order-trans.md)

[Finanzdimensionen für Einzelhandelstransaktionen bearbeiten](edit-financial-dim.md)

[Einer Excel-Arbeitsmappe zum Bearbeiten von Einzelhandelstransaktionen Felder hinzufügen](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]