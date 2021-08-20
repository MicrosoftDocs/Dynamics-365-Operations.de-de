---
title: Ein neues Lagerortlayout erstellen
description: In diesem Thema wird beschrieben, wie Informationen zu Lagerplätzen in einem Lager eingerichtet werden.
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7882d0eee1ff599ade2dacc27edaf53dc149b27f53bfe9ba490bf53fd9399a97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759574"
---
# <a name="create-a-new-warehouse-layout"></a>Ein neues Lagerortlayout erstellen

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Informationen zu Lagerplätzen in einem Lager eingerichtet werden. Dies gilt nur für Lagerorte, die mithilfe von die mithilfe der "Standardlagerung" im Modul "Lagerverwaltung" erstellt wurden, nicht für Lagerorte, die im Modul "Lagerortverwaltung" erstellt werden. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten verwenden.


## <a name="set-the-default-location-capacity"></a>Die Standardlagerplatzkapazität festlegen
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Parameter für Lager- und Lagerortverwaltung**.
2. Wählen Sie die Registerkarte **Lagerplätze** aus.
3. Geben Sie im Feld **Standardbreite** eine Zahl ein.
4. Geben Sie im Feld **Standardtiefe** eine Zahl ein.
5. Geben Sie im Feld **Standardhöhe** eine Zahl ein.
6. Wählen Sie **Speichern**.
7. Schließen Sie die Seite.

## <a name="define-the-location-name-format"></a>Das Format des Lagerplatznamens definieren
1. Wechseln Sie im Navigationsbereich zu **Module > Lagerverwaltung > Einstellungen > Lageraufschlüsselung > Lagerorte**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Lagerort** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie im Feld **Standort** den gewünschten Datensatz in der Suche aus.
6. Schalten Sie die Erweiterung des Abschnitts **Lagerplatznamen** ein/aus. Die Optionen in diesem Abschnitt definieren das Standardformat für Lagerplatznamen. In unserem Beispiel schließen wir die Gangnummer, Regalnummer und Regelbodennummer ein.  
7. Legen Sie die Option **Gang einschließen** auf **Ja** fest.
8. Legen Sie die Option **Regal einschließen** auf **Ja** fest. 
9. Geben Sie im Feld **Format** für das Regal einen Wert ein.
10. Legen Sie die Option **Regalboden einschließen** auf **Ja** fest.
11. Geben Sie im Feld **Format** für den Regalboden einen Wert ein.

## <a name="define-warehouse-locations"></a>Lagerort-Lagerplätze definieren
1. Wählen Sie im Aktivitätsbereich **Lagerort** aus.
2. Wählen Sie **Lagerplatz-Assistent** aus.
3. Wählen Sie **Weiter** aus.
4. Heben Sie die Auswahl für die Option **Ausgangsrampen** auf
5. Heben Sie die Auswahl für die Option **Sammellagerplätze** auf
6. Wählen Sie **Weiter** aus, bis die Option zur Auswahl von **Fertig stellen** angezeigt wird.
7. Schließen Sie die Seite.
8. Aktualisieren Sie die Seite.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]