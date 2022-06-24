---
title: Einen Standarddebitoren erstellen
description: In diesem Artikel wird beschrieben, wie Sie einen Standarddebitoren erstellen, der beim Erstellen eines Kanals in Microsoft Dynamics 365 Commerce verwendet wird.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b4658356e268d045fcb7065b397411ffc5161864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894528"
---
# <a name="create-a-default-customer"></a>Einen Standarddebitoren erstellen

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie einen Standarddebitoren erstellen, der beim Erstellen eines Kanals in Microsoft Dynamics 365 Commerce verwendet wird.

Wenn Sie einen Channel anlegen, müssen Sie einen Standardkunden angeben. Ein Standardkunde kann einfach erstellt werden, nachdem zuerst die Kundengruppe und das Kundenadressbuch erstellt wurden.

## <a name="create-a-customer-group"></a>Eine Debitorengruppe erstellen

Wenn noch keine Debitorengruppen vorhanden sind, können Sie eine erstellen. Beispiele können Gruppen sein, um verschiedene Kundengruppen darzustellen, z. B. Großhandel, Einzelhandel, Internet, Mitarbeiter usw.

Gehen Sie folgendermaßen vor, um eine Debitorengruppe zu erstellen.

1. Wechseln Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Debitoren \> Debitorengruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Feld **Debitorengruppe** eine Debitorengruppenkennung ein.
1. Geben Sie im Feld **Beschreibung** eine entsprechende Beschreibung ein.
1. Geben Sie im Feld **Zahlungsbedingungen** einen entsprechenden Wert ein.
1. Geben Sie in das Feld **Zeit zwischen Rechnungsfälligkeitsdatum und Zahlungsdatum** einen geeigneten Wert ein.
1. Geben Sie im Feld **Standardsteuergruppe** eine Steuergruppe ein.
1. Aktivieren Sie gegebenenfalls das Kontrollkästchen **Preise inkl. Mehrwertsteuer**.
1. Geben Sie ggf. im Feld **Standardabschreibungsgrund** einen geeigneten Wert ein.

Das folgende Bild zeigt mehrere konfigurierte Kundengruppen.

![Debitorengruppen.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Ein neues Debitorenadressbuch erstellen

Ein Debitor muss mit einem Adressbuch verknüpft sein. Wenn noch keins erstellt wurde, müssen Sie eins erstellen.

Gehen Sie folgendermaßen vor, um ein Adressbuch zu erstellen.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Kanaleinrichtung \> Adressbücher**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie im Kästchen **Name** einen Namen ein.
1. Geben Sie im Kästchen **Beschreibung** eine Beschreibung ein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt ein Beispiel für ein Adressbuch.

![Adressbuch.](media/address-book.png)

## <a name="create-a-default-customer"></a>Einen Standarddebitoren erstellen

Gehen Sie folgendermaßen vor, um einen Standarddebitor zu erstellen.

1. Wechseln Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Debitoren \> Alle Debitoren**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie in der Dropdownliste **Typ** „Person“ aus.
1. Wählen Sie in der Dropdownliste **Kundenkonto** eine Kontonummer aus (z. B. „100001”).
1. Wählen Sie in der Dropdownliste **Vorname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Standard”).
1. Wählen Sie in der Dropdownliste **Zweiter Vorname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Retail”).
1. Wählen Sie in der Dropdownliste **Nachname** einen Namen aus, oder geben Sie einen Namen ein (z. B. „Debitor”).
1. Wählen Sie in der Dropdownliste **Währung** eine Währung aus, oder geben Sie eine Währung ein (z. B. „USD”).
1. Wählen Sie in der Dropdownliste **Währung** die zuvor erstellte Debitorengruppe aus.
1. Wählen Sie in der Dropdownliste **Adressbücher** ein vorhandenes Debitorenadressbuch aus.
1. Wählen **Speichern**, um den neuen Debitor zu speichern und zum Debitorendetails-Bildschirm zurückzukehren.

> [!NOTE]
> Es ist nicht erforderlich, eine Adresse für einen Standarddebitoren hinzuzufügen.

Die folgende Abbildung zeigt ein Beispiel für die Erstellung eines Debitors.

![Erstellung eines Standarddebitors.](media/default-customer-creation.png)

Das folgende Bild zeigt die Konfiguration eines Standarddebitors.

![Beispieldebitorenkonfiguration.](media/default-customer-configuration1.png)

Die meisten Standardwerte auf dem Debitorendetailsbildschirm können beibehalten werden, es sollten jedoch zwei Werte geändert werden.

1. Erweitern Sie auf dem Bildschirm mit den Kundendetails die Option **Standardwerte für Aufträge**.
1. Wählen Sie in der Dropdownliste **Site** eine vorkonfigurierte Site aus oder geben Sie sie ein.
1. Wählen Sie in der Dropdownliste **Lagerort** einen vorkonfigurierten Lagerort aus oder geben Sie einen ein.

Die folgende Abbildung zeigt ein Beispiel für die Konfiguration eines Debitors.

![Beispielkonfiguration eines Debitors.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über Kanäle](channels-overview.md)

[Kanaleinstellungen – Voraussetzungen](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
