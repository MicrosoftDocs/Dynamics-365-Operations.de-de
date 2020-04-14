---
title: Kreditorenrechnungsrichtlinien einrichten
description: In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143360"
---
# <a name="set-up-vendor-invoice-policies"></a>Kreditorenrechnungsrichtlinien einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Richtlinien für Kreditorenrechnungen eingerichtet werden. Kreditorenrechnungsrichtlinien werden ausgeführt, wenn Sie mit der Seite "Kreditorenrechnung" eine Kreditorenrechnung buchen und wenn Sie die Seite "Richtlinienverstöße" der Kreditorenrechnung öffnen. Sie können auch den Workflow für Kreditorenrechnungen konfigurieren, sodass Kreditorenrechnungsrichtlinien immer ausgeführt werden, wenn eine Rechnung an den Workflow übermittelt wird. 

- Kreditorenrechnungsrichtlinien werden nicht auf Rechnungen angewendet, die im Rechnungsbuch oder in einer Rechnungserfassung erstellt wurden.  
- Für die Rechnungsabgleichüberprüfung werden keine Kreditorenrechnungsrichtlinien verwendet. Stattdessen wird die Prüfung auf der Seite "Kreditorenkontenparameter" eingerichtet.  
- Für diese Erfassung wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Vorbereitung zum Erstellen von Kreditorenrechnungsrichtlinien
1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Einstellung > Kreditorenkontenparameter**.
2. Wählen Sie die Registerkarte**Rechnungsprüfung**.
3. Aktivieren oder deaktivieren Sie das Kontrollkästchen **Rechnungskopfstatus automatisch aktualisieren**.
4. Wählen Sie **OK**.
5. Wählen Sie im Feld **Rechnung mit Abweichungen buchen** eine Option aus.
6. Schließen Sie die Seite.
7. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.
8. Wählen Sie **Parameter** aus.
9. Wählen Sie **Hinzufügen** aus.
10. Schließen Sie die Seite, um zur Startseite zurückzukehren.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Erstellen von Richtlinienregeltypen für Kreditorenrechnungen
1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinienregeltypen für Kreditorenrechnungen**.
2. Wählen Sie **Neu** aus.
3. Geben Sie in den Feldern **Regelname** und **Beschreibung** Werte ein.
4. Wählen Sie im Feld **Abfragename** die Dropdown-Schaltfläche aus, um die Suche zu öffnen, und wählen Sie dann den gewünschten Datensatz aus.
5. Wählen Sie **Speichern**.
6. Schließen Sie die Seite, um zur Startseite zurückzukehren.

## <a name="define-a-vendor-invoice-policy"></a>Definieren einer Kreditorenrechnungsrichtlinie
1. Wechseln Sie zu **Navigationsbereich > Module > Kreditoren > Richtlinieneinstellungen > Richtlinien für Kreditorenrechnung**.
2. Wählen Sie **Neu** aus.
3. Geben Sie in den Feldern **Name** und **Beschreibung** Werte ein.
4. Erweitern oder reduzieren Sie den Abschnitt **Richtlinienorganisationen**.
5. Wählen Sie in der Struktur **Contoso Unterhaltungsanlagen USA** aus.
6. Wählen Sie **Hinzufügen** aus.
7. Erweitern oder reduzieren Sie den Abschnitt **Richtlinienregeln**.
8. Wählen Sie **Richtlinienregel erstellen** aus.
9. Geben Sie im Feld **Beschreibung der Richtlinienregel** einen Wert ein.
10. Wählen Sie **Filter** aus.
11. Wählen Sie **Hinzufügen** aus. Wählen Sie den gewünschten Datensatz aus.
12. Wählen Sie in den Feldern **Tabelle**, **Abgeleitete Tabelle** und **Feld** Optionen aus den Dropdownmenüs aus, oder geben Sie Werte ein..
13. Schließen Sie die Seite.
14. Geben Sie im Feld **Kriterien** einen Wert ein.
15. Wählen Sie **OK**.
16. Wählen Sie **OK**.
17. Schließen Sie die Seiten, um zur Startseite zurückzukehren.

