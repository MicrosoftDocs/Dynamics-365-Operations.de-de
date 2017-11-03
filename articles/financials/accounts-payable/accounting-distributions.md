---
title: Buchhaltungsverteilungen
description: "Dieser Artikel legt Informationen zu Buchhaltungsverteilungen fest und beschreibt die Optionen, die für die Verarbeitung verfügbar sind. Buchhaltungsverteilungen werden verwendet, um Geldbeträgen für ein Quelldokument auf bestimmte Sachkonten zuzuweisen."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bbf23d9cab01e8cdbae776c9310fbd19b429443d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="accounting-distributions"></a>Buchhaltungsverteilungen

[!include[banner](../includes/banner.md)]


Dieser Artikel legt Informationen zu Buchhaltungsverteilungen fest und beschreibt die Optionen, die für die Verarbeitung verfügbar sind. Buchhaltungsverteilungen werden verwendet, um Geldbeträgen für ein Quelldokument auf bestimmte Sachkonten zuzuweisen. 

Buchhaltungsverteilungen stellen eine programmweite Funktion dar, die in jedem Quelldokument Anwendung findet und erweitert wird. Ein Quelldokument kann beispielsweise eine Bestellung, eine Kreditorenrechnung, eine Spesenabrechnung oder eine Freitextrechnung sein. Standardmäßig wird eine Standardbuchhaltungsverteilung für jede Position und jeden Geldbetrag im Quelldokument generiert und bedingt für eine Modifizierung aktiviert. 

> [!Note] 
> Einige Dokumente unterstützen außerdem Geldbeträge in Dokumentkopfzeilen, z B. Zuschläge für Aufträge und Rechnungen. 

Die allgemeinen Buchhaltungsverteilungsfunktionen stellen die folgenden Optionen für die Verarbeitung von Buchhaltungsverteilungen bereit:

-   **Beträge verteilen** – Dient zum Anzeigen und Ändern der Buchhaltungsverteilungen für eine einzelne Dokumentkopfzeile oder Position und alle untergeordneten Positionen wie Steuern oder Zuschläge.
    -   Für die obersten Geldbetragverteilungen (übergeordnete Verteilungen) lassen sich das Hauptkonto und die Finanzdimensionen unter Umständen direkt in der segmentierten Eintragssteuerung im Raster bearbeiten. Der erweiterte Preis ist ein typisches Beispiel für eine solche übergeordnete Verteilung.
    -   Die Verteilungsbeträge basieren auf der für den Zeitraum gültigen Währung für das Dokument. Normalerweise handelt es sich bei dieser Währung um die Buchungswährung. Buchhaltungs- und Berichtswährungsbeträge werden als Teil der Buchhaltung für untergeordnete Sachkonten generiert.
    -   Die Verteilungen zeigen den Abschlussstichtag und das Buchhaltungsereignis an. In der Regel wird das Buchhaltungsereignis auf **Keine** festgelegt, bis das Dokument gebucht/journalisiert wurde. Zu diesem Zeitpunkt ändert sich das Buchhaltungsereignis zu **Original**. Nach dem Buchen der Verteilungen können Sie die Verteilungen nicht mehr ändern.
    -   Die Schaltfläche **Teilen** steht möglicherweise für übergeordnete Verteilungen zur Verfügung. **Teilen** generiert neue Buchhaltungsverteilungen. Das Teilen kann basierend auf dem Prozentsatz, dem Betrag oder der Menge erfolgen.
    -   Die Schaltfläche**Gleichmäßig verteilen** kann in Kombination mit **Teilen** verwendet werden, um den Betrag automatisch gleichmäßig allen Verteilungen zuzuordnen.
    -   Die Schaltfläche **Zurücksetzen** steht möglicherweise für übergeordnete Verteilungen zur Verfügung, wenn mehrere Verteilungen vorhanden sind. Mit **Zurücksetzen** wird jede manuelle Änderung an der Verteilung rückgängig gemacht, indem alle vorhandenen Verteilungen gelöscht und die Standardverteilungen erneut generiert werden.
    -   Jede untergeordnete Verteilung, z. B. Rabatt, Belastung und Mehrwertsteuer, folgt jeweils der übergeordneten Verteilung. Sie können die über- und untergeordnete Beziehung unter **Referenz** &gt; **Informationen zur übergeordneten Position** anzeigen.
    -   Das Hauptkonto und die Finanzdimension können möglicherweise auch für untergeordnete Elemente bearbeitet werden.
    -   Die Finanzdimensionen für die Buchhaltungsverteilungen folgen einem Standardmuster, das ein Dokument erweitern kann. Weitere Informationen finden Sie in den zugehörigen Artikeln.
    -   Möglicherweise werden in den entsprechenden Szenarien Abweichungsverteilungen generiert, zum Beispiel beim Abgleich zwischen einer Kreditorenrechnung und einer Bestellung. Sie können die entsprechenden Beziehungen zwischen Buchhaltungsverteilungen unter **Referenz** &gt; **Dokumentinformationen** anzeigen.
    -   Die Schaltfläche **Korrigieren** steht für Dokumente zur Verfügung, die Korrekturen unterstützen. **Richtig** erstellt neue Verteilungen. Zuerst werden Verteilungen erstellt, die die ursprünglichen Verteilungen stornieren. Diese Verteilungen können nicht geändert werden. Als Nächstes werden neue korrekte Buchhaltungsverteilungen erstellt. Diese Verteilungen können geändert werden, wenn die ursprünglichen Verteilungen geändert werden konnten.
    -   Die Schaltfläche**Projektdetails** wird als Erweiterung aktiviert, wenn eine Position einem Projekt zugeordnet ist. Über Projektbuchhaltungsverteilungen können Sie Details ändern, z. B. die Finanzierungsquelle und den Abrechnungscode.
    -   Sie können den aktuellen Buchhaltungsstatus des Dokuments unter anzeigen unter **Referenz**. Der Status ist für das gesamte Dokument und gibt an, ob das Dokument in Prozess oder in abgeschlossenem Zustand ist.
-   **Verteilungen anzeigen** – Zeigt die Buchhaltungsverteilungen für alle Positionen und Geldbeträge im Dokument an. Sie können die Buchhaltungsverteilungen in dieser Ansicht nicht ändern.


Weitere Informationen finden Sie unter [Buchhaltungsverteilungen und Erfassungseinträge im untergeordneten Sachkonto für Freitextrechnungen](accounting-distributions-subledger-journal-entries-vendor-invoices.md)



