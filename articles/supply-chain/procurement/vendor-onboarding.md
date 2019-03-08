---
title: Kreditoren aufnehmen
description: In diesem Thema wird der Prozess beschreiben, durch den neue Kreditoren aufgenommen werden. Es werden die Aktivitäten erklärt, die während des Prozesses von verschiedenen Rollen erforderlich sind.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 5fda191a41300eea7f3036af54852857d8ff653d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "322144"
---
# <a name="onboard-vendors"></a>Kreditoren aufnehmen
[!include [banner](../includes/banner.md)]

---

Neue Kreditoren können als Kreditoren in Microsoft Dynamics 365 for Finance and Operations aufgenommen und registriert werden, basierend auf Informationen, die von einer Person gesammelt werden, die den Kreditor darstellt.

Der Prozess besteht aus den folgenden Schritten, in denen verschiedene Rollen Aktivitäten im System ausführen.

1. **OData zur Datenverwaltung** – Entitätsimport – Die ursprüngliche Anforderung ist die Registrierungsanforderung des künftigen Kreditors. Normalerweise kommt diese Anforderung von eine Quelle, wie von einer durch einen Debitor gehostete Website, die den anonymen Zugriff zulässt. Kreditoren können sich registrieren, indem sie grundlegende Informationen bereitstellen, wie z. B. Kreditorenname, Begründung, Organisationsnummer sowie Name und E-Mail-Adersse der Kontaktperson. Die Anforderungen werden über die Datenverwaltungsschnittstelle importiert.
2. **Registrierungsanforderungen-Listenseite für künftigen Kreditor** – Auf Grundlage von Daten, die in der Registerierungsanforderung des künftigen Kreditors bereitgestellt werden, entscheidet ein Prokurist, ob der Kreditor aufgenommen werden soll. Der Prokurist zeigt die eingehende Anforderung auf der Listenseite **Registrierungsanforderungen des künftigen Kreditors** in Finance and Operations an.
3. **Benutzerbereitstellungsworkflow** – Wenn ein Prokurist die Informationen in der eingehenden Anforderung überprüft hat und entschieden hat, mit dem Aufnahmeprozess fortzufahren, stellt der Anfoderungsbenutzerworkflow den neuen Benutzer bereit und sendet eine Einladungs-E-Mail, um die Kontaktperson als einen authentifizierten Benutzer von Microsoft Dynamics 365 zu akzeptieren.
4. **Kreditorenregistrierungs-Assistent** – Die Kontaktperson des Kreditors meldet sich bei Finance and Operations an, indem sie das neue Benutzerkonto verwendet. Er oder sie führen einen Kreditorenregistrierungs-Assistenten abschließend aus, um Informationen, wie Adressen, Geschäftsdaten, Beschaffungskategorien und Fragebogenantworten bereitzustellen.
5. **Genehmigungsworkflow** – Eine Kreditorenanforderung, die die Registrierungsinformationen enthält, wird erstellt. Die Kreditorenanforderung wird als Workflow übermittelt und zur Überprüfung und Genehmigung weitergeleitet.
6. **Erstellung eines Kreditorenmasters und einer Benutzerrollenänderung** – Wenn die Kreditorenanforderung genehmigt wurde, wird ein Kreditorendatensatz erstellt. Dem Benutzerkonto der Kontaktperson des Kreditors wird entweder die Berechtigung zur Kreditorenzusammenarbeit gewährt, oder es wird deaktiviert.

In der folgenden Tabelle werden die Schritte und die Rollen angezeigt, die am Prozess beteiligt sind.

