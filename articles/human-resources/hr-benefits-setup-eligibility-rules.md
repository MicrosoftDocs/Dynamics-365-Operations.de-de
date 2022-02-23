---
title: Berechtigungsregeln und -optionen konfigurieren
description: Legen Sie die Berechtigungsregeln und ‑optionen in der Vorteilsverwaltung von Microsoft Dynamics 365 Human Resources fest.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70054acafc3aec35fd985c0ca81e928519ddd0a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418628"
---
# <a name="configure-eligibility-rules-and-options"></a>Berechtigungsregeln und -optionen konfigurieren

Nachdem Sie die erforderlichen Parameter für die Vorteilsverwaltung in Microsoft Dynamics 365 Human Resources konfiguriert haben, können Sie Berechtigungsregeln, Bündel, Perioden und Programme erstellen, die Sie mit Ihren Vorteilsplänen verknüpfen.

## <a name="create-an-eligibility-rule"></a>Berechtigungsregel erstellen

Die Berechtigungsregeln legen fest, welche Mitarbeiter sich für die einzelnen Vorteilspläne registrieren können. Nachdem Sie die Berechtigungsregeln definiert haben, ordnen Sie sie Vorteilsplänen zu. Anschließend können Sie die Registrierungsberechtigung verarbeiten, um zu sehen, welche Mitarbeiter für die einzelnen Pläne berechtigt sind. 

Während der offenen Registrierung können Mitarbeiter Vorteilspläne auswählen. Wenn sie nach der Registrierung aufgrund der Berechtigungsregeln nicht mehr für einen Vorteilsplan infrage kommen, wird die Registrierung nicht automatisch rückgängig gemacht. Wenn ein Lebensereignis eintritt, das sich auf die Planberechtigung auswirkt, wird in der Regel eine Registrierungsperiode eingeleitet, in der der Mitarbeiter Pläne auswählen kann, für die er berechtigt ist. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Berechtigungsregeln** die Option **Neu** aus, um eine Berechtigungsregel zu erstellen. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einer Berechtigungsregel verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Berechtigungsregel** | Ein eindeutiger Bezeichner für die Berechtigungsregel. |
   | **Beschreibung** | Eine Beschreibung der Berechtigungsregel. |
   | **Gültig ab Datum und Zeit** | Das Startdatum der Berechtigungsregel. | 
   | **Gültig bis Datum und Zeit** | Das Enddatum der Berechtigungsregel. |
   | **Mitarbeitertyp verwenden** | Gibt an, ob für den Mitarbeitertyp des Mitarbeiters die Vorteilsberechtigungsregel verwendet werden soll. |
   | **Arbeitskrafttyp** | Der Arbeitskrafttyp, wenn die Umschaltfläche **Mitarbeitertyp verwenden** auf **Ja** eingestellt ist. |
   | **Mitarbeiterstatus verwenden** | Gibt an, ob für den Mitarbeiterstatus des Mitarbeiters die Vorteilsberechtigungsregel verwendet werden soll. |
   | **Status** | Der Mitarbeiterstatus, wenn die Umschaltfläche **Mitarbeiterstatus verwenden** auf **Ja** eingestellt ist. Wenn die Umschaltfläche **Mitarbeiterstatus verwenden** auf **Nein** eingestellt ist, wird das Feld nicht verwendet. |
   | **Beschäftigungskategorie verwenden** | Gibt an, ob die **Beschäftigungskategorie** des Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. | 
   | **Beschäftigungskategorie** | Die Beschäftigungskategorie des Mitarbeiters, wenn die Umschaltfläche **Beschäftigungskategorie verwenden** ist auf **Ja** eingestellt ist. |
   | **Neue Einstellungsregel verwenden** | Gibt an, ob der neue Einstellungsperiodenwert des neuen Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. |
   | **Registrierungsperiode** | Die Periode, für die die Registrierung einer Neueinstellung zulässig ist. Wenn Sie dies auch in Parametern einstellen, hat die Parametereinstellung Vorrang. |
   | **Ehemaligen Beschäftigungsstatus verwenden** | Gibt an, ob der frühere Beschäftigungsstatus eines Mitarbeiters als Teil der Vorteilsberechtigungsregel verwendet werden soll. Beispielsweise können Sie eine Berechtigungsregel angeben, die auf eine Deckungswartezeit für alle Mitarbeiter verzichtet, die vom Status **Entlassen** zu einem Status **Beschäftigt** innerhalb von 90 Tagen nach ihrer vorherigen Beschäftigung gewechselt haben. |

