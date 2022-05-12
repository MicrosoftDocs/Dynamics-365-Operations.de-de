---
title: Power BI-Inhalt zur Abonnementabrechnung
description: In diesem Thema wird beschrieben, was im Microsoft Power BI-Inhalt zur Abonnementabrechnung enthalten ist.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: fad96bdaf60e7772e9ea1ff937435b0274303505
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645419"
---
# <a name="subscription-billing-power-bi-content"></a>Power BI-Inhalt zur Abonnementabrechnung

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, was im Microsoft Power BI-Inhalt zur Abonnementabrechnung enthalten ist. Es erläutert, wie Sie auf die Power BI-Berichte zugreifen, und enthält Informationen zum Datenmodell und zu den Entitäten, die verwendet wurden, um den Inhalt zu erstellen. 

## <a name="overview"></a>Übersicht

Der Power BI-Inhalt zur Abonnementabrechnung wurde für Sachbearbeiter und Manager für Abonnementabrechnung erstellt. Er bietet wichtige Abonnementabrechnungsmetriken, wie z. B. monatlich wiederkehrende Umsatzerlöse (MRR) für Abrechnungszeitpläne und Informationen zum Restwert und Wasserfall für Stundungszeitpläne. Er verwendet die Daten aus den Abrechnungszeitplänen und Stundungszeitplänen, um einen Überblick über wiederkehrende Einnahmen und Umsatzerlöse zu geben.

Der Power BI-Inhalt verfügt über die folgenden drei Registerkarten, die insgesamt vier Analyseberichte bereitstellen: 

- **Analyse – MRR** – Diese Registerkarte enthält die Berichte **Monatlich wiederkehrende Abrechnung** und **Abrechnungszeitplandetails**.
- **Analyse – Wasserfall** – Diese Registerkarte enthält den Bericht **Umsatzerlöswasserfall**.
- **Analyse – Restwert** – Diese Registerkarte enthält den Bericht **Restwert**.

## <a name="view-data-on-the-analytical-reports"></a>Daten in Analyseberichten anzeigen

Bevor Sie Daten zu den Analyseberichten anzeigen können, müssen Sie einen regelmäßigen Prozess ausführen, der die Berichtsdaten für jeden Bericht generiert. Diese für die Berichte erforderlichen Daten müssen generiert werden, da sie nicht direkt in der Datenbank gespeichert werden. 

1. Gehen Sie zu **Abonnementabrechnung \> Wiederkehrende Vertragsabrechnung \> Periodische Aufgaben \> Batchverarbeitung für MRR-Analysebericht** und befolgen Sie diese Schritte:

    1. Geben Sie einen Zeitraum von maximal drei Jahren ein.
    2. Optional: Richten Sie einen wiederkehrenden Stapelverarbeitungsprozess ein, um die Daten regelmäßig zu aktualisieren.
    3. Wählen Sie **OK** aus.

2. Nachdem der Batchauftrag ausgeführt wurde, gehen Sie zu **Systemverwaltung \> Einrichtung \> Entitätsspeicher** und aktualisieren Sie die aggregierte Messung **MRR-Bericht**. 
3. Gehen Sie zu **Abonnementabrechnung \> Umsatzerlös- und Ausgabenstundungen \> Periodische Aufgaben \> Batchverarbeitung für Wasserfallanalysebericht** und befolgen Sie diese Schritte:

    1. Geben Sie ein Startdatum und ein Enddatum ein, die nicht mehr als 26 Zeiträume umfassen. 
    2. Wenn Sie die prognostizierte Menge vergangener Zeiträume im aktuellen Zeitraum anzeigen möchten, stellen Sie die Option **Vergangene Beträge für aktuellen Zeitraum planen** auf **Ja**.
    3. Optional: Richten Sie einen wiederkehrenden Stapelverarbeitungsprozess ein, um die Daten regelmäßig zu aktualisieren.
    4. Wählen Sie **OK** aus. 

4. Nachdem der Batchauftrag ausgeführt wurde, gehen Sie zu **Systemverwaltung \> Einrichtung \> Entitätsspeicher** und aktualisieren Sie die aggregierte Messung **Wasserfallbericht**.
5. Gehen Sie zu **Abonnementabrechnung \> Umsatzerlös- und Ausgabenstundungen \> Periodische Aufgaben \> Batchverarbeitung des Restwertanalyseberichts** und befolgen Sie diese Schritte:

    1. Geben Sie ein Startdatum und ein Enddatum ein, die nicht mehr als 26 Zeiträume umfassen. 
    2. Wenn Sie die prognostizierte Menge vergangener Zeiträume im aktuellen Zeitraum anzeigen möchten, stellen Sie die Option **Vergangene Beträge für aktuellen Zeitraum planen** auf **Ja**.
    3. Optional: Richten Sie einen wiederkehrenden Stapelverarbeitungsprozess ein, um die Daten regelmäßig zu aktualisieren.
    4. Wählen Sie **OK** aus.

6. Nachdem der Batchauftrag ausgeführt wurde, gehen Sie zu **Systemverwaltung \> Einrichtung \> Entitätsspeicher** und aktualisieren Sie die aggregierte Messung **Restwertbericht**.

## <a name="accessing-the-power-bi-content"></a>Zugreifen auf den Power BI-Inhalt

Der Power BI-Inhalt zur Abonnementabrechnung wird im Arbeitsbereich **Abonnementabrechnung** angezeigt.
