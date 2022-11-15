---
title: Erweiterbarkeit der geschlechtsbasierte Enumeration
description: Dieser Artikel bietet einen Überblick über die Erweiterbarkeit der geschlechtsspezifischen Basisenumeration (enum).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749314"
---
# <a name="gender-base-enum-extensibility"></a>Erweiterbarkeit der geschlechtsbasierte Enumeration

Die **Geschlecht** Enumeration (enum) ist jetzt erweiterbar. Dieser Artikel beschreibt die Änderungen, die Sie an der Codebasis vornehmen müssen, wenn Sie planen, die **Geschlecht** Enumeration zu erweitern.

## <a name="gender-vs-hcmpersongender"></a>Geschlecht vs. HcmPersonGender

Es gibt zwei Aufzählungen für Geschlechtswerte:

- **Geschlecht** (Anwendungsplattform)
- **HcmPersonGender** (Personalmanagement)

Die **Geschlecht** Enumeration wird in Microsoft Dynamics 365 Finance durchgehend verwendet, während **HcmPersonGender** spezifisch für die Human Capital Management (HCM)-Funktionalität ist. Wenn Sie die HCM-Funktionalität verwenden und Änderungen an der **Geschlecht** Enumeration vornehmen, sollten Sie die gleichen Änderungen an der **HcmPersonGender** vornehmen. Wenn Sie zum Beispiel **Transgender** zur **Geschlecht** Enumeration hinzufügen, fügen Sie **Transgender** auch zur **HcmPersonGender** Enumeration hinzu.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTransformUtil (Klasse)

Eine neue **HcmPersonGenderTransformUtil** Klasse wurde erstellt, um die Übersetzung zwischen den beiden Basisenumeratoren zu ermöglichen. In dieser Klasse gibt es zwei Methoden: **convertGenderToHcmPersonGender** und **convertHcmPersonGenderToGender**. Sie sollten eine Erweiterung erstellen, indem Sie die Klasse **Befehlskette** bzw. **Event-Handler** verwenden, und Sie beide Methoden erweitern, um neue Werte zuzuordnen, die einer der beiden Basisaufzählungen hinzugefügt werden.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (Class)

**PayrollStateWageTaxPrepDP** ist die Datenanbieterklasse für den **Payroll State Lohnsteuer Prep** SQL Server Reporting Services (SSRS)-Bericht. Für die Vereinigten Staaten sind drei Werte verfügbar: **Männlich**, **Weiblich**, und **Nicht spezifiziert**. In der **populatePayrollStateWageTaxPrepTmp**-Methode gibt es eine Switch-Anweisung, die verwendet wird, um den Wert der **HcmPersonGender** Aufzählung zu einem von drei Feldern abzubilden: **IsMale**, **IsFemale**, oder **IsUnspecifiedGender**. Der Standardwert für die Switch-Anweisung ist **IsUnspecifiedGender**. Wenn Sie Werte zur **HcmPersonGender** Aufzählung anders zuordnen, müssen Sie eine Erweiterung erstellen, indem Sie die **Befehlskette** Klasse über die **populatePayrollStateWageTaxPrepTmp**-Method verwenden, um den Wert nach Bedarf zu ändern.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (Klasse)

Die **smmOutlookSync_Contact** Integrationsklasse verknüpft Werte mit und von **Outlook** und **Kontaktpersonen**. **Outlook** unterstützt drei Werte: **Männlich**, **Weiblich**, und **Nicht spezifiziert**. Die Klasse verfügt über zwei Methoden, die Ihnen bei der Zuordnung von **Geschlechter** zu **OutlookGenders** helfen. Die Standardmethode ist **NonSpecific/UnSpecified**. Wenn Sie zusätzliche Werte für die **Gender** Enumeration erstellen, sollten Sie eine Erweiterung erstellen, indem Sie bei Bedarf die Klasse **Befehlskette** verwenden, und Sie beide Methoden erweitern, um neue Werte zuzuordnen, die einer der beiden Basisaufzählungen hinzugefügt werden.