4. Wählen Sie unter **Zusätzliche Kriterien** die folgenden Optionen aus und fügen Sie nach Bedarf Informationen hinzu:

   | Option | Beschreibung |
   | --- | --- |
   | **Zulässiges Alter** | Gibt den Altersbereich oder die Altersbereiche an, die erforderlich sind, um die Berechtigungsregel zu erfüllen. |
   | **Zulässige Abteilung** | Gibt die Abteilung oder Abteilungen an, in denen sich ein Mitarbeiter befinden muss, um die Berechtigungsregel zu erfüllen. |
   | **Zulässiger Beschäftigungstyp** | Gibt den Beschäftigungstyp oder die Beschäftigungstypen an, unter den/die ein Mitarbeiter fallen muss, um die Berechtigungsregel zu erfüllen. Beispiel: Vollzeit oder Teilzeit. |
   | **Zulässige Stelle** | Gibt die Stelle oder Stellen an, die die Berechtigungsregel erfüllen. Stellen sind mit Positionen verbunden und Positionen werden von Mitarbeitern besetzt. |
   | **Zugelassene Stellenfunktion** | Gibt die Stellenfunktion oder Stellenfunktionen an, die eine Berechtigungsregel erfüllen. Beispiel: Vertriebskraft oder Techniker. |
   | **Zulässiger Stellentyp** | Gibt den Stellentyp oder die Stellentypen an, die die Berechtigungsregel erfüllen. Beispiel: Bürotätigkeit oder Führungskraft. |
   | **Zulässige juristische Person** | Gibt die juristische Person oder die juristischen Personen an, die für die Berechtigungsregel zulässig sind. Beispiel: Contoso Entertainment System USA. |
   | **Region für Vergütungsberechtigung** | Gibt den Standort des Mitarbeiters an, der die Berechtigungsregel erfüllt. Beispiel: USA, Mitte. |
   | **Zulässige Position** | Gibt die Position oder die Positionen an, die die Berechtigungsregel erfüllen. Beispiel: HR Assistant oder HR Manager. |
   | **Zulässiger Positionstyp** | Gibt den Positionstyp oder die Positionstypen an, die die Berechtigungsregel erfüllen. Beispiel: Vollzeit. |
   | **Zulässigers** | Gibt die Bundesländer oder Kantone an, die die Berechtigungsregel erfüllen. Beispiel: Sachsen, Deutschland oder Wallis, Schweiz. |
   | **Zulässige Beschäftigungsbedingungen** | Gibt die Beschäftigungsbedingung an, die die Berechtigungsregel erfüllt. Beispiel: beliebig oder Gruppenvertrag. |
   | **Zulässige Gewerkschaft** | Gibt die Mitgliedschaft bei Gewerkschaften an, die die Berechtigungsregel erfüllen. Beispiel: IG Metall. </br></br>Bei Verwendung einer gewerkschaftsbasierten Berechtigungsregel muss das Enddatum des Gewerkschaftsdatensatzes der Arbeitskraft angegeben werden. Sie können es nicht leer lassen. |
   | **Zulässige Postleitzahl** | Gibt die Postleitzahlen an, die die Berechtigungsregel erfüllen. Beispiel: 58104. |

5. Unter **Zusätzliches Detail** können Sie die folgenden zusätzlichen Details anzeigen:

   | Feld | Beschreibung |
   | --- | --- |
   | **Zulässiges Benutzerfeld** | Gibt zusätzliche Berechtigungsregeln basierend auf benutzerdefinierten Feldern an. |
   | **Berechtigungstyp** | Gibt die Kriterienkategorie an, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |
   | **Berechtigungsreferenz** | Gibt die Werte an, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |
   | **Beschreibung** | Die Beschreibung, die Sie unter **Zusätzliche Kriterien** ausgewählt haben. |

6. Wählen Sie **Speichern**.

## <a name="configure-bundles"></a>Bündel konfigurieren

Bündel sind ein Satz verwandter Vorteilspläne. Sie können Vorteilsbündel verwenden, um Vorteilspläne zu gruppieren, die ein Mitarbeiter auswählen muss, um sich für bestimmte Vorteilspläne anzumelden, die möglicherweise von anderen Vorteilsplanregistrierungen abhängig sind. Beispiele dafür, wann Sie ein Bündel verwenden sollten:

