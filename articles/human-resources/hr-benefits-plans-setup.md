---
title: Vorteilsplan erstellen
description: In diesem Artikel erfahren Sie, wie Sie Vorteilspläne in Dynamics 365 Human Resources einrichten.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c8d4488f1782d80484a8b91f4ae7303fea0e464
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337029"
---
# <a name="create-a-benefit-plan"></a>Vergütungsplan erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel erfahren Sie, wie Sie Vorteilspläne in Dynamics 365 Human Resources einrichten.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie **Neu** aus.

3. Definieren Sie auf der Registerkarte **Allgemeines** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Plan** | Ein eindeutiger Bezeichner für den Plan. |
   | **Beschreibung** | Eine Beschreibung des Plans. |
   | **Typ des Plans** | Wenn Sie einen neuen Plan erstellen, müssen Sie den Plantyp angeben. Ein Plantyp ist eine übergeordnete Gruppierung bestimmter Vorteilstypen. Jeder Plantyp gibt an, ob ein Mitarbeiter sich für mehrere Pläne dieses Typs registrieren kann, gibt an, ob Kontakte Begünstigte oder Unterhaltsberechtigte sind und definiert Abdeckungsoptionen. Sie können neue benutzerdefinierte Plantypen erstellen, um die Anforderungen Ihrer Vorteilsangebote zu erfüllen. Die wichtigsten Typen von Vorteilsplänen sind: <ul><li>401K</li><li>ADD</li><li>Zahnbehandlungs-Zusatzversicherung</li><li>Fitness</li><li>FSA</li><li>Leben</li><li>LTD</li><li>Medizinisch</li><li>PTO</li><li>STD</li><li>Vision</li></ul> |
   | **Code des Plantyps** | Der Plantypcode des Plantyps. |
   | **Programm** | Gibt ein Programm an, dem der Plan optional zugewiesen werden soll. |
   | **Bündel** | Gibt ein Bündel an, dem der Plan optional zugewiesen werden soll. |
   | **Haupt** | Gibt an, ob es sich bei dem Plan um den Produktprogrammplan innerhalb des Bündels handelt, dem es zugewiesen ist. |
   | **Gültig ab Datum und Zeit** | Datum und Uhrzeit des Zeitpunkts, zu dem der Plan startet. Das aktuelle Systemdatum ist der Standardwert. |
   | **Gültig bis Datum und Zeit** | Datum und Uhrzeit des Zeitpunkts, zu dem der Plan endet. Der Standardwert lautet 31.12.2154 (stellvertretend für „endet nie“). |

4. Geben Sie auf der Registerkarte **Konfiguration** Werte für die folgenden Felder an, abhängig vom Plantyp, den Sie erstellen:

   | Typ des Plans | Feld | Beschreibung |
   | --- | --- | --- |
   | Medizinisch (Medizinisch, Zahnbehandlung, Augenbehandlung, HMO) | COBRA | Gibt an, ob der Plan gemäß COBRA (Consolidated Omnibus Budget Reconciliation Act) wählbar ist. |
   | Medizinisch (Medizinisch, Zahnbehandlung, Augenbehandlung, HMO) | HIPAA | Gibt an, ob der Plan gemäß HIPAA (Health Insurance Portability and Accountability Act) wählbar ist. |
   | Medizinisch (Medizinisch, Zahnbehandlung, Augenbehandlung, HMO)<br><br>Sonstiges (PTO, Fitness)<br><br>Sonstige<br><br>Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig)<br><br>Sparen (z. B. 401(k))<br><br>FSA | Zur Vorsteuer berechtigt | Gibt an, ob Beiträge zum Plan geleistet werden können, bevor Steuern angewendet werden. |
   | Medizinisch (Medizinisch, Zahnbehandlung, Augenbehandlung, HMO)<br><br>Sonstiges (PTO, Fitness)<br><br>Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig)<br><br>Sparen (z. B. 401(k))<br><br>FSA | Steuerliche Verwendbarkeit buchen | Gibt an, ob Beiträge zum Plan geleistet werden können, nachdem Steuern angewendet werden. |
   | Medizinisch (Medizinisch, Zahnbehandlung, Augenbehandlung, HMO)<br><br>Sonstiges (PTO, Fitness)<br><br>Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig)<br><br>Sparen (z. B. 401(k))<br><br>FSA | Mitwirkender | Gibt an, wer zum Plan beiträgt – der Mitarbeiter, der Arbeitgeber oder beide. |
   | Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig) | Minimale Deckung | Die für den Plan erforderliche Mindestversicherungssumme. |
   | Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig) | Maximale Deckung | Die für den Plan erforderliche maximale Versicherungssumme. |
   | Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig) | Deckungserhöhungen verwenden | Gibt an, ob überprüft werden soll, ob der Abdeckungsbetrag einem gültigen inkrementellen Betrag entspricht. |
   | Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig) | Zusätzlicher Betrag | Die inkrementelle Versicherungssumme für den Plan. Wenn beispielsweise der inkrementelle Betrag 1.000 beträgt, kann ein Mitarbeiter keine Versicherungssumme von 200.500 Euro haben. Er muss sie auf 201.000 Euro aufrunden oder 200.000 Euro abrunden. |
   | Langfristige Behinderung<br><br>ADD (Leben – Basis, freiwillig) | Erhöhungsrichtung | Gibt die Rundungsrichtung an (entweder nach oben oder nach unten), wenn der Deckungsbetrag den Wert für den inkrementellen Betrag nicht erfüllt. |
   | ADD (Leben – Basis, freiwillig) | Nachweis der Versicherbarkeit | Gibt an, ob ein Mitarbeiter einen Versicherungsnachweis erbringen muss. |
   | ADD (Leben – Basis, freiwillig) | Dauer | Der Betrag in Buchhaltungswährung. Dieses Feld ist nur aktiv, wenn das Kontrollkästchen „Nachweis der Versicherbarkeit“ aktiviert ist. |
   | Sparen (z. B. 401(k))<br><br>FSA | Minimaler jährlicher Beitrag | Der für den Plan erforderliche minimale Beitragsbetrag. |
   | Sparen (z. B. 401(k))<br><br>FSA | Maximaler jährlicher Beitrag | Der für den Plan erforderliche maximale Beitragsbetrag. |
   | Sparen (z. B. 401(k)) | Maximaler jährlicher Betrag des Arbeitgebers | Der Höchstbetrag, den ein Arbeitgeber während einer Vorteilperiode zu einem Sparplan eines Mitarbeiters beitragen darf. Sie müssen das Kontrollkästchen „Arbeitgeberabgleich“ aktivieren, um dieses Feld zu verwenden. |
   | Sparen (z. B. 401(k)) | Arbeitgeberabgleich | Gibt an, ob der Arbeitgeber zum Sparplan eines Mitarbeiters beiträgt. |
   | Sparen (z. B. 401(k)) | Arbeitgeberabgleich in Prozent | Der Prozentsatz eines Mitarbeiterbeitrags, den der Arbeitgeber abgleicht. |
   | Sparen (z. B. 401(k)) | Obergrenze für Arbeitgeberabgleich | Der maximale Prozentsatz, den der Arbeitgeber abgleicht. Wenn ein Arbeitgeber beispielsweise 100 % der Arbeitnehmerbeiträge mit bis zu 6 % des Mitarbeiterlohns abgleicht, beträgt die Obergrenze für den Mitarbeitgeberabgleich 6 %. |

