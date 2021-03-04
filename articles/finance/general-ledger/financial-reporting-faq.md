---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070216"
---
# <a name="financial-reporting-faq"></a>Häufig gestellte Fragen zur Finanzberichterstellung 

In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?

Szenario: Das Demounternehmen USMF hat eine Bilanz erstellt, die nicht alle Benutzer der Finanzberichterstellung in Dynamics 365 einsehen sollen. Lösung: Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer die Berichte aufrufen können. 

1.  Im Berichts-Designer der Finanzberichterstellung anmelden

2.  Neue Baumdefinition erstellen (Datei | Neu | Baumdefinition) a.    Doppelklicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.
  i.    Klicken Sie auf „Benutzer und Gruppen“.  
          1. Wählen Sie den/die Benutzer oder die Gruppe aus, die auf diesen Bericht zugreifen möchte. 
          
[![Benutzerbildschirm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![Sicherheitsbildschirm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klicken Sie auf **Speichern**.
  
[![Schaltfläche „Speichern“](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Neue Baumdefinition in der Berichtsdefinition ergänzen

[![Formular „Baumdefinition“](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Klicken Sie in der Baumdefinition auf „Einstellung“ und danach unter „Auswahl der Berichtseinheit“ auf „Alle Einheiten einschließen“.

[![Formular zur Auswahl der Berichtseinheit](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Vorher:** [![Screenshot „Vorher“](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Nachher:** [![Screenshot „Nachher“](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Hinweis: Die obige Meldung wird angezeigt, weil der Benutzer nach Übernahme der Einheitssicherheit keinen Zugriff mehr auf den Bericht hat.



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Wie finde ich heraus, welche Konten nicht mit meinen Saldo in D365 übereinstimmen?

Wenn ein Bericht in D365 nicht den Erwartungen entspricht, können Sie Konten und Abweichungen wie folgt ermitteln. 

### <a name="in-financial-reporter-report-designer"></a>Im Berichts-Designer der Finanzberichterstellung

1.  Neue Zeilendefinition erstellen a.    Auf „Bearbeiten“ | „Zeilen aus Dimensionen einfügen“ i.  „MainAccount“ auswählen [![Hauptbildschirm auswählen](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Auf „OK“ klicken b.    Zeilendefinition speichern

2.  Eine neue Spaltendefinition erstellen     [![Eine neue Spaltendefinition erstellen](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Eine neue Berichtsdefinition erstellen a.    Auf „Einstellungen“ klicken und das Kontrollkästchen [![Einstellungsformular](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png) deaktivieren
   
4.  Erstellen Sie den Bericht. 

5.  Exportieren Sie den Bericht in Excel.

### <a name="in-d365"></a>In D365: 
1.  Auf „Hauptbuch“ | „Anfragen und Berichte“ | „Zwischenbilanz“ klicken a.    Parameter i.  Ab Datum: Beginn des Geschäftsjahres ii. Bis Datum: Datum, zu dem der Bericht erstellt wurde iii.    Finanzdimensionssatz, „Hauptkonto“ festgelegt [![Hauptkontoformular](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Auf „Berechnen“ klicken

2.  Bericht in Excel exportieren

Sie sollten nun in der Lage sein, die Daten aus dem Excel-Bericht in der Finanzberichterstellung in den D365-Zwischenbilanzbericht zu kopieren und die Spalten mit der Abschlussbilanz zu vergleichen.