- Ein Krankenversicherungsbündel , das eine Krankenversicherung mit hohem Selbstbehalt und einem dazugehörigen Gesundheitssparkonto (Health Savings Account, HSA) umfasst.

- Eine Lebensversicherungsplan mit einem obligatorischen Lebensversicherungsplan für Mitarbeiter in einem Bündel mit einem Lebensversicherungsplan für Unterhaltsberechtigte. Dies würde sicherstellen, dass ein Mitarbeiter keine Lebensversicherung für Unterhaltsberechtigte auswählen kann, ohne sich für die Mitarbeiterlebensversicherung zu registrieren.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Bündel** die Option **Neu** aus, um ein Bündel zu erstellen. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Bündel verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Bündel** | Ein eindeutiger Bezeichner für das Bündel. |
   | **Beschreibung** | Eine Beschreibung des Bündels. |
   | **Haupt** | Gibt an, ob einer der Pläne im Bündel als Produktprogrammplan gekennzeichnet sein muss. Der Produktprogrammplan muss während der offenen Registrierung als Teil des Bündels ausgewählt werden, bevor der Vorteilsadministrator die Vorteilswahlen des Mitarbeiters bestätigen kann. |
   | **Gültig ab Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Bündel aktiv wird. |
   | **Gültig bis** | Das Datum, an dem das Bündel abläuft. Der Standardwert lautet 31.12.2154 (stellvertretend für nie). |

4. Wählen Sie **Speichern**.

## <a name="configure-periods"></a>Perioden konfigurieren

In den Perioden wird festgelegt, wann die Vorteile in Kraft sind und wann sich Mitarbeiter registrieren dürfen. Sie können so viele Perioden erstellen, wie Sie möchten, um die offenen Registrierungs‑ und VorteilsabdeckungsPerioden beizubehalten. Die Jahre des Vorteilsplans können einem Kalenderjahr entsprechen oder nicht. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Perioden** die Option **Neu** aus, um eine Periode zu erstellen. Um einen Prozess auszuführen, der alle gültigen aktiven Vorteilspläne mit der Vorteilsperiode verknüpft, wählen Sie **Pläne anhängen**. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Bündel verknüpft sind. 

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Periode** | Der eindeutige Bezeichner für die Periode. |
   | **Gültig ab Datum und Zeit** | Das Startdatum und die Uhrzeit, zu der die Vorteilsperiode aktiv wird. |
   | **Gültig bis Datum und Zeit** | Das Datum und die Uhrzeit, ab denen die Vorteilsperiode inaktiv wird. |
   | **Start der Registrierung** | Das Anfangsdatum für die offene Registrierung. Bei einer offenen Registrierung kann ein Mitarbeiter in Self-Service-Vorteilen seine Vorteile auswählen. |
   | **Ende der Registrierung** | Das Enddatum für die offene Registrierung. |
   | **Öffnen** | Gibt an, ob die Periode offen ist, basierend auf dem Systemdatum und den Daten und Uhrzeiten für „Gültig ab“ und „Gültig bis“. | 
   | **Vorherige Periode** | Gibt die Vorteilsperiode an, die der ausgewählten Vorteilsperiode vorausgeht. Diese Informationen werden während der Vorteilsberechtigungsregistrierung verwendet, um Pläne, Abdeckungsoptionen und Beauftragte aus einem früheren Jahr zuzuweisen. |
 
4. Wählen Sie **Speichern**.

## <a name="use-a-flex-credit-program"></a>Flexguthabenprogramm verwenden

Sie können Flexguthabenprogramme verwenden, um Mitarbeiter für Vorteile gemäß einer festgelegten Höhe von Flexguthaben zu registrieren. Mitarbeiter können wählen, wie sie ihr Flexguthaben zuordnen möchten. Wenn ein Mitarbeiter beispielsweise in der Krankenversicherung seines Ehepartners mitversichert ist, möchte er möglicherweise das Guthaben, das er sonst für die Krankenversicherung verwendet hätte, für andere Vorteile verwenden.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie auf der Registerkarte **Perioden** die Option **Flexguthabenprogramme**.

