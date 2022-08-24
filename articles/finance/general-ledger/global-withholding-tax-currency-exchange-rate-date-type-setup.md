---
title: Die globale Einrichtung des Währungswechselkurstyps der Quellensteuer und des Datumstyps aktivieren
description: In diesem Artikel wird erläutert, wie Sie die globale Einrichtung des Währungswechselkurstyps der Quellensteuer und des Datumstyps aktivieren.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 41f12a33651c14439f3a59c5c2f2d34019dada2d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229958"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Die globale Einrichtung des Währungswechselkurstyps der Quellensteuer und des Datumstyps aktivieren

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

In diesem Artikel wird erläutert, wie Sie die globale Einrichtung des Währungswechselkurstyps der Quellensteuer und des Datumstyps aktivieren. Sie können nun einen eigenen Wechselkurstyp und Wechselkursberechnungsdatumstyp für die Quellensteuerwährung auswählen. Diese Auswahlen bestimmen den Fremdwährungswechselkurs, der zur Berechnung des Quellensteuerbetrags in der Quellensteuerwährung in den Zahlungsbuchungen verwendet wird.

Diese Funktionalität ist in Microsoft Dynamics 365 Finance ab Version 10.0.29 verfügbar.

1. Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Parameter** \> **Hauptbuchparameter**.
2. Legen Sie auf der Registerkarte **Quellensteuer** die Option **Erweiterte Quellensteuerwährung aktivieren** auf **Ja**.
3. Wählen Sie im Feld **Wechselkurstyp** einen Wechselkurstyp für die Quellensteuerwährung aus.
4. Wählen Sie im Feld **Typ des Berechnungsdatums** einen Typ des Berechnungsdatums aus, der den Währungswechselkurs der Quellensteuer bestimmt:

    - **Zahlungsdatum**: Bestimmen Sie den Wechselkurs basierend auf dem Buchungsdatum der Zahlungserfassung.
    - **Rechnungsdatum**: Bestimmen Sie den Wechselkurs basierend auf dem Rechnungsdatum der Rechnungserfassung. Wenn das Rechnungsdatum des Belegs leer ist, wird das Buchungsdatum der Rechnung verwendet. 
    - **Belegdatum**: Legen Sie den Wechselkurs basierend auf dem Belegdatum der Zahlungserfassung fest. Wenn das Belegdatum des Belegs leer ist, wird das Zahlungsdatum verwendet.

5. Wählen Sie **Speichern** aus.

Weicht die Buchungswährung von der Quellensteuerwährung ab, die im Quellensteuercode hinterlegt ist, wird der Betrag in der Quellensteuerwährung anhand der vorangegangenen Einstellungen aus der Buchungswährung errechnet und in den gebuchten Quellensteuerbuchungen erfasst.