| Rolle und „Prozess”       | OData zur Datenverwaltung – Entitätsimport | Listenseite für die Registrierungsanforderung künftiger Kreditoren | Benutzerbereitstellungs-Workflow | Kreditorenregistrierungs-Assistent | Genehmigungsworkflow | Erstellung eines Kreditorenmasters und einer Benutzerrollenänderung |
|--------------------------|---|---|---|---|---|---|
| System                   | Die Anforderung für einen neuen Kreditor wird importiert. | | | | | Nachdem die Kreditorenanforderung angenommen wurde, wird der Kreditorendatensatz erstellt. |
| Prokurist | | Starten Sie den Aufnahmeprozess. | | | Überprüfen Sie die Kreditorenanforderung, und nehmen Sie sie entweder an oder lehnen Sie sie ab. | |
| Administrator            | | | Erstellen Sie einen Benutzer in Finance and Operations und Microsoft Azure. | | | |
| Kontaktperson des Kreditors    | | | Senden Sie eine E-Mail an die Kontaktperson. | Erfassen Sie Kreditoreninformationen. | | |

Für eine rasche Präsentation des Lieferanten-Onboardingprozesses schauen Sie das kurze YouTube video: [Onboard a new vendor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=0KUc3AGaTKk}.

## <a name="importing-the-prospective-vendor-registration-request"></a>Importieren der Registrierungsanforderung des künftigen Kreditors

Die Registrierungsanforderung des künftigen Kreditors ist eine Entität in Finance and Operations. Sie können das System so einrichten, dass Daten über diese Entität importiert werden. 

In der folgenden Tabelle werden die Informationen angezeigt, die diese Entität enthält und die importiert werden können.

| Feld                        | Beschreibung |
|------------------------------|-------------|
| Kreditorenname                  | Der Name des Kreditors. |
| Geschäftsbegründung       | Der Grund oder die Gründe für die Kreditorenanforderung. |
| Unternehmensnummer          | Eine offiziell bekannte Registrierungsnummer. |
| Sparte             | Die Sparte, in der der Kreditor tätig ist |
| Vorname der Kontaktperson  | Der Vorname der Person, die eingeladen wird, um die Kreditoreninformationen zu erfassen. |
| Zweiter Vorname der Kontaktperson | Der zweite Vorname der Person, die eingeladen wird, um die Kreditoreninformationen zu erfassen. |
| Der Nachname der Kontaktperson   | Der Nachname der Person, die eingeladen wird, um die Kreditoreninformationen zu erfassen. |
| E-Mail der Kontaktperson       | Die E-Mail-Adresse, die dazu verwendet wird, einen neuen Benutzer in Finance and Operations zu erstellen, der im Azure Active Directory (Azure AD)-Konto des Mandanten erfasst wird. |
| Übermittlungsdatum               | Das Datum, an dem die Anforderung in einem externen System erstellt wurde. |
| Juristische Person                 | Die juristische Person, bei der der Kreditor anfragt, ein Kreditor zu werden. Dieser Wert muss ein Code für eine juristische Person sein, der in Finance and Operations erfasst wurde. Wenn kein Wert durch den Importprozess empfangen wird, wird ein Wert aus den Beschaffungsparametern angewendet. |
| Kreditortyp                  | Der Kreditor kann entweder eine Organisation oder eine Person sein. Der Kreditortyp bestimmt, wie der Kreditor letztendlich erstellt wird. |

Nachdem die Registrierungsanforderung des künftigen Kreditors importiert wurde, wird sie auf der Listenseite **Registrierungsanforderung des künftigen Kreditors** angezeigt. Von dieser Listenseite aus kann ein Prokurist den Benutzer einladen. Eine Benutzeranforderung zur Bereitstellung des Benutzers wird an einen Workflow übermittelt.

## <a name="submitting-a-prospective-vendor-user-request"></a>Eine Anforderung eines künftigen Kreditorenbenutzers übermitteln

Der Zweck der Anforderung für künftige Kreditorbenutzer liegt darin, die Person bereitzustellen, die die ursprüngliche Anforderung übermittelt hat, sodass er oder sie sich bei Finance and Operations mithilfe des E-Mail-Kontos anmelden kann, das in der Registrierungsanforderung für künftige Kreditoren bereitgestellt wird.

