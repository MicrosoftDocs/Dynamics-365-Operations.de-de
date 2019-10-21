---
title: Standardkosten für Arbeit und Ausgaben konfigurieren
description: Dieses Thema erläutert, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185404"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Standardkosten für Arbeit und Ausgaben konfigurieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dieses Thema erläutert, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten. Diese Aufgabe verwendet das USSI-Dataset.

1. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Einstandspreis (Stunde)**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
4. Geben Sie im Feld **Kostenpreis** eine Zahl ein. Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeitskraftnummer, Projektnummer, Kategorie, Datum oder einer Kombination von ihnen einrichten. Es wird jeweils der Einstandspreis mit der höchsten Genauigkeit angewendet.  
5. Wählen Sie **Speichern**.
6. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Verkaufspreis (Stunde)**.
7. Wählen Sie **Neu** aus.
8. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
9. Wählen Sie im Feld **Gültig für** eine Option aus.
10. Geben Sie im Feld **Preisgestaltung** eine Zahl ein. Sie können einen Standardverkaufspreis für Stundenbuchungen oder für eine Projektkategorie einrichten. Sie können auch Verkaufspreise nach Arbeitskraftnummer, Projektnummer, Kategorie, Buchungsdatum oder einer beliebigen Kombination dieser Angaben einrichten. Der tatsächliche Verkaufspreis, der angewendet wird, wenn eine Arbeitskraft eine Buchung in die Stundenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit. Wenn also z. B. ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.  
11. Wählen Sie **Speichern**.
12. Schließen Sie die Seite.
13. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Einstandspreis (Ausgaben)**.
14. Wählen Sie **Neu** aus.
15. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
16. Geben Sie im Feld **Kostenpreis** eine Zahl ein. Mehrere können Felder ausgefüllt werden, dies ist jedoch das Minimum, das erforderlich ist, um den Datensatz zu speichern.  
17. Wählen Sie **Speichern**.
18. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Verkaufspreis (Ausgaben)**.
19. Wählen Sie **Neu** aus.
20. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
21. Wählen Sie im Feld **Gültig für** eine Option aus.
22. Geben Sie im Feld **Preisgestaltung** eine Zahl ein. Der tatsächliche Verkaufspreis, der dann angewendet wird, wenn eine Arbeitskraft Buchungen in eine Ausgabenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit. Wenn also beispielsweise ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.  
23. Wählen Sie **Speichern**.

