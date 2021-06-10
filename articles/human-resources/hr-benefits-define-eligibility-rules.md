---
title: Regeln und Richtlinien zur Vorteilsberechtigung festlegen
description: Dieser Artikel beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053152"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Regeln und Richtlinien zur Vorteilsberechtigung festlegen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema beschreibt, wie Sie Vorteilsberechtigungsregeln und -richtlinien erstellen und diese Regeln dann zu Vorteilen zuweisen.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Erstellen eines Regeltyps für Vergütungsberechtigungsrichtlinien

1. Wechseln Sie zu **Personalverwaltung > Vorteile > Berechtigung > Regeltypen für Vorteilsberechtigungsrichtlinien**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Regelname** einen Wert ein.
4. Geben Sie im Feld **Beschreibung** einen Wert ein, oder wählen Sie einen Wert aus.
5. Wählen Sie im Feld **Abfragename** die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
7. Wählen Sie **Speichern** aus.
8. Schließen Sie die Seite.

## <a name="benefit-eligibility-policy"></a>Vergütungsberechtigungsrichtlinie

1. Wechseln Sie zu **Personalverwaltung > Vorteile > Berechtigung > Vorteilsberechtigungsrichtlinien**.
2. Wählen Sie eine vorhandene Vorteilsrichtlinie aus.
3. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
4. Schalten Sie die Erweiterung des Abschnitts **Richtlinienorganisationen** ein/aus. Sie können alle Organisationen hinzufügen oder entfernen, die Sie in der Richtlinie einbeziehen möchten.
5. Erweitern oder reduzieren Sie den Abschnitt **Richtlinienregeln**.
6. Suchen Sie in der Liste die zuvor erstellte Richtlinienregel.
7. Wählen Sie **Richtlinienregel erstellen** aus.
8. Geben Sie im Feld **Gültigkeitsdatum** das Datum ein, an dem die Richtlinie gültig werden soll.
    * Das Festlegen des effektiven Enddatums ermöglicht es Ihnen, zukünftige Änderungen an den Richtlinienregeln vorzunehmen, sodass Sie nicht zur Richtlinie zurückkehren müssen, wenn diese Änderungen wirksam werden sollen.  
9. Fügen Sie bei Bedarf eine where-Klausel im **Bedingung hinzufügen**-Feld hinzu.
    * Wenn Sie beispielsweise möchten, dass die Regel nur für Verkaufsleiter gilt, können Sie eine where-Klausel erstellen, bei der die Positionsbeschreibung Verkaufsleiter entspricht. Sie können mehrere where-Anweisungen zusammen in der Regel hinzufügen.  
10. Wählen Sie **OK**.
11. Schließen Sie die Seite.

## <a name="assign-rule-to-benefit"></a>Zuweisen der Regel zum Vorteil

1. Wechseln Sie zu **Personalverwaltung > Vorteile > Vorteile**.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
4. Erweitern oder reduzieren Sie den Abschnitt **Berechtigungsregeln**.
5. Wählen Sie **Bearbeiten** aus.
6. Wählen Sie die Regel im Feld **Berechtigung** aus.
7. Wählen Sie im Feld **Regeltyp** die zuvor erstellte Regel aus.
9. Wählen Sie in der Liste den Link in der ausgewählten Zeile.
10. Wählen Sie **Speichern** aus.
11. Schließt das Formular.



[!INCLUDE[footer-include](../includes/footer-banner.md)]