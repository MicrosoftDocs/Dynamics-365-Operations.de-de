---
title: Intercompany-Projektrechnungsstellung konfigurieren
description: Dieses Thema zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144278"
---
# <a name="configure-intercompany-project-invoicing"></a>Intercompany-Projektrechnungsstellung konfigurieren

[!include [banner](../../includes/banner.md)]

Dieses Thema zeigt, wie die Projektfakturierung zwischen zwei Unternehmen in Ihrer Organisation eingerichtet wird. Diese Aufgabe verwendet das USSI-Dataset.

1. Wechseln Sie im Navigationsbereich zu **Module > Kreditorenkonten > Kreditoren > Alle Kreditoren**.
2. In der Liste **Alle Kreditoren** suchen Sie den gewünschten Datensatz und wählen ihn aus.
3. Wählen Sie im Aktivitätsbereich **Allgemein** aus.
4. Wählen Sie **Intercompany** aus.
5. Legen Sie **Aktiv** auf **Ja** fest, um den Intercompanyhandel zu aktivieren.
6. Geben Sie im Feld **Debitorenunternehmen** einen Wert ein oder wählen Sie einen Wert aus.
7. Geben Sie im Feld **Mein Konto** einen Wert ein oder wählen Sie einen Wert aus.
8. Wählen Sie **Speichern**.
9. Schließen Sie die Seiten, um zur Startseite zurückzukehren.
10. Gehen Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einrichtung > Projektverwaltungs- und -verrechnungsparameter**.
11. Wählen Sie die Registerkarte **Intercompany** aus.
12. Bewegen Sie den Schieberegler auf **Ja**, um die Intercompany-Ressourcenplanung und -Arbeitszeittabellen zu aktivieren.
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Wählen Sie **Neu** aus.
15. Geben Sie im Feld **Leihende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.
16. Aktivieren Sie das Kontrollkästchen **Umsatzerlös antizipieren**.
17. Geben Sie im Feld **Standard-Arbeitszeittabellenkategorie** einen Wert ein oder wählen Sie einen Wert aus.
18. Geben Sie im Feld **Standard-Ausgabenkategorie** einen Wert ein oder wählen Sie einen Wert aus.
19. Wählen Sie **Speichern**.
20. Schließen Sie die Seite.
21. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Buchung > Sachkontobuchungseinstellungen**.
22. Wählen Sie im Feld **Sachkontotypen** eine Option aus.
23. Wählen Sie **Neu** aus.
24. Geben Sie im Feld **Hauptkonto** der neuen Zeile die gewünschten Werte an.
25. Wählen Sie **Speichern**.
26. Schließen Sie die Seite.
27. Wechseln Sie im Navigationsbereich zu **Module > Projektverwaltung und -verrechnung > Einstellungen > Preise > Interner Verrechnungspreis**.
28. Wählen Sie **Neu** aus.
29. Geben Sie im Feld **Gültigkeitsdatum** ein Datum ein.
30. Geben Sie im Feld **Leihende juristische Person** einen Wert ein, oder wählen Sie einen Wert aus.
31. Wählen Sie im Feld **Verrechnungspreismodell** eine Option aus.
32. Geben Sie im Feld **Preisgestaltung** eine Zahl ein.
33. Wählen Sie **Speichern**.

