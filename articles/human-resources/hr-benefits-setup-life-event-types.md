---
title: Lebensereignistypen konfigurieren
description: Microsoft Dynamics 365 Human Resources verwendet Life-Ereignistypen, um Ereignisse zu definieren, bei denen es gültig ist, die Anmeldung für Mitarbeiterleistungen zu aktualisieren.
author: andreabichsel
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 821e11d6ee22cb560b3d23017c7c332f80d41c18
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057645"
---
# <a name="configure-life-event-types"></a>Lebensereignistypen konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources verwendet Lebensereignis-Typen, um Ereignisse zu definieren, bei denen es gültig ist, die Anmeldung für Mitarbeiterleistungen zu aktualisieren, wie z.B. Heirat oder Geburt eines Kindes. Jede Kennung des Lebensereignistyps darf nur einem Lebensereignistyp zugeordnet werden. Wenn Sie beispielsweise eine Kennung eines Lebensereignistyps mit dem Namen „Adressänderung“ erstellen, die dem Lebensereignistyp „Änderung der Mitarbeiteradresse“ zugeordnet ist, können Sie keine andere Kennung mit der Bezeichnung „Änderung der Mitarbeiteradresse“ erstellen und sie dem Lebensereignistyp „Änderung der Mitarbeiteradresse“ zuordnen. Wenn ein Lebensereignistyp nicht mit einem Plantyp verknüpft ist, löst der Lebensereignistyp kein Lebensereignis aus. Weitere Informationen finden Sie unter [Plantypen erstellen](hr-benefits-setup-plan-types.md).

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
| **Änderung des Beschäftigungsstatus** | Arbeitskraft > Beschäftigung<br>Beschäftigungshistorieseite | Für eine Arbeitskraft mit einem bestehenden Beschäftigungsdetail wird das Erstellen eines neuen Beschäftigungsdetail mit einem anderen Beschäftigungsstatus ein Lebensereignis auslösen.  Das Aktualisieren eines vorhandenen Beschäftigungsdetaildatensatzes mit einem anderen Beschäftigungsstatus löst ebenfalls ein Ereignis aus.  |
| **Änderung der Mitarbeiteradresse** | Arbeitskraft > Profil > Adressen<br>Arbeitskraft > Persönliche Informationen > Persönliche Kontakte > Adresse | Änderung der Adresse. Die Adresse muss primär sein, um ein Lebensereignis auszulösen. |
| **Änderung der abhängigen Person** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte<br>Mitarbeiter-Self-Service | Fügen Sie einen persönlichen Kontakt hinzu, indem Sie ihn als abhängig angeben und **Gültig ab** definieren. Aktualisierung der abhängigen **Gültig bis**-Informationen eines persönlichen Kontakts. Die persönliche Kontaktbeziehung muss Kind, Ehepartner, Lebenspartner oder Ex-Ehepartner sein.  |
| **Geburt oder Adoption (Unterhaltsberechtigter)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte<br>Mitarbeiter-Self-Service > Persönliche Daten bearbeiten > Persönliche Kontakte | **Geburtsdatum** oder **Adaptionsdatum** werden hinzugefügt oder aktualisiert. Das **Geburtsdatum** des Untergeordneten ist erforderlich. |
| **Verlust der Abdeckung (Ehepartner/Lebenspartner)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Verlust der Abdeckung | **Verlust der Abdeckung** wurde für einen persönlichen Kontakt ausgewählt, zusammen mit **Gültigkeitsdatum** |
| Beschäftigungsänderung für Lebenspartner | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Abhängige Details > Beschäftigt | Erstellen eines persönlichen Kontakts und Festlegen von **Beschäftigt** auf **Ja**. Aktualisieren eines persönlichen Kontakts und Ändern von **Beschäftigt**.  |
| **Beurlaubung (Ehepartner/Lebenspartner)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Beurlaubung | Persönlicher Kontakt erstellt und **Abwesenheitsdatum** ist definiert. Persönlicher Kontakt **Freistellung** wird aktualisiert. Persönlicher Kontakt **Abwesenheitsdatum** wird aktualisiert.  |
| **Änderung der Abdeckung (Position)** | Arbeitskraft > Positionszuweisung > Positionszuweisungen der Arbeitskraft<br>Positionen > Positionen | Änderung der Position in den Datensätzen für die Zuordnung der Arbeitskräfte zur Position. Änderung der Zuordnung der Arbeitskraft in der Position. |
| **Änderung der Abdeckung (Gehalt)** | Arbeitskraft > Vergütung > Fester Plan<br>Arbeitskraft > Persönliche Informationen > Leistungen Jahresgehalt | Wenn Leistungsmanagement > Gemeinsame Parameter von Human Resources > Leistungen > Jahresgehalt der Leistungen nicht aktiviert ist, erstellt das Aktualisieren von Arbeitskraft > Vergütung > Fester Plan ein Ereignis. Wenn Leistungsmanagement > Gemeinsame Parameter von Human Resources > Leistungen > Jahresgehalt der Leistungen aktiviert ist, erstellt die Aktualisierung von Arbeitskraft > Persönliche Informationen > Jahresgehalt der Leistungen ein Lebensereignis. |
| **Krankenversicherung (Mitarbeiter/Unterhaltsberechtigter)** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigtendetails > Gültigkeitsdatum Krankenversicherung | Das Hinzufügen oder Aktualisieren des **Medicare Gültig**-Datums für einen persönlichen Kontakt erstellt dieses Lebensereignis. |
| **Gerichtlich angeordnete Unterstützung** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte > Unterhaltsberechtigter > Durch Gericht angeordnete Unterstützung (QMSCO/QDRO) und Gültigkeitsdaten | Beim Erstellen eines persönlichen Kontakts wird ein Lebensereignis erstellt, wenn **Gerichtlich angeordnete Unterstützung** **Ja** ist. Das Aktualisieren von **Gerichtlich angeordnete Unterstützung** oder **Gerichtlich angeordnetes Verfallsdatum** löst ebenfalls ein Lebensereignis aus. |
| **Verstorben** | Arbeitskraft > Profil > Persönliche Informationen > Todestag | Ein Verstorbenen-Datum wird eingegeben oder aktualisiert. |
| **Versicherungsnachweis** | Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails | **Versicherungsnachweis** wird auf **Ja** festgelegt. **Datum für den Nachweis der Versicherbarkeit** ist definiert. |
| **Begünstigter** | Arbeitskraft > Profil > Persönliche Informationen > Persönliche Kontakte | Ein persönlicher Kontakt wird hinzugefügt und die Felder **Begünstigter** und **Gültigkeitsdatum** werden ausgefüllt. Der persönliche Kontakt muss vom Typ **Kind**, **Ehepartner**, **Haushaltspartner**, **Geschwister**, **Familienkontakt**, **AndererKontakt** oder **Elternteil** sein. |
| **Mitarbeiter-Krankenversicherung** | Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie > Datumsmanager > Vorteilsdetails | **Medicare-Berechtigung** wird auf **Ja** festgelegt. **Medicare-Berechtigungsdatum** wird geändert. |
| **Geburtstag** | Leistungsverwaltung > Verarbeitung von Lebensereignissen | Diese Lebensereignisse werden von **Life Event Change Processing** erstellt. Der Prozess analysiert den gewählten Zeitraum und die juristische Entität und findet die zugehörigen Arbeitskräfte. Es berechnet den letzten Geburtstag und erstellt ein Geburtstags-Lebensereignis, falls nicht bereits eines erstellt wurde. |
| **Änderung der Arbeitskraftberechtigung (nicht US-spezifisch)** | Arbeitskraft > Beschäftigung<br>Arbeitskraft > Arbeitskraft > Versionen > Beschäftigungshistorie | Erstellt ein Lebensereignis, wenn:<br><ul><li>Erstellen einer neuen Beschäftigung, und es gibt eine frühere Beschäftigung, und der Typ der Arbeitskraft ändert sich.</li><li>Erstellen eines neuen Beschäftigungsdetails, und es gibt ein vorheriges Beschäftigungsdetail, und der Beschäftigungstyp oder die Beschäftigungskategorie ändert sich.</li><li>Aktualisierung eines Beschäftigungsdatensatzes und ein anderer Typ von Arbeitskraft wird festgelegt.</li><li>Aktualisierung eines Datensatzes zur Beschäftigung und Angabe eines anderen Beschäftigungstyps oder einer anderen Kategorie.</li></ul> |
| **Neue Berechtigungsüberschreibung (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung | Lebensereignisverarbeitung verwenden<br>Das Erstellen einer neuen Leistungsplan-Berechtigungsüberschreibung für eine Arbeitskraft löst dieses Lebensereignis aus.<br>BenefitEligibilityRuleOverride.ValidFrom. |
| **Änderung der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Vorteile > Berechtigungsregelüberschreibung | Das Aktualisieren von **Gültig von** oder **Gültig bis** bei einer Leistungsplan-Berechtigungsüberschreibung löst dieses Lebensereignis aus. |
| **Ablauf der Berechtigungsregelüberschreibung (nicht US-spezifisch)** | Leistungsverwaltung > Verarbeitung von Lebensereignissen  | Diese Lebensereignisse werden von **Life Event Change Processing** erstellt. Der Prozess analysiert den gewählten Zeitraum und die juristische Entität und findet die zugehörigen Leistungsplan-Zulassungen. Es erstellt Lebensereignisse, wenn die Überschreibungen abgelaufen sind. |
| **Neuer Vorteilsplan (nicht US-spezifisch)** | Erweiterte Personalverwaltung > Vorteile > Pläne > Neu | Berechtigungsoptionen werden zu einem aktuellen Plan hinzugefügt. Ein neuer Plan mit Berechtigungsoptionen im Anhang wurde hinzugefügt.</br></br>HR-Mitarbeiter sollten in diesem Fall die Verarbeitung der Lebensereignisberechtigung ausführen. |
| **Änderung der Berechtigungsregel (nicht US-spezifisch)** | Leistungsmanagement > Anspruchsregeln | Verarbeitung von Lebensereignisberechtigungen verwenden. Protokolliert, wenn **BenefitEligibilityRule** Datensätze die folgenden Werte geändert haben: **UseEmplCategory**, **UseEmplStatus**, oder **UseEmplType**. Aktualisiert nur Lebensereignistransaktionen, die bereits für eine geänderte Regel oder ein geändertes Berechtigungskriterium vorhanden sind. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]