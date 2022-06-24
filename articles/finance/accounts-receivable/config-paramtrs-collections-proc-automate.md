---
title: Parameter für die Automatisierung des Inkassoprozesses konfigurieren
description: In diesem Artikel werden die Parameter beschrieben, die sich auf automatisierte Inkassoprozesse auswirken. Er bietet Anleitungen zu deren Einstellung, damit der automatisierte Prozess Ihre Absichten und Erwartungen widerspiegelt.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c5d0f801c47ef2d98d8ba410dc593bd7640839c1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900041"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Parameter für die Automatisierung des Inkassoprozesses konfigurieren

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Parameter beschrieben, die sich auf automatisierte Inkassoprozesse auswirken. Er bietet Anleitungen zu deren Einstellung, damit der automatisierte Prozess Ihre Absichten und Erwartungen widerspiegelt. Informationen zum Automatisieren von Inkassoprozessen finden Sie unter [Automatisierung des Inkassoprozesses](collections-process-automate.md).

## <a name="general"></a>Allgemeines
Geben Sie eine Zahl in **Prozentsatz der Kunden pro Batchaufgabe** ein, um die Anzahl der Batchaufgaben pro Automatisierungsprozess zu bestimmen. Legen Sie **Inkassobriefe automatisch buchen** auf **Ja** fest, damit der Aktionstyp „Inkassobrief“ den Brief während der Automatisierung bucht. Legen Sie **Aktivitäten für Automatisierungen erstellen** auf **Ja** fest, um Aktivitäten für Aktionstypen ohne Aktivität zu erstellen und zu schließen, sodass alle automatisierten Schritte angezeigt werden, die für ein Konto ausgeführt wurden. Definieren Sie die Anzahl der Tage, in denen der Inkassoverlauf in **Tage, um den Verlauf der Automatisierung des Inkassoprozesses aufzubewahren** gespeichert wird. Wenn eine Rechnung den letzten Schritt des Inkassoprozesses erreicht, wird sie nicht verwendet, um zukünftige Aktionstypen für die Prozessautomatisierung zu erstellen, wenn **Rechnung nach der Aktivierung des letzten Prozessschrittes ausschließen** auf **Ja** festgelegt ist. Die nächstälteste Rechnung bestimmt den nächsten Prozessautomatisierungsschritt, um sicherzustellen, dass die Automatisierungsaktionen für den Inkassoprozess fortgesetzt werden. 

## <a name="payment-predictions"></a>Zahlungsvorhersagen
Ab Version 10.0.21 prognostizieren Vorhersagen für Kundenzahlungen, die in Finance Insights zu finden sind, ob eine Rechnung pünktlich, verspätet oder sehr spät bezahlt wird. Sie können jede dieser Kategorien in Finance Insights konfigurieren. Wenn Rechnungen voraussichtlich verspätet bezahlt werden, ist es wichtig, den Inkassoprozess vor Fälligkeit der Rechnung zu starten. Diese Vorhersagen können verwendet werden, um Inkassoaktivitäten zu erstellen, wenn die Automatisierungen für Inkassoprozesse ausgeführt werden. Legen Sie **Vorhersagen für Zahlungen aktivieren** auf **Ja** fest, um Vorhersagen für Kundenzahlungen zu verwenden und so Inkassoaktivitäten basierend auf der Wahrscheinlichkeit zu erstellen, dass die Rechnung verspätet bezahlt wird. 

Weitere Informationen zu Vorhersagen für Kundenzahlungen und Finance Insights finden Sie unter [Vorhersagen für Kundenzahlungen](payment-insights-overview.md).

Wenn das Modell für Vorhersagen für Kundenzahlungen ausgeführt wird, weist es der Vorhersage einen Prozentsatz zu, der angibt, ob die Rechnung pünktlich, verspätet oder sehr spät bezahlt wird. Sie können diese Informationen verwenden, um Inkassoaktivitäten mithilfe der Inkasso-Prozessautomatisierung automatisch zu starten, wenn mit Zahlungsverzug zu rechnen ist. Sie können diese Prozentsätze auf den Seiten **Zahlungsvorhersagen pro Debitor** oder **Zahlungsvorhersagen pro Transaktion** unter **Kredit und Inkasso > Inkasso** anzeigen. 

Wenn die durchschnittliche Zahlungsvorhersage für eine Kundenrechnung kleiner als der Benchmark-Prozentsatz ist, wird keine Aktivität erstellt. Wenn die Rechnungsvorhersage größer oder gleich dem Benchmark-Prozentsatz ist, wird eine Aktivität pro Debitor erstellt. Geben Sie für **Vorhersage: Spät** den **Benchmark-Prozentsatz** ein, bei dem die Automatisierung von Inkassoprozessen Inkassoaktivitäten erstellen soll. Dies ist ein Gesamtwert von spät und sehr spät. Wählen Sie eine **Vorlage für Geschäftsdokumente** aus, die für die erstellte Aktivität zu verwenden ist, oder erstellen Sie eine neue. Dadurch werden **Typ**, **Zweck** und **Tage bis zum Abschluss der Aktivität** identifiziert. Geben Sie **Notizen** ein, die beim Erstellen der Aktivität standardmäßig als Beschreibung angegeben werden. Geben Sie für **Vorhersage: Sehr spät** den **Benchmark-Prozentsatz** ein, bei dem die Automatisierung von Inkassoprozessen Inkassoaktivitäten für einen Kunden erstellen soll, bei dem vorhergesagt wird, dass er Rechnungen sehr spät bezahlt. Wählen Sie eine **Vorlage für Geschäftsdokumente** aus, die für die erstellte Aktivität zu verwenden ist. Dadurch werden **Typ**, **Zweck** und **Tage bis zum Abschluss der Aktivität** identifiziert. Geben Sie **Notizen** ein, die beim Erstellen der Aktivität standardmäßig als Beschreibung angegeben werden. 

### <a name="example"></a>Beispiel
Wenn der Benchmark-Prozentsatz für späte Zahlungen auf 60 % gesetzt ist. Wenn Vorhersagen für Kundenzahlungen für jede Rechnung ausgeführt werden, weist das System einen Prozentsatz zu, der angibt, ob die Rechnung pünktlich, verspätet oder sehr spät bezahlt wird. Wenn die Zahlungsvorhersage, dass die Rechnung verspätet bezahlt wird, 59 % oder weniger beträgt, wird durch den automatisierten Inkassoprozess keine Inkassoaktivität für die Rechnung erstellt. Wenn die Vorhersage der Kundenzahlung für eine Rechnung größer oder gleich 60 % ist, wird während der Automatisierung des Inkassoprozesses eine Inkassoaktivität erstellt. 

> [!NOTE]
> Die sehr späte Vorhersage wird vor der späten Vorhersage ausgewertet, da die Angabe„sehr spät“ Rechnungen umfasst, die voraussichtlich zu spät bezahlt werden. Der Inkassoprozess generiert nur eine Aktivität, wenn die Rechnung sowohl in den späten als auch in den sehr späten Benchmark fällt. In diesem Fall verwendet das System die sehr späte Aktivität und den Geschäftsbeleg, da die Angabe „sehr spät“ eine höhere Priorität hat. Alle anderen bereits generierten Aktionen werden nicht ein zweites Mal generiert.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