Die Anforderung des künftigen Kreditorenbenutzers wird durch den Benutzeranforderungsworkflow verarbeitet. Dieser Workflow kommuniziert durch die Azure AD B2B-Zusammenarbeit. Er erstellt einen Benutzer in Finance and Operations, der über die entsprechenden Sicherheitseinstellungen verfügt.

Neue Benutzer, die eingerichtet werden, haben die folgenden Sicherheitsrollen:

- Externer Systembenutzer
- Künftiger Kreditor (externer Interessent)

Der neue Benutzer wird eine E-Mail empfangen, die durch den Benutzeranforderungsworkflow generiert wird. Diese E-Mail lädt den Benutzer ein, sich im System anzumelden.

Informationen zur Konfiguration der E-Mail und des Workflows im Allgemeinen finden Sie in der Beschreibung eines Benutzeranforderungsworkflows in [Einrichten und Verwalten von Kreditorenzusammenarbeit](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Kreditorenregistrierung

Ein künftiger Kreditorbenutzer, der sich bei Finance and Operations anmeldet, sieht die erste Seite eines Kreditorenregistrierungs-Assistenten, wo er oder sie Kreditoreninformationen eingeben können.

Der Assistent spiegelt die Konfiguration der Kreditorenanforderung wider. Das Land oder die Region, wo der Kreditor Geschäfte tätigt, bestimmt, welche Informationen im Assistenten angefordert werden und welche Informationen obligatorisch sind.

Weitere Informationen zur Kreditorenanforderungskonfiguration finden Sie unter [Konfiguration und Verwaltung der Kreditorenzusammenarbeit](set-up-maintain-vendor-collaboration.md) Die nachstehende Tabelle enthält einen Überblick über die Seiten im Assistenten und den Zweck jeder Seite.

| Seite                       | Beschreibung |
|----------------------------|-------------|
| Land/Region             | Das Land bzw. die Region bestimmt die Kreditorenanforderungskonfiguration, die auf die verbleibenden Assistentenseiten angewendet wird. Es bestimmt auch Werte in der **Steuerstatus**-Suche. |
| Geschäftsbedingungen       | Diese Seite kann möglicherweise verfügbar sein, abhängig von der Kreditorenanforderungskonfiguration. Wenn sie verfügbar ist, muss der Benutzer die Bedingungen bestätigen, um den Vorgang fortzusetzen. |
| Kreditoreninformationen         | Diese Seite enthält den Kreditorennamen, der automatisch anhand der ursprünglichen Registrierungsanforderung des künftigen Kreditors eingegeben wird. Außerdem enthält sie die Unternehmensnummer, die Telefonnummer, Faxnummer und E-Mail-Adresse des Kreditors sowie Adressen des Kreditors für verschiedene Zwecke. |
| Informationen zur Kontaktperson | Diese Seite enthält den Namen der Kontaktperson, der automatisch anhand der ursprünglichen Registrierungsanforderung des künftigen Kreditors eingegeben wird. Außerdem enthält sie die Telefonnummer und E-Mail-Adresse der Kontaktperson sowie die Adressen der Kontaktperson für verschiedene Zwecke. |
| Unternehmensinformationen       | Diese Seite enthält Steuernummern (für verschiedene Länder/Regionen) und die Anzahl von Mitarbeitern. Außerdem gibt sie an, ob das Unternehmen in Minderheitseigentum ist. |
| Beschaffungskategorien     | Diese Seite enthält die Beschaffungskategorien, für die der Kreditor eine Genehmigung anfordert. Der Benutzer kann Kategorien in der Beschaffungskategoriehierarchie auswählen. Sie können die Anzahl der Ebenen konfigurieren, die in der Hierarchie in **Beschaffungsparameter** &gt; **Kreditorenzusammenarbeit** unter **Beschaffung** &gt; **Einstellungen** angezeigt werden. |
| Fragebögen             | Der Assistent fügt möglicherweise einen Satz von Fragebögen für den Kreditor ein. Fragebögen, die im Assistenten angezeigt werden, werden entweder in der Kreditorenanforderung oder pro Beschaffungskategorie angezeigt. Wenn Fragebögen pro Beschaffungskategorie konfiguriert sind, bestimmen die Beschaffungskategorien, für die der Kreditor die Genehmigung anfordert, die Fragebögen, die im Assistenten angezeigt werden. Auf der Seite **Beschaffungskategorien** können Sie einen Fragebogen unter der betreffenden Kategorie hinzufügen und den Aktivitätstyp auf **Kreditoreinführung** festlegen. |

Wenn der künftige Kreditorenbenutzer den Kreditorenerfassungs-Assistenten abschließt, wird eine Kreditorenanforderung erstellt.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Manuelles oder automatisches Übermitteln einer Kreditorenanforderung

Eine Kreditorenanforderung kann als Entwurf erstellt werden und manuell an ein Workflow übermittelt werden. Alternativ kann die Kreditorenanforderung automatisch an einen Workflow übermittelt werden, wenn der Kreditorenregistrierungs-Assistent abgeschlossen ist. Eine Anforderung kann manuell übermittelt werden, wenn zum Beispiel ein Prokurist beurteilen möchte, ob die Anforderung durch einen Genehmigungsprozess weitergeleitet werden soll, bevor sie an den Workflow übermittelt wird.

- Wählen Sie **Beschaffungsparameter** &gt; **Kreditorenzusammenarbeit** aus, und wählen Sie dann **Registrierung des künftigen Kreditors automatisch an den Workflow übermitteln**, um die Kreditorenanforderung zu konfigurieren, sodass sie automatisch an einen Workflow übermittelt wird, wenn der Kreditorregistrierungs-Assistent abgeschlossen ist.

## <a name="vendor-requests"></a>Kreditorenanforderungen

Kreditorenanforderungen sind auf der Seite **Kreditorenzusammenarbeits-Benutzeranforderungen** verfügbar.

Eine Kreditorenanforderung enthält die Informationen, die der künftige Kreditorenbenutzer in den Kreditorenregistrierungs-Assistenten eingegeben hat.

Die Anforderung ermöglicht es Ihnen, die Kreditoreninformationen zu überprüfen und zu entscheiden, ob der Kreditor ein registrierter Kreditor in Finance and Operations werden soll.

Die Kreditorenanforderung sollte an einen Workflow übermittelt werden, und sie sollte an die relevanten Prüfer und genehmigenden Personen weitergeleitet werden. Grundlegende Informationen zum Einrichten von Workflows finden Sie unter [Beschaffung](procurement-sourcing-workflows.md).

Die folgende Tabelle zeigt die Statusangaben, die Kreditorenanforderungen haben können.

| Status                     | Beschreibung |
|----------------------------|-------------|
| Überblick                      | Die Kreditorenanforderung ist noch nicht übermittelt worden. |
| Anforderung übermittelt          | Die Kreditorenanforderung wurde übermittelt, und der erste Schritt im Workflow wird gerade verarbeitet. |
| Überprüfung ausstehend             | Wenn es mehrere Prüfer in einer Workflowaufgabe gibt, kann ein Prüfer die Aufgabe der Überprüfung der Kreditorenanforderung akzeptieren und dann die Überprüfung abschließen. Wenn es nur einen Prüfer gibt, kann dieser Teilnehmer die Prüfung abschließen, indem er **Abgeschlossen** in der Workflowaktivität auswählt. Er oder sie müssen die Arbeitsaufgabe nicht zuerst akzeptieren. |
| Genehmigung der Anforderung ausstehend   | Die Kreditorenanforderung wurde an die Teilnehmer zur Genehmigung weitergeleitet, und es gibt eine Option, weitere Informationen anzufordern. Eine Anforderung weiterer Informationen führt dazu, dass die Arbeitsaufgabe zurück zum Übermittler weitergeleitet wird. Die Kreditorenanforderung kann genehmigt oder abgelehnt werden, während sie in diesem Status ist. |
| Antragsänderungsanforderung | Zusätzliche Informationen sind vom Genehmiger angefordert worden, und die Kreditorenanforderung wurde an die Person weitergeleitet, die die Kreditorenanforderung übermittelt hat. Der Übermittler kann erforderliche Informationen hinzufügen und dann die Kreditorenanforderung erneut übermitteln. Wenn eine Kreditorenanforderung erneut übermittelt wird, wird der Status wieder in **Anforderung mit ausstehender Genehmigung** geändert. |
| Anforderung genehmigt           | Dieser Status ist ein Endzustand. |
| Anforderung abgelehnt           | Dieser Status ist ein Endzustand. |

## <a name="approving-a-vendor-request"></a>Genehmigung einer Kreditorenanforderung

Wenn eine Kreditorenanforderung genehmigt ist, wird ein Kreditorenkonto erstellt, und der Status **Genehmigt** wird sowohl auf der ursprünglichen Registrierungsanforderung des künftigen Kreditors als auch auf der Kreditorenanforderung angezeigt.

Bevor Sie eine Kreditorenanforderung genehigen, wählen Sie auf der Seite **Neuer Kreditor** im Inforegister **Allgemein** die Option **Kreditorengruppe** aus, um eine Kreditorengruppe auszuwählen.

Wenn der künftige Kreditorenbenutzer Zugriff auf Finance and Operations als ein Kreditorenzusammenarbeitsbenutzer haben soll, der den Kreditor vertritt, legen Sie die Zugriffsberechtigung für die Kreditorenzusammenarbeit auf **Ja** fest. Um das Benutzerkonto zu deaktivieren, das der künftige Kreditor verwendet hat, um sich zu registrieren, legen Sie diese Berechtigung auf **Nein** fest.

Wenn die Zugriffsberechtigung für die Kreditorenzusammenarbeit auf **Ja** festgelegt ist, wenn die Kreditorenanforderung genehmigt ist, wird eine Anforderung übermittelt, um die Rollen des Benutzers zu ändern, sodass der Benutzer die Rollen hat, die für den Typ **Kreditor** in **Externe Rollen** definiert sind. Wenn diese Berechtigung auf **Nein** festgelegt ist, wenn die Kreditorenanforderung genehmigt ist, wird eine Anforderung übermittelt, den Benutzer zu deaktivieren. In diesem Fall muss der Workflow, um einer Benutzeranforderung zu deaktivieren, eingerichtet werden.

Damit ein Kreditorenkonto erstellt werden kann, wenn die Kreditorenanforderung genehmigt wird, muss der Nummernkreis zum Erstellen von Kreditoren aus Kreditorenanforderungen auf **Automatisch** festgelegt sein.

Einen Überblick über die Zugriffsberechtigungen eines Kreditorenzusammenarbeitbenutzers finden Sie unter [Kreditorenzusammenarbeit einrichten und verwalten](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Ablehnen einer Kreditorenanforderung

Wenn eine Kreditorenanforderung abgelehnt wird, muss ein Grund für die Ablehnung in der Kreditorenanforderung ausgewählt werden.

Im Fall der Ablehnung einer Kreditorenanforderung, wird eine Anforderung übermittelt, den Benutzer zu deaktivieren. In diesem Fall muss der Workflow, um einer Benutzeranforderung zu deaktivieren, eingerichtet werden. Weitere Informationen finden Sie unter [Kreditorenzusammenarbeit einrichten und verwalten](set-up-maintain-vendor-collaboration.md).

Wenn eine Kreditorenanforderung abgelehnt wird, wird der Status **Abgelehnt** sowohl auf der ursprünglichen Registrierungsanforderung des künftigen Kreditors als auch auf der Kreditorenanforderung angezeigt.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Löschen einer Registrierungsanforderung eines künftigen Kreditors in verschiedenen Statussituationen

Die verschiedenen Status einer Registrierungsanforderung eines künftigen Kreditors geben eine Übersicht über den Fortschritt der Anforderung.

Indem Sie die Aktivität **Löschen** in der Registrierungsanforderung des zukünftigen Kreditors verwenden, können Sie die Kette von Datensätzen bereinigen und entfernen, die erstellt wurde, und Sie können das Benutzerkonto deaktivieren. Das Ergebnis der Aktivität **Löschen** variiert, abhängig vom Status der Registrierungsanforderung des künftigen Kreditors, wie in der folgenden Tabelle dargestellt.


|          Status          |                                                                                     Statusbeschreibung                                                                                      |                                                                                                                                                            Ergebnis der Aktivität „Löschen”                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Neue            |                                                                         Keine Aktivitäten sind auf die Anforderung hin ausgeführt worden.                                                                          |                                                                                                                                              Die Registrierungsanforderung des künftigen Kreditors ist gelöscht.                                                                                                                                               |
|      Benutzer angefordert      | Wenn Sie <strong>Benutzer einladen</strong> auswählen, wird der Status zu <strong>Benutzer angefordert</strong> geändert, und eine Anforderung eines künftigen Benutzer wird erstellt und an ein Benutzeranforderungsworkflow übermittelt. |                                                                                                          Sie können eine Registrierungsanforderung eines künftigen Kreditors nicht löschen, die diesen Status hat, da der Benutzeranforderungsworkflow nicht abgeschlossen wurde.                                                                                                          |
|       Benutzer eingeladen       |                                                               Der Benutzeranforderungsworkflow wird genehmigt, und der Benutzer wird erstellt.                                                               |                                                                                                                      Eine Anforderung, den Benutzer zu deaktivieren, wird erstellt, und die Registrierungsanforderung des künftigen Kreditors wird gelöscht.                                                                                                                      |
| Registrierung in Bearbeitung |                                                         Der neue Benutzer hat sich angemeldet und hat den Kreditorenregistrierungs-Assistenten gestartet.                                                          |                                                                                     Eine Anforderung, den Benutzer zu deaktivieren, wird erstellt, und die Registrierungsanforderung des künftigen Kreditors sowie die in den Kreditorenregistrierungs-Assistenten eingegebenen Daten werden gelöscht.                                                                                      |
|  Kreditorenanforderung erstellt  |                                                                     Der Kreditorenregistrierungs-Assistent wurde abgeschlossen.                                                                      | Eine Anforderung, den Benutzer zu deaktivieren, wird erstellt, und die Registrierungsanforderung des künftigen Kreditors, die in den Kreditorenregistrierungs-Assistenten eingegebenen Daten sowie die Kreditorenanforderung werden gelöscht.<blockquote>[!NOTE]<br>Sie können die Aktivität <strong>Löschen</strong> nicht verwenden, wenn die Kreditorenanforderung sich in einem Prüfprozess im Workflow befindet.</blockquote> |
|         Genehmigt         |                                                                               Die Kreditorenanforderung ist genehmigt.                                                                               |                                                                                                   Eine Registrierungsanforderung des künftigen Kreditors, die in den Kreditorenregistrierungs-Assistenten eingegebenen Daten sowie die Kreditorenanforderung werden gelöscht.                                                                                                    |
|         Verweigert         |                                                                               Die Kreditorenanforderung wird abgelehnt.                                                                               |                                                                                                   Eine Registrierungsanforderung des künftigen Kreditors, die in den Kreditorenregistrierungs-Assistenten eingegebenen Daten sowie die Kreditorenanforderung werden gelöscht.                                                                                                    |

