---
title: Lebensereignistypen konfigurieren
description: Microsoft Dynamics 365 Human Resources verwendet Lebensereignistypen, um Ereignisse zu definieren, bei denen eine Vorteilsregistrierung von Mitarbeitern aktualisiert werden muss.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5286bcd940f4068531bae624876c8a35e64db4c3
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741485"
---
# <a name="configure-life-event-types"></a>Lebensereignistypen konfigurieren

Microsoft Dynamics 365 Human Resources verwendet die Lebensereignistypen, um Ereignisse zu definieren, bei denen eine Vorteilsregistrierung von Mitarbeitern aktualisiert werden muss. Beispiel: Heirat oder Geburt eines Kindes. Jede Kennung des Lebensereignistyps darf nur einem Lebensereignistyp zugeordnet werden. Wenn Sie beispielsweise eine Kennung eines Lebensereignistyps mit dem Namen „Adressänderung“ erstellen, die dem Lebensereignistyp „Änderung der Mitarbeiteradresse“ zugeordnet ist, können Sie keine andere Kennung mit der Bezeichnung „Änderung der Mitarbeiteradresse“ erstellen und sie dem Lebensereignistyp „Änderung der Mitarbeiteradresse“ zuordnen. 

Nachdem Sie Lebensereignistypen erstellt haben, müssen Sie sie mit Plantypen verknüpfen. Weitere Informationen finden Sie unter [Plantypen erstellen](hr-benefits-setup-plan-types.md).

   > [!NOTE]
   > Wenn Sie einen Lebensereignistypen erstellt haben, müssen Sie ihn mit einem Plantypen verknüpfen. Weitere Informationen finden Sie unter [Plantypen erstellen](hr-benefits-setup-life-event-types.md).

## <a name="create-a-life-event-type"></a>Lebensereignistyp erstellen

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Lebensereignistypen**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Kennung des Lebensereignistyps** | Der eindeutige Bezeichner für den Lebensereignistyp. |
   | **Beschreibung** | Eine Beschreibung des Lebensereignistyps. |
   | **Lebensereignistyp** | Ein Katalysator für die Aktualisierung der Vorteilsregistrierung eines Mitarbeiters. Eine Liste der Lebensereignisse finden Sie unter [Lebensereignisse](hr-benefits-setup-payment-frequencies.md?life-events) unten. |

4. Wählen Sie **Speichern**.

## <a name="view-attached-plans"></a>Angefügte Pläne anzeigen

Sie können eine Liste der Pläne anzeigen, die dem ausgewählten Lebensereignistyp zugeordnet sind. Lebensereignisse sind an einen Plantyp gebunden und Plantypen sind mit einem Plan verknüpft. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Lebensereignistypen**.

2. Wählen Sie **Aktivitäten**.

3. Wählen Sie **Angefügte Pläne**.

## <a name="life-events"></a>Lebensereignisse

Sie können beim Erstellen eines Lebensereignistyps aus den folgenden Lebensereignissen auswählen:

