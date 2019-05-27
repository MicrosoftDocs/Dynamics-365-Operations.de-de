---
title: Österreich
description: Dieses Thema bietet eine Übersicht der Dynamics 365 for Finance and Operations-Funktionen, die für Österreich spezifisch sind.
author: ShylaThompson
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1c532d10aa82a57d11eb2f2a7d7252a0f475cacd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537761"
---
# <a name="austria"></a>Österreich

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen und Verknüpfungen zu Ressourcen, mit deren Hilfe Sie Dynamics 365 for Finance and Operations für juristische Personen mit primärer Adresse in Österreich einrichten können.

## <a name="depreciation"></a>Abschreibung

Bei Unternehmen in Österreich werden die Abschreibung für zusätzliche Anschaffungen und Anschaffungsänderungen gemäß den folgenden Regeln berechnet: Weitere Informationen finden Sie unter [Halbjährliche Abschreibung auf zusätzlichen Anschaffungen](emea-aut-half-year-depreciation.md).

## <a name="packing-material-fees"></a>Verpackungsmaterialgebühren

In Österreich werden Verpackungsmaterialien in verschiedene Kategorien gruppiert z. B. und Haushalt und Kommerz. Die Verwaltung gibt Steuersätze für Verpackungsmaterialien für jede einzelne Kategorie an. Die Kategorie, in die das Verpackungsmaterial gehört, hängt von der Größe und den Produkten ab, die für die Verpackung verwendet wurde. Verpackungsmaterialgebühren werden kalkuliert und erfasst, es werden jedoch keine Sachkontobuchungen ausgeführt, da die Gebühren nicht als Steuern betrachtet werden, die an eine Behörde zu entrichten sind. Weitere Informationen finden Sie unter [Verpackungsmaterialgebühr](emea-aut-packing-material-fee-calculation.md).

## <a name="purchase-duties"></a>Einkaufsaufgaben

Bei der Einkaufssteuer handelt es sich um eine Steuer auf die eingehende Mehrwertsteuer. Sie wird als prozentualer Anteil der gezahlten Mehrwertsteuer berechnet. Dieser Abschnitt umfasst Informationen zu Einkaufssteuern für juristische Personen mit primärer Adresse in Österreich. Weitere Informationen über die globale Mehrwertsteuerfunktionen finden Sie im [Mehrwertsteuerüberblick](../general-ledger/indirect-taxes-overview.md).

Die Berechnung der Einkaufssteuern basiert auf Mehrwertsteuercodes. Um einen Mehrwertsteuercode in die Einkaufssteuerberechnung einzubeziehen, aktivieren Sie das Kontrollkästchen **Einkaufssteuer** auf der Seite **Mehrwertsteuercodes**. 

Sie können Einkaufssteuereinstellungen im Menü **Steuereinstellungen** auf der Seite **Einkaufssteuer** angeben. Sie können den Bezeichner für Berechtigungen (beispielsweise **KU**), Beschreibung, Steuerbehörde und Konten, die für die Buchung verwendet werden, festlegen Das Steuerkonto ist ein Bilanzkonto, in dem die Verbindlichkeiten für die Einkaufssteuer erfasst werden. Das Kostenkonto ist ein Gewinn- und Verlustkonto, auf dem die Kosten gebucht werden, und ein Ausgleichskonto, wo Ausgleichstransaktionen generiert werden.

Um den Wert der Einkaufssteuer anzugeben, klicken Sie auf **Einkaufssteuerwert**, um die Seite **Einkaufssteuerwert** zu öffnen. Sie können den Einkaufssteuersatz in Prozent ( z. B. **0.30**) für den erforderlichen Zeitraum angeben.

Einkaufssteuern werden generiert, wenn Sie die Mehrwertsteuer ausgleichen und buchen. Sie können den Bericht **Einkaufssteuer** im Menü **Einkaufssteuererklärung** generieren.

## <a name="vat"></a>MwSt.
Informationen zum Einrichten des Mehrwertsteuer (VAT)- Auszugs für juristische Personen in Österreich, finden Sie unter [Mehrwertsteuerbeitreibung für Österreich](emea-aut-vat-statement-details.md). 

Weitere Informationen zu den Einstellungen des MwSt. -Auszugs finden Sie unter [MwSt Bericht](emea-vat-reporting.md).

## <a name="reports-for-austria"></a>Berichte für Österreich

| Bericht                     | Bericht abrufen | Weitere Informationen                 |
|----------------------------|--------------------------|----------------------------------------|
|Bericht "Grenzüberschreitende Dienstleistungen"|**Hauptbuch** > **Berichte** > **Extern** > **Grenzüberschreitende Dienstleistungen**|Mit diesem Bericht wird eine Zusammenfassung der eingehenden und ausgehenden grenzübergreifenden Dienstleistungen, der Länder, die Anbieter oder Empfänger grenzübergreifender Dienstleistungen sind, sowie Nettobeträge, die für die Dienstleistungen bezahlt werden, gedruckt. Dieser Bericht wird in der Regel von Buchhaltungsleitern, Buchhaltern und Vertriebsleitern verwendet, um sich über den Status von Verkaufstransaktionen zu erkundigen. |


## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Microsoft Dynamics-Lokalisierungs-Portal: Österreich-Bericht](https://mbs.microsoft.com/files/customer/AX/Support/supportnews/Austria.html)
- [Überblick über die elektronische Berichterstellung](../../dev-itpro/analytics/general-electronic-reporting.md)
- [Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
