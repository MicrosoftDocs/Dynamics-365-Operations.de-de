---
title: Regeln und Richtlinien zur Vorteilsberechtigung festlegen
description: Dieser Artikel beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009215"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Regeln und Richtlinien zur Vorteilsberechtigung festlegen

Dieser Artikel beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.  

Das Demodatenunternehmen, das verwendet wird, um diese Aufzeichnung zu erstellen, ist USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Erstellen eines Regeltyps für Vergütungsberechtigungsrichtlinien
1. Wechseln Sie zu "Personalverwaltung" > "Vorteile" > "Berechtigung" > "Regeltypen für Vergütungsberechtigungsrichtlinien".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Regelname" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Klicken Sie im Feld "Abfragename" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.

## <a name="benefit-eligibility-policy"></a>Vergütungsberechtigungsrichtlinie
1. Wechseln Sie zu "Personalverwaltung"  "Vorteile"  "Berechtigung"  "Vorteilsberechtigungsrichtlinien".
2. Wählen Sie eine vorhandene Vorteilsrichtlinie aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts "Richtlinienorganisationen" ein/aus.  Hier können Sie alle Organisationen hinzufügen oder entfernen, die Sie in der Richtlinie einbeziehen möchten.
5. Erweitern oder reduzieren Sie den Abschnitt "Richtlinienregeln".
6. Suchen Sie in der Liste die zuvor erstellte Richtlinienregel.
7. Klicken Sie auf "Richtlinienregel erstellen".
8. Geben Sie im Feld "Gültigkeitsdatum" das Datum ein, an dem die Richtlinie gültig werden soll.
    * Das Festlegen des effektiven Datums und des Enddatums ermöglicht es Ihnen, zukünftige Änderungen an den Richtlinienregeln vorzunehmen, ohne dass Sie zur Richtlinie zurückkehren müssen, wenn diese Änderungen wirksam werden sollen.  
9. 
    * Wenn Sie beispielsweise möchten, dass die Regel nur für Verkaufsleiter gilt, können Sie eine WHERE-Klausel erstellen, bei der die Positionsbeschreibung Verkaufsleiter entspricht.  Sie können mehrere WHERE-Anweisungen mit AND und OR in der Regel verbinden.  
10. Klicken Sie auf "OK".
11. Schließen Sie die Seite.
12. Schließen Sie die Seite.

## <a name="assign-rule-to-benefit"></a>Zuweisen der Regel zum Vorteil
1. Wechseln Sie zu "Personalverwaltung" > "Leistungen" > "Leistungen".
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
4. Erweitern oder reduzieren Sie den Abschnitt "Berechtigungsregeln".
5. Klicken Sie auf Bearbeiten.
6. Wählen Sie im Feld "Berechtigung" "Regelbasiert" aus der Liste aus.
7. Klicken Sie im Feld "Regeltyp" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
8. Suchen Sie in der Liste die zuvor erstellte Richtlinienregel und wählen Sie diese aus.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Klicken Sie auf "Speichern".
11. Schließt das Formular.

