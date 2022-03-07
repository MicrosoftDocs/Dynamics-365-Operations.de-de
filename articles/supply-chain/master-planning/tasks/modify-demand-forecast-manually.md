---
title: 'Anleitung: Manuelles Ändern einer Bedarfsplanung'
description: In dem Thema wird beschrieben, wie Sie die Planung für einen Artikel ändern
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f48e1689d21fd0085ec38aab8f5171997fbf432
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567198"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Anleitung: Manuelles Ändern einer Bedarfsplanung

[!include [banner](../../includes/banner.md)]

Im folgenden Verfahren wird gezeigt, wie Sie die Planung für einen Artikel ändern. Diese Prozedur ist für den Produktionsplaner vorgesehen.

## <a name="modify-the-forecast-for-a-selected-item"></a>Die Planung für einen ausgewählten Artikel ändern

Um die Planung für einen ausgewählten Artikel zu ändern:

1. Gehen Sie zu **Module \> Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus. Wählen Sie den Artikel aus, für den Sie die Planung ändern möchten.
1. Öffnen Sie im Aktivitätsbereich die Registerkarte **Planen** und dann **Bedarfsplanung**.
1. Wählen Sie in der Liste eine Zeile aus. Wenn es keine Planungspositionen gibt, erstellen Sie eine neue Position, indem Sie im Aktivitätsbereich **Neu** auswählen.  
1. Geben Sie im Feld **Verkaufsmenge** eine positive Zahl ein. Diese Zahl gibt die prognostizierte Menge des Artikels wieder. Ein Fehler wird angezeigt, wenn Sie eine negative Zahl eingeben.
1. Füllen Sie bei Bedarf die anderen Felder aus.
1. Wählen Sie **Speichern** im Aktivitätsbereich aus.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Die Planung für einen oder mehrere Artikel in Microsoft Excel ändern

So ändern Sie die Planung für einen oder mehrere Artikel in Microsoft Excel:

1. Führen Sie einen der folgenden Schritte aus:
    - Öffnen Sie die Seite **Bedarfsplanung** für einen Artikel (egal welchen) wie im vorherigen Abschnitt beschrieben.
    - Wechseln Sie zu **Produktprogrammplan \> Planung \> Planung manuell eintragen \> Bedarfsplanungspositionen**.
1. Wählen Sie im Aktivitätsbereich **In Microsoft Office öffnen \> Bedarfsplanungseinträge**.
1. Wählen Sie einen Download-Speicherort aus, speichern Sie die Datei und öffnen Sie die heruntergeladene Datei in Excel.
1. Wenn Sie eine Warnung sehen, wählen Sie **Bearbeitung aktivieren**.
1. Melden Sie sich in Excel bei Supply Chain Management über den Aufgabenbereich Microsoft Dynamics an. Sie müssen sich mit der Option **Angemeldet bleiben** anmelden und Sie müssen der Datenverbindungs-App vertrauen.
1. In der Excel-Tabelle werden jetzt alle aktuellen Bedarfsplanungspositionen für Ihr Unternehmen angezeigt.  Sie können Bedarfsplanungspositionen nach Bedarf hinzufügen, löschen und bearbeiten.
1. Wählen Sie **Veröffentlichen** im Aufgabenbereich von Microsoft Dynamics, um Ihre Änderungen wieder in Supply Chain Management hochzuladen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