5. Definieren Sie auf der Registerkarte **Einstellungen** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Registrierung zulassen/fortsetzen** | Gibt an, ob Mitarbeiter sich für den Plan registrieren können, wenn sie die Berechtigungsbedingungen erfüllen.</br></br>Wenn dies auf „Nein“ gesetzt ist, steht der Plan den Mitarbeitern nicht zur Verfügung, wenn Sie die Berechtigung verarbeiten. |
   | **Automatische Registrierung aus dem vorherigen Jahr** | Gibt an, ob ein berechtigter Mitarbeiter im Plan automatisch registriert werden soll, wenn er im vorangegangenen Jahr registriert wurde. |
   | **Standardmäßig automatisch registrieren** | Gibt an, ob der Plan standardmäßig für die Registrierung ausgewählt werden soll. Der Plan ist nicht obligatorisch, sodass der Mitarbeiter die Standardauswahl ändern kann. |
   | **Für neue Registrierungen geschlossen** | Gibt an, ob der Plan nur auf berechtigte Mitarbeiter beschränkt werden soll, die im Vorjahr für den Plan registriert waren. |
   | **Obligatorischer Plan** | Gibt an, ob Mitarbeiter automatisch für den Plan registriert werden sollen. Mitarbeiter können die Registrierungsauswahl nicht ändern. |
   | **Anfangsdatum** | Das Datum, an dem der Plan im Unternehmen erstellt wurde. |
   | **Lieferantenkonto** (Leistungserbringer) | Der Kreditor, an den das Unternehmen die Prämien für den Plan zahlt. |
   | **Name** (Leistungserbringer) | Der Name des Kreditors. |
   | **Kreditorreferenz** (Leistungserbringer) | Die Referenz des Kreditors für den Plan. Zum Beispiel die Gruppenplannummer des Unternehmens. |
   | **Alternative Referenz** (Leistungserbringer) | Die alternative Referenz des Kreditors für den Plan. Zum Beispiel die Kontonummer des Unternehmens. |
   | **Währung** (Leistungserbringer) | Die Währung, in der die Prämien an den Erbringer gezahlt werden. |
   | **Ausgabenkonto** (Leistungserbringer) | Das Hauptbuchkonto, das als Ausgabenkonto für Planprämien verwendet wird. |
   | **Kreditorenkonto** (Vorteilsadministrator) | Der Lieferant, den das Unternehmen für die Verwaltung des Plans zahlt. Wenn der Plan selbst verwaltet wird, lassen Sie dieses Feld leer. |
   | **Name** (Vorteilsadministrator) | Der Name des Vorteilsadministrators. |
   | **Lieferantenreferenz** (Vorteilsadministrator) | Die Referenz des Vorteilsadministrators für den Plan. |
   | **Alternative Referenz** (Vorteilsadministrator) | Die alternative Referenz des Vorteilsadministrators für den Plan. |
   | **Währung** (Vorteilsadministrator) | Die Währung, in der der Vorteilsadministrator gezahlt wird. |
   | **Ausgabenkonto** (Vorteilsadministrator) | Das Hauptbuchkonto, das als Ausgabenkonto für die Kosten verwendet wird, die mit der Planverwaltung zusammenhängen. |