| Lebensereignis | Elektronische Adresse | Auslöser |
| --- | --- | --- |
| **Änderung des Familienstands** | Arbeitskraft > Profil > Persönliche Informationen > Familienstand| Änderung des Familienstandes |
| **Änderung des Beschäftigungsstatus** | <ul><li>Arbeitskraft > Beschäftigung</li><li>Beschäftigungshistorieseite</li></ul> | Änderung des Beschäftigungsstatus |
| **Änderung der Mitarbeiteradresse** | <ul><li>Arbeitskraft > Profil > Adressen </li><li>Arbeitskraft > Persönliche Informationen > Persönliche Kontakte > Adresse</li></ul> Adresse hinzufügen, bearbeiten oder löschen |
| **Änderung der abhängigen Person** | <ul><li>Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigten hinzufügen oder löschen</li><li>Mitarbeiter-Self-Service</li></ul> | Unterhaltsberechtigten hinzufügen oder löschen. Die persönliche Kontaktbeziehung muss Kind, Ehepartner, Lebenspartner oder Ex-Ehepartner sein. Das Aktualisieren des Datums **Gültig ab** löst das Lebensereignis aus. Wenn Sie dieses Datum nicht aktualisieren, wird kein Lebensereignis ausgelöst. |
| **Geburt oder Adoption (Unterhaltsberechtigter)** | <ul><li>Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails</li><li>Mitarbeiter-Self-Service</li></ul> | Feld **Adoptionsdatum** wurde ausgefüllt. Das Geburtsdatum des Kindes ist erforderlich. |
| **Verlust der Abdeckung (Ehepartner/Lebenspartner)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Verlust der Abdeckung | **Verlust der Abdeckung** wurde für einen persönlichen Kontakt ausgewählt, zusammen mit **Gültigkeitsdatum** |
| Beschäftigungsänderung für Lebenspartner | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Eingestellt. | <ul><li>Datensatz mit Unterhaltsberechtigtendetails wurde erstellt und Kontrollkästchen **Persönlicher Kontakt eingestellt** = Ja</li><li>Kontrollkästchen **Persönlicher Kontakt eingestellt** wurde geändert (Ja oder Nein)</li></ul> |
| **Beurlaubung (Ehepartner/Lebenspartner)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Beurlaubung | <ul><li>Datensatz mit Unterhaltsberechtigtendetails wurde erstellt und **EhrLOAEffectiveDate** wurde ausgefüllt</li><li>**personPrivateDetails.EhrIsLOA** wurde geändert (Ja oder Nein)</li><li>**personPrivateDetails.EhrLOAEffectiveDate** wurde geändert</li></ul> |
| **Änderung der Abdeckung (Position)** | <ul><li>Arbeitskraft > Positionszuweisung > Positionszuweisungen der Arbeitskraft</li><li>Positionen > Positionen</li></ul> | <ul><li>Zur Position in den Arbeitskraftpositionszuweisungsdatensätzen wechseln</li><li>Arbeitskraftzuweisung in der Position ändern</li></ul> |
| **Krankenversicherung (Mitarbeiter/Unterhaltsberechtigter)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Gültigkeitsdatum Krankenversicherung | Wird nicht automatisch ausgelöst, wenn ein persönlicher Kontakt ein Gültigkeitsdatum eingibt. |
| **Gerichtlich angeordnete Unterstützung** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigter > Durch Gericht angeordnete Unterstützung (QMSCO/QDRO) und Gültigkeitsdaten | Löst keine automatischen Aktualisierungen aus. Dies hat keinen Einfluss auf die Berechtigung. Es zeichnet ein Lebensereignis auf. |
| **Verstorben** | Arbeitskraft > Profil > Persönliche Informationen > Todestag | Ein Todestag wird eingegeben |
| **Versicherungsnachweis** | <ul><li>Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails</li><li> Arbeitskraft > Beschäftigung > Vorteilsdetails > Überprüfungsdatum</li></ul> | <ul><li>Eine Arbeitskraft gibt ein Überprüfungsdatum ein</li><li>Eine Arbeitskraft setzt das Feld „EvidenceOfInsurability“ auf **Ja**</li></ul> |
| **Begünstigter** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte | Ein persönlicher Kontakt wird hinzugefügt und die Felder **Begünstigter** und **Gültigkeitsdatum** werden ausgefüllt. Der persönliche Kontakt muss einer der folgenden Typen sein: **Kind**, **Ehepartner**, **Lebenspartner**, **Geschwister**, **Familienkontakt**, **Sonstiger Kontakt**, **Elternteil**, **Begünstigter – Vermögen**, **Begünstigter – Organisation** oder **Begünstigter – Treuhänderschaft**. |
| **Mitarbeiter-Krankenversicherung** | Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails | <ul><li>**EhrMedicareEligibilityDate** wurde geändert</li><li>**MedicareEligibile** ist eingestellt auf **Ja**</li></ul> |
| **Geburtstag** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Geburtsdatum | Ein Geburtsdatum wird hinzugefügt oder aktualisiert (nicht nach der Verarbeitung von Lebensereignisänderungen). Beispiel: Wenn in den **Berechtigungsoptionen für persönliche Kontakte** für ein Kind unter Einstellung > Vorteile > Berechtigungsoptionen für persönliche Kontakte das Alter auf 26 festgelegt wurde und ein HR-Mitarbeiter nach dem 26. Geburtstag des Unterhaltsberechtigten die Verarbeitung von Lebensereignisänderungen ausführt, wird eine Meldung angezeigt, dass der Unterhaltsberechtigte nicht mehr abdeckungsberechtigt ist. |
| **Änderung der Arbeitskraftberechtigung (nicht US-spezifisch)** | <ul><li>Arbeitskraft > Beschäftigung</li><li>Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie</li></ul> | <ul><li>Mitarbeitertyp, Beschäftigungskategorie oder die fünf benutzerdefinierbaren Berechtigungsfelder werden geändert</li><li>**HcmEmploymentDetail.EhrEmploymentType** wurde geändert (nur verarbeitet für *geänderte* Beschäftigungsdetaildatensätze, nicht verarbeitet für *neue* Beschäftigungsdatensätze wie Wiedereinstellung und Kündigung)</li></ul> |
| **Neue Berechtigungsüberschreibung (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung | Lebensereignisverarbeitung verwenden | EhrBenefitEligibilityRuleOverride.ValidFrom |
| **Änderung der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung | Lebensereignisverarbeitung verwenden (erfasst nur Änderungen der Felder **Gültig ab** und **Gültig bis** in „Berechtigungsregeln überschreiben“) |
| **Ablauf der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung | Verarbeitung von Lebensereignisänderungen verwenden. Wenn Sie beispielsweise das Ablaufdatum für die Berechtigungsregelüberschreibung eines Plans auf heute um 17:00 Uhr setzen, wird nach 17:00 Uhr des heutigen oder an allen folgenden Tagen bei der Verarbeitung von Lebensereignisänderungen eine Meldung mit dem Hinweis angezeigt, dass die Berechtigungsregelüberschreibung nun abgelaufen ist. |
| **Neuer Vorteilsplan (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Neu | <ul><li>Berechtigungsoptionen werden zu einem aktuellen Plan hinzugefügt</li><li>Ein neuer Plan mit Berechtigungsoptionen wurde hinzugefügt</li></ul></br></br>HR-Mitarbeiter sollten in diesem Fall die Verarbeitung der Lebensereignisberechtigung ausführen. |
| **Änderung der Berechtigungsregel (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Regeln/Optionen > Berechtigungsregeln | Verarbeitung von Lebensereignisberechtigungen verwenden. Wird protokolliert, wenn bei den **EhrBenefitEligibilityRule**-Datensätzen die folgenden Werte geändert werden: **UseEmplCategory**, **UseEmplStatus** oder **UseEmplType**. Aktualisiert nur Lebensereignistransaktionen, die bereits für eine geänderte Regel oder ein geändertes Berechtigungskriterium vorhanden sind. |
