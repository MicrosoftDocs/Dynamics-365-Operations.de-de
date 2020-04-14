---
title: Einrichten von Mehrwertsteuerbehörden
description: Mehrwertsteuerbehörden sind Entitäten, an welche die eingezogene Mehrwertsteuer gemeldet und abgeführt werden muss.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc6aeb39591c68cae78537faa077010d68628b02
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144765"
---
# <a name="set-up-sales-tax-authorities"></a>Einrichten von Mehrwertsteuerbehörden

[!include [banner](../../includes/banner.md)]

Mehrwertsteuerbehörden sind Entitäten, an welche die eingezogene Mehrwertsteuer gemeldet und abgeführt werden muss. Sie können die Mehrwertsteuer direkt an die Behörde abführen oder mittels eines für die Mehrwertsteuerbehörde erstellten Kreditorenkontos. Dies ermöglicht dem Unternehmen die Verwendung der normalen Zahlungsroutinen zum Abführen der Mehrwertsteuer an die Mehrwertsteuerbehörde und gewährleistet eine pünktliche Zahlung. Wird die Steuerbehörde nicht als Kreditor eingerichtet, muss am korrekten Fälligkeitsdatum eine manuelle Zahlung an die Steuerbehörde vorbereitet werden. Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuerbehörden".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Behörde" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Kreditorenkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Wählen das Berichtslayout für das Land/die Region aus (sofern verfügbar). Wenn die Berichtslayouts nicht den Anforderungen der Mehrwertsteuerbehörde entsprechen, verwenden Sie das Standardlayout.
9. Geben Sie Werte im Formular "Rundung" und in den Feldern "Rundung" ein, um anzugeben, wie der zu zahlende Gesamtsteuerbetrag gerundet werden soll. Alle Rundungsdifferenzen werden zu "Konten für automatische Buchungen" gebucht, die im "Hauptbuch" eingerichtet sind.
10. Geben Sie im Feld "Rundung" eine Zahl ein.
11. Klicken Sie auf "Speichern".