6. Wählen Sie auf der Registerkarte **Filter** nach Bedarf Filter aus. Sie können nach folgenden Feldern filtern:

   - **Unternehmenseinheit**
   - **Abteilung**
   - **Juristische Person**
   - **Elektronische Adresse**
   - **Position**

7. Definieren Sie auf der Registerkarte **Berechtigungsregeln** die Werte für die folgenden Felder:

   | Feld | Beschreibung |
   | --- | --- |
   | **Positionsnummer** | Positionsnummer der Berechtigungsregel. |
   | **Berechtigungsregel** | Eine Berechtigungsregel, die für den Vorteilsplan gilt. Diese Berechtigungsregel wird auf den entsprechenden Vorgangstyp angewendet und mit der angegebenen Abdeckungs‑ und Abzugswarteperiode verknüpft. |
   | **Vorgangstyp** | Die Aktivität zum Anwenden der Berechtigungsregel auf: Vorteilsregistrierung oder Vorteilsablauf. |
   | **Abdeckungswarteperiode** | Ein Wert aus dem Formular „Wartezeiten“. Die Abdeckungswarteperiode bestimmt die Anzahl der Tage oder Monate, die ein Mitarbeiter auf die Vorteilsabdeckung oder den Vorteilsablauf wartet, basierend auf den Kriterien in der Berechtigungsregel und dem Vorgangstyp. |
   | **Abzugswarteperiode** | Ein Wert aus dem Formular „Wartezeiten“. Die Abzugswarteperiode bestimmt die Anzahl der Tage oder Monate, die ein Mitarbeiter auf den Vorteilsabzug vom Lohnscheck wartet, basierend auf den Kriterien in der Berechtigungsregel und dem Vorgangstyp. |

8. Wählen Sie **Speichern**.

## <a name="view-enrolled-workers"></a>Registrierte Arbeitskräfte anzeigen

Sie können Arbeitskräfte anzeigen, die für einen ausgewählten Vorteilsplan registriert sind.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie auf der Registerkarte **Vergütungen** in der Navigationsleiste **Registrierte Arbeitskräfte**.

## <a name="attach-coverage-options"></a>Abdeckungsoptionen anhängen

Sie können dem ausgewählten Vorteilsplan Abdeckungsoptionen hinzufügen. Durch das Anhängen von Abdeckungsoptionen werden die Satz‑ und Abzugseinstellungen für eine Abdeckungsoption zusammengefasst.  Beispiel: Für einen Krankenversicherungsplan wählt der Benutzer eine Familienversicherungsoption aus.  Sie müssten dann den Familiensatz für den zugeordneten Plan (in der Satzeinstellung festgelegt) und den Abzug für den zugeordneten Plan (in der Satzeinstellung festgelegt) auswählen. Dies liefert die Kosten für den Arbeitgeber und den Mitarbeiter für eine ausgewählte Abdeckung. Anschließend wiederholen Sie den Vorgang für eine Mitarbeiter+1-Abdeckung oder eine Mitarbeiterabdeckung.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie auf der Registerkarte **Vergütungen** in der Navigationsleiste **Abdeckungsoptionen anhängen**.

## <a name="override-eligibility-rules"></a>Berechtigungsregeln überschreiben

Sie können Arbeitskräfte als Ausnahmen zu den Berechtigungsregeln zu einem Plan hinzufügen. Jede Arbeitskraft, die Sie hinzufügen, hat Anspruch auf den Vorteilsplan.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie auf der Registerkarte **Vergütungen** in der Navigationsleiste **Berechtigungsregelüberschreibung**.

## <a name="view-attached-periods"></a>Angehängte Perioden anzeigen

Sie können eine Liste der verfügbaren Vorteilsperioden anzeigen.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie in der Navigationsleiste die Registerkarte **Perioden** aus.

## <a name="view-plan-description"></a>Planbeschreibung anzeigen

Sie können eine Beschreibung des Plans bereitstellen, um den Mitarbeitern bei der Auswahl ihrer Vorteile zu helfen. Die Planbeschreibung, die Sie hier eingeben, wird im Mitarbeiter-Self-Service angezeigt, wenn Sie den Mauszeiger über den Plan in der Liste der Abdeckungsoptionen bewegen.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie auf der Registerkarte **Vergütungen** in der Navigationsleiste **Planbeschreibung**.

## <a name="view-flex-credit-programs"></a>Flexible Gutschriftenprogramme anzeigen

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Pläne** die Option **Vorteilspläne**.

2. Wählen Sie auf der Registerkarte **Vergütungen** in der Navigationsleiste **Programme für flexible Kredite**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
