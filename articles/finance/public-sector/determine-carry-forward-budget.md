---
title: Den Budgetvortrag nach Kürzungen in Bestellungen und Rechnungen aktualisieren
description: In diesem Artikel wird beschrieben, wie Sie steuern können, was mit dem Budgetvortag passiert, wenn Bestellungen storniert oder gekürzt werden und wenn Rechnungen gekürzt werden.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: f51839b6890e39a2f2c5867977f3935ab43e2c5d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280528"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Den Budgetvortrag nach Kürzungen in Bestellungen und Rechnungen aktualisieren

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel wird beschrieben, wie Sie steuern können, was mit dem Budgetvortag passiert, wenn Bestellungen storniert oder gekürzt werden und wenn Rechnungen gekürzt werden.

Informationen zur Verarbeitung von Bestellungen am Jahresende finden Sie unter [Bestellungen am Jahresende bearbeiten](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Budgetvortag für Rechnungsabweichungen ein- oder ausschalten

Das System kann den Budgetvortag immer aktualisieren, wenn eine Bestellung storniert oder verringert wird Wenn Sie jedoch den Budgetvortrag aktualisieren möchten, wenn eine Rechnung gekürzt wird, müssen Sie die *Den Budgetvortag reduzieren, wenn eine Rechnung für eine Bestellung mit einer Abweichung verringert wird*-Funktion aktivieren. Administratoren können diese Funktion ein- oder ausschalten, indem Sie im Arbeitsbereich **[Funktionssuche](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** danach suchen.

## <a name="purchase-order-reductions-and-cancellations"></a>Kürzungen und Stornierungen von Bestellungen

Egal ob die *Budgetvortrag reduzieren, wenn eine Rechnung zu einer Bestellung mit einer Abweichung gekürzt wird*-Funktion aktiviert ist, der Budgetvortag wird aktualisiert, wenn eine qualifizierte Bestellung storniert oder reduziert wird. Sie können jeden Hauptbuchfonds so einstellen, dass er auf eine der folgenden Arten reagiert:

- Bewahren Sie den Budgetvortag so auf, wie es erstellt wurde.
- Passen Sie den Budgetvortag automatisch an, um den stornierten oder gekürzten Betrag zu entfernen.

Nur Bestellpositionen mit Verteilungen, die einen Fonds enthalten, sind für die automatische Budgetanpassung verfügbar. Die automatische Budgetanpassung erfolgt, wenn die Bestellung abgeschlossen oder eine Bestellkürzung bestätigt wird.

## <a name="invoice-reductions"></a>Rechnungskürzungen

Wenn die *Budgetvortrag reduzieren, wenn eine Rechnung zu einer Bestellung mit einer Abweichung gekürzt wird*-Funktion aktiviert ist, können Sie angeben, ob jeder Fonds den Budgetvortag verringern all, wenn eine Rechnung gekürzt wird, zusätzlich dazu wenn eine Bestellung gekürzt oder storniert wird. Die Rechnung muss sich auf eine Bestellung beziehen, die einen Budgetvortrag hat. Ermäßigungen umfassen Preisabweichungen, Gebührenabweichungen und Steuerabweichungen. Wird eine Bestellung mit Vortag bei der Fakturierung gekürzt, entsteht eine Abweichung. Wenn die Rechnung gebucht wird, wird die Bestellbelastung um den Betrag der Abweichung reduziert. Die Funktion erstellt auch die automatische Budgetregulierung für den Betrag der Abweichung.

Wenn die *Den Budgetvortag reduzieren, wenn eine Rechnung für eine Bestellung mit einer Abweichung verringert wird*-Funktion deaktiviert ist, wird der Budgetvortag in diesem Szenario nicht gekürzt. Daher bleibt der verbleibende Budgetvortrag in Höhe der Abweichung zurück.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Die Optionen des Budgetvortags für alle Fonds konfigurieren

Befolgen Sie diese Schritte für jeden Hauptbuchfonds, der in der Lage sein sollte, den Budgetvortag zu reduzieren, wenn eine Bestellung oder Rechnung reduziert wird.

1. Wechseln Sie zu **Hauptbuch \> Kontenplan \> Geldmittel \> Geldmittel**.
1. Wählen Sie die Geldmittel aus, die Sie einrichten möchten.
1. Stellen Sie unter **Bestellungsprozess zum Jahresende** sicher, dass die **Ausgewählte Option zum Jahresende überschreiben**-Option auf *Ja* eingestellt ist.
1. Legen Sie unter **Status des Budgetvortrags** das Feld **Wiedereinsetzung des Budgets, wenn eine Übertragsbestellung storniert oder verringert wird** nach Bedarf fest. Die Einstellungen haben leicht unterschiedliche Auswirkungen, je nachdem, ob die *Budgetvortrag reduzieren, wenn eine Rechnung zu einer Bestellung mit einer Abweichung gekürzt wird*-Funktion in Ihrem System aktiviert ist.

    - Wenn die Funktion ausgeschaltet ist, reagiert das System nur auf stornierte oder reduzierte Bestellungen. Die Optionseinstellungen funktionieren wie folgt:

        - *Nein* – das System erstellt einen Budgetregistereintrag für den verbleibenden Saldo der Bestellungen, die storniert oder reduziert wurden.
        - *Ja* – das System lässt zu, dass Bestellungen storniert oder reduziert werden, erstellt jedoch keinen Budgetregistereintrag. Der Budgetvortrag bleibt für den Verbrauch durch andere Belege verfügbar.

    - Wenn die Funktion eingeschaltet ist, reagiert das System auf Rechnungsabweichungen und stornierte oder reduzierte Bestellungen. Die Optionseinstellungen funktionieren wie folgt:

        - *Nein* – bei Rechnungsabweichungen erstellt das System einen Budgetregistereintrag für die Bestellung für den Betrag der Abweichungsreduzierung. Bei stornierten oder reduzierten Bestellungen hat diese Einstellung die gleiche Wirkung wie bei ausgeschalteter Funktion.
        - *Ja* – bei Rechnungsabweichungen lässt das System die Rechnungskürzung zu, erstellt aber keinen Budgetregistereintrag. Der Budgetvortrag bleibt für den Verbrauch durch andere Belege verfügbar. Bei stornierten oder reduzierten Bestellungen hat diese Einstellung die gleiche Wirkung wie bei ausgeschalteter Funktion.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Bestellungen am Jahresende verarbeiten](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Allgemeine Budgetreservierungen verwalten](general-budget-reservation-tasks.md)
- [Geldmittel im öffentlichen Sektor](funds-public-sector.md)
- [Erstellen Sie einen Zahlungsmittelcode für öffentlichen Sektor](tasks/set-up-fund-public-sector.md)
