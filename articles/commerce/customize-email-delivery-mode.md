---
title: Transaktions-E-Mails nach Lieferart anpassen
description: In diesem Artikel wird beschrieben, wie Sie benutzerdefinierte E-Mail-Vorlagen für bestimmte Benachrichtigungstypen und Lieferarten in Microsoft Dynamics 365 Commerce einrichten.
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f16bc23e3527f57bd61d73e92506946067c6eeb9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850303"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Transaktions-E-Mails nach Lieferart anpassen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie benutzerdefinierte E-Mail-Vorlagen für bestimmte Benachrichtigungstypen und Lieferarten in Microsoft Dynamics 365 Commerce einrichten.

Transaktions-E-Mails können jetzt für eine Kombination eines Benachrichtigungstyps angepasst werden (z. B. **Auftrag erstellt**, **Bestellung verpackt** oder **Bestellung in Rechnung gestellt**) sowie für eine Lieferart (z. B. über Nacht, Abholung im Laden oder Abholung am Straßenrand). Mit benutzerdefinierten Transaktions-E-Mails können Einzelhändler ihre Kundenbestellung mit Erfüllungserlebnissen anbieten, die auf die Lieferart der Bestellung zugeschnitten sind. Beispielsweise kann das Ereignis „Bestellung gepackt“ so angepasst werden, dass es Anweisungen zur Abholung am Straßenrand für Kunden enthält, die sich für die Abholung am Straßenrand entscheiden. Alternativ kann es Informationen zu Spediteur und Lieferinformationen für Kunden bereitstellen, die ihren Auftrag liefern lassen möchten.

> [!NOTE]
> Um die Funktionalität für benutzerdefinierte Transaktions-E-Mails nutzen zu können, müssen Sie zuerst die Funktion **Transaktions-E-Mail-Vorlagen nach Zustellungsart anpassen** aktivieren, indem Sie in der Commerce-Zentralverwaltung zu **Arbeitsbereiche \> Funktionsverwaltung** wechseln.

E-Mails können je nach Lieferart für die folgenden Benachrichtungstypen angepasst werden:

- **Auftragsstornierung** – Dieser E-Mail-Benachrichtigungstyp ist neu.
- **Auftrag erstellt**
- **Auftrag bestätigt**
- **Auftrag fakturiert** – Dieser E-Mail-Benachrichtigungstyp ist neu. Er kann anstelle des Benachrichtigungstyps **Auftrag gesendet** verwendet werden, wodurch eine Benachrichtigung für jedes Rechnungsereignis gesendet wird, das die Lieferart Gesendet (nicht Abholung, Mitnehmen oder elektronische Lieferart) hat.
- **Auftrag entnommen**
- **Auftrag verpackt**
- **Auftrag zur Abholung bereit** – Dieser Benachrichtigungstyp kann nur dann nach Lieferart angepasst werden, wenn die Funktion **Unterstützung für mehrere Lieferarten** aktiviert ist. In diesem Fall entspricht dieser Benachrichtigungstyp funktional dem Benachrichtigugnstyp **Auftrag verpackt**.
- **Zahlung fehlgeschlagen**
- **Ersatzauftrag erstellt**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>E-Mail-Vorlagen für bestimmte Lieferarten konfigurieren

Bei diese Prozedur wird davon ausgegangen, dass Sie bereits Ihre neuen, benutzerdefinierten E-Mail-Vorlagen erstellt und sie der Seite **E-Mail-Vorlagen der Organisation** hinzugefügt haben. Informationen zum Erstellen und Hochladen von E-Mail-Vorlagen finden Sie unter [E-Mail-Vorlagen für Transaktionsereignisse erstellen](email-templates-transactions.md).

Führen Sie die folgenden Schritte aus, um E-Mail-Vorlagen für bestimmte Lieferarten in der Commerce-Zentralverwaltung zu konfigurieren.

1. Wechseln Sie zum **Commerce-E-Mail-Benachrichtigungsprofil**.
1. Unter **Einstellungen für Retail-Ereignisbenachrichtigungen** wählen Sie einen vorhandenen Benachrichtigungstyp aus.
1. Während der Benachrichtigungstyp noch ausgewählt ist, wählen Sie **Lieferarten konfigurieren** aus.
1. Wählen Sie im Dialogfeld **Lieferarten** die Option **Neu** aus.
1. Wählen Sie in der neuen Zeile im Feld **Lieferart** eine Lieferart aus.
1. Im Feld **E-Mail-ID** wählen Sie die E-Mail-Vorlage aus, die der Lieferart zugeordnet werden soll.
1. Aktivieren Sie das Kontrollkästchen **Aktiv**.
1. Wiederholen Sie die Schritte 4 bis 7, um weitere Lieferarten hinzuzufügen.
1. Wählen Sie abschließend **OK** aus.

> [!NOTE]
> - Wenn in verschiedenen Positionen in einem Auftrag mehr als eine Lieferart vorhanden sind, wird die Standardvorlage verwendet. Die Standardvorlage ist die Vorlage, die dem Benachrichtigungstyp auf der Seite **Commerce-E-Mail-Benachrichtigungsprofil** zugeordnet ist.
> - Wenn ein Auftrag eine Lieferart hat, die nicht für eine benutzerdefinerte E-Mail-Vorlage konfiguriert wurde, wird die standardmäßige E-Mail-Vorlage verwendet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Callcenteraufträge erstellen](tasks/create-call-center-orders.md)

[Lieferart in POS ändern](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]