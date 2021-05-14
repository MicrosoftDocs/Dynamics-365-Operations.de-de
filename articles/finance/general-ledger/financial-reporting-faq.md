---
title: Häufig gestellte Fragen zur Finanzberichterstellung
description: In diesem Artikel werden Fragen anderer Benutzer zur Finanzberichterstellung beantwortet.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923024"
---
# <a name="financial-reporting-faq"></a>Häufig gestellte Fragen zur Finanzberichterstellung 

Dieser Artikel gibt Antwort auf häufig gestellte Fragen zur Finanzberichterstattung. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Wie beschränke ich den Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit?

Das folgende Beispiel zeigt, wie der Zugriff auf einen Bericht mithilfe der Baumstruktursicherheit eingeschränkt werden kann.

Auf den Bilanzbericht des USMF-Demounternehmens sollen nicht alle Benutzer der Finanzberichterstellung zugreifen dürfen. Mithilfe der Baumstruktursicherheit können Sie den Zugriff auf einzelne Berichte so einschränken, damit nur bestimmte Benutzer die Berichte aufrufen können. So schränken Sie den Zugriff ein: 

1. Melden Sie sich in Financial Reporter Report Designer an.
2. Erstellen Sie eine neue Baumdefinition. Wählen Sie **Datei > Neu > Baumdefinition** aus.
3. Doppelklicken Sie in der Spalte **Einheitssicherheit** auf **Zusammenfassung**.
4. Klicken Sie auf **Benutzer und Gruppen**.  
5. Wählen Sie die Benutzer oder Gruppen aus, die auf diesen Bericht zugreifen dürfen. 
6. Wählen Sie **Speichern** aus.
7. Ergänzen Sie die neue Baumdefinition in der Berichtsdefinition.
8. Wählen Sie in der Baumdefinition **Einstellung** aus. Wählen Sie unter **Auswahl der Berichtseinheit** die Option **Alle Einheiten einschließen** aus.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Wie finde ich heraus, welche Konten nicht mit meinen Salden übereinstimmen?

Bei einem Bericht, in dem die Salden nicht übereinstimmen, können Sie die einzelnen Konten und Abweichungen in folgenden Schritten ermitteln. 

**Financial Reporter Report Designer**
1. Erstellen Sie in Financial Reporter Report Designer eine neue Zeilendefinition. 
2. Wählen Sie **Bearbeiten > Zeilen aus Dimensionen einfügen** aus.
3. Wählen Sie **Hauptkonto** aus.  
4. Wählen Sie **OK** aus.
5. Speichern Sie die Zeilendefinition.
6. Neue Spaltendefinition erstellen
7. Erstellen Sie eine neue Berichtsdefinition.
8. Wählen Sie **Einstellungen** aus, und deaktivieren Sie diese Option.  
9. Erstellen Sie den Bericht. 
10. Exportieren Sie den Bericht in Microsoft Excel.

**Dynamics 365 Finance** 
1. Wählen Sie in Dynamics 365 Finance die Optionen **Hauptbuch > Anfragen und Berichte > Zwischenbilanz** aus.
2. Legen Sie die folgenden Parameter fest:
   - **Ab Datum**: Geben Sie den Beginn des Geschäftsjahres ein.
   - **Bis Datum**: Geben Sie das Datum ein, zu dem der Bericht erstellt wird.
   - **Finanzdimension**: Setzen Sie dieses Feld auf **Hauptkonto festgelegt**.
 3. Wählen Sie **Berechnen** aus.
 4. Exportieren Sie den Bericht in Microsoft Excel.

Nun sollten sich die Daten aus dem Excel-Bericht in der Finanzberichterstellung in den Bericht zur Zwischenbilanz kopieren lassen, damit Sie die Spalten zur **Abschlussbilanz** vergleichen können.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]