3. Wählen Sie ein zu übernehmendes Flexguthabenprogramm aus. Die Felder enthalten die folgenden Informationen:

   | Feld | Beschreibung |
   | --- | --- |
   | Vergütungsgutschriftenkennung | Der eindeutige Bezeichner des Flexguthabenprogramms. |
   | Beschreibung | Eine Beschreibung des Flexguthabenprogramms. | 
   | Anfangsdatum | Das Datum, an dem das Flexguthabenprogramm aktiv wird. |
   | Enddatum | Das Enddatum des Flexguthabenprogramms. Sie können den Standardwert (31.12.2154) beibehalten, um anzugeben, dass für das Flexguthabenprogramm kein geplanter Ablauf festgelegt ist. |
   | Guthabenwert gesamt | Die Höhe des Guthabens, das jeder Mitarbeiter für seine Vorteile verwenden muss. |
   | Regel zur anteiligen Verrechnung | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn ein Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt wird. </br></br><ul><li>**Kein** – Der Mitarbeiter erhält kein Flexguthaben, wenn er nach dem Start des Flexguthabenprogramms eingestellt wird.</li><li>**Volles Guthaben** – Der Mitarbeiter erhält die volle Höhe des Flexguthabens, unabhängig davon, wann er eingestellt wird.</li><li>**Anteilige Verrechnung** – Der Mitarbeiter erhält einen Anteil des Flexguthabens, das auf seinem Startdatum basiert.</li></ul> |
   | Formel für anteilige Berechnung des Flexguthabens | Die Regel zur anteiligen Verrechnung von Flexguthaben, wenn Mitarbeiter in der Mitte der Flexguthabenperiode eingestellt werden. Die anteilige Verrechnung basiert auf dem Einstellungsbeginn. Dieses Feld wird nur verwendet, wenn im Feld **Regel zur anteiligen Verrechnung** die Option **Anteilige Verrechnung** ausgewählt wird. </br></br><ul><li>**Täglich** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Tageslevel. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Tage in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 400 Tage beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 400, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Tag erhält.</li><li>**Aktueller Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den aktuellen Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li><li>**Folgender Monat** – Teilt die Höhe des Flexguthabens, die ein Mitarbeiter erhält, auf dem Monatslevel, auf den nächsten Monat gerundet. Die Gesamthöhe des Flexguthabens wird durch die Anzahl der Monate in der Periode geteilt. Wenn Ihre Vorteilsperiode beispielsweise 15 Monate beträgt, dividiert das System die Gesamthöhe des Flexguthabens durch 15, um die Höhe des Flexguthabens zu berechnen, das ein Mitarbeiter pro Monat erhält.</li></ul> |
   
   Stellen Sie sicher, dass jeder Vorteilsplan nur für ein Flexguthabenprogramm pro Vorteilsperiode registriert ist. Andernfalls weiß das System nicht, mit welchem Flexguthabenprogramm das Flexguthaben vergeben werden soll und es treten Probleme auf. 

## <a name="configure-programs"></a>Programme konfigurieren

Bei Programmen handelt es sich um eine Reihe von Vorteilsplänen, für die gemeinsame Berechtigungsregeln gelten. Sie können Berechtigungsregeln für das gesamte Programm anstatt für jeden einzelnen Plan definieren. Beispiel: ein FTE-Programm von Contoso Canada oder ein Führungskräfteprogramm von Contoso Europe. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsregeln und -optionen**.

2. Wählen Sie in der Registerkarte **Programme** die Option **Neu** aus, um ein Programm zu erstellen. Um Ausnahmen für Mitarbeiter zu machen, die die Anforderungen der Berechtigungsregeln nicht erfüllen, wählen Sie **Berechtigungsregelüberschreibung**. Wählen Sie **Angefügte Pläne** aus, um Pläne anzuzeigen, die mit einem Programm verknüpft sind.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Programm** | Der eindeutige Bezeichner für das Programm. |
   | **Beschreibung** | Eine Beschreibung des Programms. | 
   | **Gültig ab Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Programm aktiv wird. |
   | **Gültig bis Datum und Zeit** | Das Datum und die Uhrzeit, an dem das Programm abläuft. Der Standardwert lautet 31.12.2154 (stellvertretend für nie). |
   | **Abdeckungswarteperiode** | Die Periode, die ein Mitarbeiter warten muss, bevor die Abdeckung für das Vorteilsprogramm beginnt. |
   | **Abzugswarteperiode** | Die Periode, die ein Mitarbeiter wartet, bevor Abzüge für das Vorteilsprogramm beginnen. |
   | **Berechtigungsregeln** | Wählen Sie die Berechtigungsregeln aus, die für das Vorteilsprogramm gelten sollen. Sie definieren die Berechtigungsregeln auf der Registerkarte **Berechtigungsregeln** auf dieser Seite. |
   
4. Wählen Sie **Speichern**.
