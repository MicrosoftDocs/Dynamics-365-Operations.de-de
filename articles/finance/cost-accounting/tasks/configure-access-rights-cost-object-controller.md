---
title: Zugriffsrechte für einen Kostenobjekt-Controller konfigurieren
description: Verwenden Sie diese Prozedur, um Zugriffsberechtigungen für einen Kostenträgercontroller zu konfigurieren.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17615ff70c15789ac30223464b20ccd61a1bad55
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710629"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Zugriffsrechte für einen Kostenobjekt-Controller konfigurieren

[!include [banner](../../includes/banner.md)]

Verwenden Sie diese Prozedur, um Zugriffsberechtigungen für einen Kostenträgercontroller zu konfigurieren. Für diese Aufzeichnung wird das Demo-Datenunternehmen USP2 verwendet.


## <a name="assign-the-cost-object-controller-role"></a>Weisen Sie die Kostenträgercontroller-Rolle zu
1. Wechseln Sie zu "Systemverwaltung" > "Benutzer" > "Benutzer".
2. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise im Feld Benutzernamen mit einem Wert "Alicia".
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Rollen zuweisen
5. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
6. Klicken Sie auf "OK".

## <a name="enable-access-list-security"></a>Aktivieren Sie dke Zugriffslistensicherheit
1. Wechseln Sie zu Kostenrechnung > Dimensionen > Dimensionshierarchien.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Organisation auswählen  
3. Klicken Sie auf "Bearbeiten".
4. Wählen Sie die Option Ja im Feld Zugriffslisten-Hierarchiegebiet aus.
5. Klicken Sie auf "Hierarchie anzeigen".

## <a name="assign-access-rights-to-user"></a>Weisen Sie dem Benutzer Zugriffsberechtigungen zu
1. Klicken Sie auf "Neu".
2. Markieren Sie in der Liste die ausgewählte Zeile.
3. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Administrator aus.  
4. Wählen Sie in der Struktur Organisation\CEO\CFO\FIM'.
5. Klicken Sie auf "Neu".
6. Markieren Sie in der Liste die ausgewählte Zeile.
7. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
    * Wählen Sie Alicia aus.  
8. Klicken Sie auf "Speichern".

## <a name="enable-access-rights-in-cost-accounting"></a>Aktivieren Sie Zugriffsberechtigungen in der Kostenrechnung
1. Gehen Sie zu Kostenbuchhaltung > Einrichtung > Parameter.
2. Klicken Sie auf die Registerkarte "Allgemein".
3. Wählen Sie im Anzeigezugriff für Kostenobjektdimensionsmitglieder Ja aus.
4. Klicken Sie auf "Speichern".
5. Schließen Sie die Seite.
6. Wechseln Sie zur Kostenbuchhaltung > Einstellungs > Kostenkontrollearbeitsbereichskonfiguration.
7. Klicken Sie auf "Bearbeiten".
8. Wählen Sie "Ja" im Feld "Veröffentlichte Felder" aus.
    * Wenn Sie diese Option auf Ja setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller. Wenn Sie diese Option auf Nein setzen, können Benutzer, denen eine der Rollen zugewiesen wurde, den Bericht im Kostenkontrollerarbeitsbereich sehen: Kostenrechnungsmanager, Buchhalter, Kostenbuchhalter oder Kostenträgercontroller.    
9. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
