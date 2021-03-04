---
title: Häufig gestellte Fragen zu Aktivitäten am Jahresende
description: In diesem Artikel finden Sie Informationen über die Aktivitäten zum Jahresende.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d10f54913ca8dff56a59ea597a9bd7c3e69d4bc
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107694"
---
# <a name="year-end-activities-faq"></a>Häufig gestellte Fragen zu Aktivitäten am Jahresende 

In diesem Artikel finden Sie Informationen über die Aktivitäten zum Jahresende. Es geht überwiegend um Fragen zum Jahresabschluss von Hauptbuch und Kreditorenkonten.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Hauptbuch: Woher weiß ich, dass wir den Jahresendabschluss durchführen und nicht rückgängig machen?
Wir wissen, das Unternehmen versucht haben, den Jahresendabschluss durchzuführen, ihn stattdessen aber rückgängig gemacht haben. Wenn der Jahresendabschluss sehr schnell endet oder keine Anfangssalden ergibt, überprüfen Sie unter **Jahresendabschluss** die Einstellung **Vorherigen Abschluss rückgängig machen** (**Hauptbuch > Jahresendabschluss > Geschäftsjahresabschluss ausführen**). 

[![Durchführung des Jahresendabschlusses im Vergleich zum Rückgängigmachen des Jahresendabschlusses](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Ist **Vorherigen Abschluss rückgängig machen** auf **Ja** eingestellt, wird der vorherige Abschluss rückgängig gemacht. Beim Rückgängigmachen werden alle Abschluss- und Anfangssalden gelöscht, als wäre der Jahresendabschluss nie erfolgt. Belege werden gelöscht. Der Jahresendabschluss wird nicht automatisch erneut ausgeführt. Vielmehr muss der Vorgang manuell erneut gestartet werden, indem **Vorherigen Abschluss rückgängig machen** auf **Nein** gesetzt wird. 

> [!NOTE]
> Der Abschlusssaldo wird optional im abzuschließenden Jahr erstellt. Dies tritt nur auf, wenn der Hauptbuchparameter **Abschlussbuchungen bei Umbuchung erstellen** auf **Ja** eingestellt ist. Der Anfangssaldo wird immer erstellt, weil damit das nächste Jahr beginnt.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Hauptbuch: Was ist der Unterschied zwischen dem Rückgängigmachen und dem Löschen des Hauptbuchparameters beim Jahresendabschluss?
Eventuell bestehen Unklarheiten bezüglich des Parameters **Vorherigen Abschluss rückgängig machen** aus dem Dialogfeld **Jahresendabschluss** und des Parameters **Jahresabschlussbuchungen bei Umbuchung löschen** aus dem Hauptbuch (**Hauptbuch > Periodenabschluss > Jahresendabschluss > Geschäftsjahresabschluss ausführen**).  

[![Unterschied zwischen dem Rückgängigmachen und Löschen des Hauptbuchparameters](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Sollen alle Abschluss- und Anfangssalden gelöscht werden, so als ob der Jahresendabschluss nie erfolgt wäre, wählen Sie bei Durchführung des Jahresendabschlusses im Dialogfeld im Dropdownmenü die Option **Vorherigen Abschluss rückgängig machen** aus. Die Belege werden gelöscht. Der Jahresendabschluss wird nicht automatisch erneut ausgeführt. Um den Jahresendabschluss durchzuführen, müssen Sie diesen Prozess erneut starten, wobei Sie die Option **Vorherigen Abschluss rückgängig machen** (**Hauptbuch > Einrichten des Hauptbuchs > Hauptbuchparameter**) auf **Nein** setzen. 

[![Einstellung des Hauptbuchparameters](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Der Parameter **Jahresabschlussbuchungen bei Umbuchung löschen** aus dem Hauptbuch wird nur verwendet, wenn der Jahresendabschluss ausgeführt wird (nicht, wenn er rückgängig gemacht wird. Die Option **Vorherigen Abschluss rückgängig machen** ist auf **Nein** eingestellt). Ist dieser Parameter auf **Ja** eingestellt, werden alle Abschluss- und Anfangssalden gelöscht, und der Jahresendabschluss wird erneut ausgeführt. Dieser Vorgang wird verwendet, wenn das Unternehmen möchte, dass alle Transaktionen, einschließlich Anpassungen seit dem letzten Jahresendabschluss, für Abschluss- und Anfangssaldo in einer einzigen Buchung gebucht werden sollen. 

Ist diese Option auf **Nein** gesetzt, bleiben alle Abschluss- und Anfangssalden bestehen. Sie werden nicht gelöscht. Stattdessen werden ein neuer Abschlusssaldo- und ein neuer Anfangssaldoeintrag nur für das Delta oder die neuen Transaktionen erstellt, die seit dem letzten Jahresendabschluss dieses Geschäftsjahres gebucht wurden.  

> [!NOTE]
> Der Abschlusssaldo wird im abzuschließenden Jahr erstellt. Dies tritt nur auf, wenn der Hauptbuchparameter **Abschlussbuchungen bei Umbuchung erstellen** auf **Ja** eingestellt ist. Der Anfangssaldo wird immer erstellt, weil damit das nächste Jahr beginnt. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Hauptbuch: Durch welche Änderungen kann die Leistung bei der Verarbeitung des Jahresendabschlusses verbessert werden? 
Die Leistung bei der Verarbeitung des Jahresendabschlusses kann durch eine Reihe von Änderungen verbessert werden. Überlegen Sie anhand der vorgeschlagenen Änderungen, ob diese für Ihr Unternehmen geeignet sind.  

### <a name="dimension-sets"></a>Dimensionssätze
Bei Durchführung des Jahresendabschlusses wird der Saldo jedes Dimensionssatzes neu erstellt, was sich direkt auf die Leistung auswirkt. Einige Unternehmen erstellen unnötigerweise Dimensionssätze, weil diese in der Vergangenheit verwendet wurden oder ggf. wieder verwendet werden könnten.  Diese unnötigen Dimensionssätze werden beim Jahresendabschluss neu erstellt, was Zeit in Anspruch nimmt. Sehen Sie sich Ihre Dimensionssätze genau an, und löschen Sie nicht benötigte Sätze.

Unnötige Dimensionssätze wirken sich auch auf den Batchauftrag **BudgetDimensionFocusInitializeBalance** (**Hauptbuch > Kontenplan > Dimensionen > Finanzdimensionssätze**) aus.

[![Finanzdimensionssätze](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfiguration der Vorlage zum Jahresendabschluss
Mit der Vorlage zum Jahresendabschluss können Unternehmen das Finanzdimensionsniveau auswählen, das bei der Übertragung von Gewinn- und Verlustsalden auf einbehaltene Gewinne beibehalten werden soll. Mit den Einstellungen können Unternehmen die genauen Finanzdimensionen (**Alle abschließen**) beibehalten, wenn die Salden in einbehaltene Gewinne verschoben oder die Beträge zu einem eindimensionalen Dimensionswert zusammengefasst werden (**Einzeln abschließen**). Dies kann für jede Finanzdimension festgelegt werden. Weitere Informationen zu diesen Einstellungen erhalten Sie im Artikel [Jahresendabschluss](year-end-close.md).

Wir empfehlen, dass Sie die Anforderungen Ihres Unternehmens genau betrachten und mit der Option **Einzeln abschließen** so viele Dimensionen wie möglich abschließen, um die Leistung zu verbessern. Durch den Abschluss auf einen einzelnen Dimensionswert (der auch leer sein kann) fällt die systeminterne Berechnung der Salden des Kontos für einbehaltene Gewinne weniger ausführlich aus.

### <a name="10013-update-or-later"></a>Update 10.0.13 oder höher
Wenn Sie seit dem letzten Jahresendabschluss auf Version 10.0.13 oder höher aktualisiert haben, kann der Vorgang aufgrund der [Einführung der HashV2-Funktion](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2) länger dauern. (Der Begriff *Hash* bezieht sich auf ein Feld, das aus anderen Zeichenfolgenfeldern berechnet wird. Die API zur Berechnung des Hash-GUID-Werts wurde zwecks mehr Sicherheit aktualisiert.) Um den Jahresendabschluss zu beschleunigen, empfehlen wir, die Salden der Dimensionssätze vor Durchführung des Jahresendabschlusses neu zu erstellen. Haben Sie die Salden der Dimensionssätze nach der Aktualisierung auf Version 10.0.13 bereits neu erstellt, muss der Vorgang nicht erneut durchgeführt werden.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Hauptbuch: Was geschieht beim Periodenabschluss und beim Jahresendabschluss?
 
[![Periodenabschluss, Jahresendabschluss](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Leistungsverbesserungen bei der Neuerstellung von Finanzdimensionssätzen (neue Funktion)
Eine neue Funktion, die in Version 10.0.16 ergänzt wurde, verbessert die Leistung bei Jahresendabschluss und Konsolidierung. Bei dieser Funktion handelt es sich um Leistungsverbesserungen bei der Neuerstellung von Finanzdimensionssätzen. Im Zuge dieser Verbesserungen werden Dimensionssätze nur über einen relevanten Zeitraum neu erstellt. In den Vorgängerversionen wurden die Dimensionssätze zu sämtlichen Datumsangaben neu erstellt. Wenn Sie beispielsweise das Jahr 2020 abschließen, erstellt das System nur die Salden für Transaktionen im Geschäftsjahr 2020 neu. Erfolgt die Konsolidierung über den Zeitraum vom 1. November bis zum 30. November 2020, erstellt das System die Salden nur über diesen Zeitraum neu.

Weil diese Funktion eine erhebliche Veränderung darstellt, muss sie im Arbeitsbereich **Funktionsverwaltung** aktiviert werden.
 
[![Jahresendabschluss](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Kreditorenkonten: Welche Änderungen wurden zugunsten der Jahresendsteuererklärung (US 1099) für das Jahr 2020 vorgenommen?

2020 wurden zwei neue auflagenrelevante Funktionen für die Jahresendsteuererklärung (US 1099) eingeführt. Die erste Funktion mit der Bezeichnung **Änderungen an den Formularen 1099-NEC und 1099-MISC für 2020 übernehmen** wurde Mitte des Jahres als Pflichtfunktion veröffentlicht. Damit soll sichergestellt werden, dass 1099-Transaktionsdaten von 2020 für das neue 1099-NEC-Formular nachverfolgt werden können. Im Zuge dieser Funktion wurden die Steuerfelder (US 1099) ergänzt, die zur Unterstützung des neuen 1099-NEC-Formulars und zur Aktualisierung der Felder aus dem 1099-MISC-Formular benötigt werden. Bei diesem Update wurden auch die Daten der Herstellerdatensätze für die Informationen im Steuerformularfeld (US 1099) aktualisiert. 

Das zweite auflagenrelevante Funktion mit der Bezeichnung **Steuererklärungen (US 1099) entsprechend Steuergesetzgebung von 2020 aktualisiert** enthält die folgenden Änderungen.

- 1099-OID: Die Bundessteuerbehörde IRS der USA hat das Formular zwecks kontinuierlicher Verwendung umgewandelt.
   - Beim Drucken müssen die 3. und 4. Ziffer des Meldejahres angegeben werden. Verwenden Sie unter **Steuererklärung (US 1099) – Druckoptionen** die 3. und 4. Ziffer des Felds **Jahr der Steuererklärung**. 

- 1099-NEC: ein neues Formular für 2020 Hiermit wird die Vergütung von Nichtmitarbeitern erfasst. 

-   1099-MISC: Aufgrund der Einführung des Formulars 1099-NEC hat das IRS das Formular 1099-MISC überarbeitet und die Feldziffern zur Meldung bestimmter Einnahmen neu angeordnet.
Die Änderungen bei der Meldung von Einkünften und die Änderung der Feldziffern sind nachstehend aufgeführt.
   - Der Steuerzahler hat in Feld 7 mindestens 5.000 US-Dollar (Kontrollkästchen) durch Direktverkäufe erzielt.
   - Der Erlös aus der Ernteversicherung ist in Feld 9 aufgeführt.
   - Das Bruttohonorar für einen Anwalt ist in Feld 10 angegeben.
   - Stundungen gemäß Abschnitt 409A sind in Feld 12 aufgeführt.
   - Nicht qualifizierte Entgeltumwandlung wird in Feld 14 ausgewiesen.
   - In den Feldern 15, 16 und 17 werden die einbehaltenen Steuern, die Identifikationsnummer und die Einkommenshöhe auf Bundesstaatsebene angegeben.

- An 1099-DIV und 1099-INT gab es 2020 keine Änderungen.

- Elektronische Übermittlung: Das Format wurde geändert, um dem neuen NEC-Formular und den oben beschriebenen Änderungen an den MISC-Feldern Rechnung zu tragen. Genaue Informationen zu den Voraussetzungen für eine elektronische Übermittlung finden Sie in der [IRS-Publikation 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Kreditorenkonten: 1099 – Wie ändere ich das Steuerformularfeld (US 1099) und die Werte bei einem Kreditor, der das ganze Jahr über keine Steuerdaten (US 1099) erfasst hat?
Verwenden Sie die Funktionen zum Aktualisieren von 1099 (**Kreditorenkonten > Kreditoren > Alle Kreditoren > Kreditor auswählen > Registerkarte zum Kreditor im Menüband > 1099 aktualisieren**), um die Transaktionen zu den zuvor bezahlten Rechnungen durchzusehen und die Daten aus 1099 entsprechend den Einstellungen auf der Registerkarte **Steuererklärung (US 1099)** auf der Seite **Kreditor** neu zuzuweisen.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kann die Funktion zum Aktualisieren von 1099 für alle meine Kreditoren gleichzeitig ausgeführt werden?
Nein. Die Funktion zum Aktualisieren von 1099 muss für jeden Kreditor einzeln ausgeführt werden. Wenn eine massenweise Aktualisierung in Ihrem Unternehmen erforderlich sein sollte, stimmen Sie bitte für die Idee [Batchverarbeitung zur Aktualisierung der Steuerdaten (US 1099) von Kreditoren](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Kreditorenkonten: 1099 – „Bestehende 1099-Beträge neu berechnen“ im Vergleich zu „Alle aktualisieren“ aus dem Dienstprogramm zur Aktualisierung von 1099.
Mit dem Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird der Steuerbetrag (US 1099) auf die insgesamt bezahlte Summe zurückgesetzt, wenn dies zusammen mit dem Kontrollkästchen **Alle aktualisieren** verwendet wird. 

[![Steuerbuchungen (US 1099): Vor Ausführung der Aktualisierung](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Das Kontrollkästchen **Bestehende 1099-Beträge neu berechnen** wird nur verwendet, wenn die Rechnung partielle 1099-Werte aufweist oder wenn Sie im Formular zur Steuererklärung (US 1099) geändert wurde. Angenommen, Sie haben eine Rechnung im Wert von 1.000,00 US-Dollar, aber der Benutzer gibt auf der Rechnung manuell einen 1099-Betrag von 500,00 US-Dollar ein.

[![Steuerbuchungen (US 1099): Markierung von sowohl „Alle aktualisieren“ als auch „Bestehende 1099-Beträge neu berechnen“](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Bei Bezahlung entspricht der Betrag von 500,00 US-Dollar dem gezahlten Betrag im Formular 1099. Wird eine Neuberechnung durchgeführt, ändert das System den 1099-Betrag in 1.000,00 US-Dollar, was der insgesamt bezahlten Summe entspricht.

[![Steuerbuchungen (US 1099): Nach Ausführung des 1099-Vorgangs](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Kreditorenkonten: 1099 – Buchungen (US 1099) manuell erstellen
Eventuell müssen in einem Unternehmen Buchungen (US 1099), die keiner Rechnung zugeordnet sind, manuell erstellt werden. Dies ist möglich unter **Kreditorenkonten > Periodische Aufgaben > Steuererklärung (US 1099) > Kreditorenausgleich für Steuerformulare (US 1099)**. Wählen Sie die Schaltfläche **Manuelle US 1099-Buchungen** aus. 

Manuell erstellte Buchungen (US 1099) werden nicht im Zuge von **Alle aktualisieren** oder **Bestehende 1099-Beträge neu berechnen** aus dem Dienstprogramm **1099 aktualisieren** aktualisiert.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Kreditorenkonten: 1099 – Wird das 1096-Formular in Dynamics 365 Finance unterstützt? 

Das Formular 1096 mit der jährlichen Zusammenfassung und Übermittlung von US-Informationen kann in Dynamics 365 Finance nicht gedruckt werden.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Kreditorenkonten: 1099 – Gibt es neue Funktionen, mit denen die Steuererklärung (US 1099) im öffentlichen Sektor getätigt werden kann? 
Es wurde eine neue Funktion mit der Bezeichnung **1099-Informationen anhand von Hauptkonto aktualisieren** ergänzt, die Sie im Arbeitsbereich **Funktionsverwaltung** aktivieren können. Damit können die 1099-Werte zu einem Kreditor anhand des Hauptkontos in der Buchhaltungsverteilung und nicht anhand des Standardkontos im Kreditorendatensatz verknüpft werden.

Weitere Informationen finden Sie unter [Kreditoren für Steuererklärung (US 1099) einrichten](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).
