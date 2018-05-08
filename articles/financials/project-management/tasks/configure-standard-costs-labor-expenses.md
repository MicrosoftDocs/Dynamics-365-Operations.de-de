--- 
title: "Standardkosten für Arbeit und Ausgaben konfigurieren"
description: "Diese Prozedur zeigt, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 432b5b195b29fb03786cb0560e277735b531b7d7
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Standardkosten für Arbeit und Ausgaben konfigurieren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Diese Prozedur zeigt, wie Sie Standardkosten für Arbeit und Ausgaben für ein Projekt einrichten. Diese Aufgabe verwendet das USSI-Dataset.

1. Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Einstandspreis (Stunde)”.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
4. Geben Sie im Feld "Kostenpreis" eine Zahl ein.
    * Sie können einen Standardeinstandspreis für die Projektkategorie oder einen Einstandspreis nach Arbeitskraftnummer, Projektnummer, Kategorie, Datum oder einer Kombination von ihnen einrichten. Es wird jeweils der Einstandspreis mit der höchsten Genauigkeit angewendet.  
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.
7. Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Verkaufspreis (Stunde)”.
8. Klicken Sie auf "Neu".
9. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
10. Wählen Sie im Feld "Gültig für" eine Option aus.
11. Geben Sie im Feld „Preisgestaltung” eine Zahl ein.
    * Sie können einen Standardverkaufspreis für Stundenbuchungen oder für eine Projektkategorie einrichten. Sie können auch Verkaufspreise nach Arbeitskraftnummer, Projektnummer, Kategorie, Buchungsdatum oder einer beliebigen Kombination dieser Angaben einrichten. Der tatsächliche Verkaufspreis, der angewendet wird, wenn eine Arbeitskraft eine Buchung in die Stundenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit. Wenn also z. B. ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.
14. Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Einstandspreis (Ausgaben)”.
15. Klicken Sie auf "Neu".
16. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
17. Geben Sie im Feld "Kostenpreis" eine Zahl ein.
    * Mehrere können Felder ausgefüllt werden, dies ist jedoch das Minimum, das erforderlich ist, um den Datensatz zu speichern.  
18. Klicken Sie auf "Speichern".
19. Schließen Sie die Seite.
20. Wechseln Sie zu „Projektverwaltung und -buchhaltung” > „Setup” > „Preise” > „Verkaufspreis (Ausgaben)”.
21. Klicken Sie auf "Neu".
22. Geben Sie im Feld "Gültigkeitsdatum" ein Datum ein.
23. Wählen Sie im Feld "Gültig für" eine Option aus.
24. Geben Sie im Feld „Preisgestaltung” eine Zahl ein.
    * Der tatsächliche Verkaufspreis, der dann angewendet wird, wenn eine Arbeitskraft Buchungen in eine Ausgabenerfassung eingibt, ist der Verkaufspreis mit der höchsten Genauigkeit. Wenn also beispielsweise ein allgemeiner und ein arbeitskraftspezifischer Verkaufspreis eingerichtet sind, wird der arbeitskraftspezifische Verkaufspreis verwendet.  
25. Klicken Sie auf "Speichern".


