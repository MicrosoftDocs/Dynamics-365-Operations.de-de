---
title: Bestellanforderungsworkflow
description: "Der Workflowprozess leitet Bestellanforderungen durch den Prüfungsprozess, vom Anfangsstatus &quot;Übersicht&quot; bis zum Endstatus &quot;Genehmigt&quot;. Wenn eine Bestellanforderung zur Prüfung übermittelt wird, wird der Workflowprozess gestartet. Nachdem die Bestellanforderung genehmigt wurde, kann eine Bestellung für die Bestellanforderungspositionen generiert und zur Auftragserfüllung an den Kreditor übermittelt werden."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d28e92fa853d155bc62932625e0e714cdf4edcc
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="purchase-requisition-workflow"></a>Bestellanforderungsworkflow

[!include[banner](../includes/banner.md)]


Der Workflowprozess leitet Bestellanforderungen durch den Prüfungsprozess, vom Anfangsstatus "Übersicht" bis zum Endstatus "Genehmigt". Wenn eine Bestellanforderung zur Prüfung übermittelt wird, wird der Workflowprozess gestartet. Nachdem die Bestellanforderung genehmigt wurde, kann eine Bestellung für die Bestellanforderungspositionen generiert und zur Auftragserfüllung an den Kreditor übermittelt werden.

Bevor eine Bestellanforderung zur Prüfung übermittelt werden kann, müssen Sie einen Workflow konfigurieren. Der Workflowprozess kann einen oder mehrere Prüfschritte in beliebiger Reihenfolge umfassen. Der Workflowprozess kann auch so konfiguriert werden, dass die Prüfaufgaben übersprungen werden und die Bestellanforderung automatisch genehmigt wird Sie können den Workflow so konfigurieren, dass die Bestellanforderung als einzelnes Dokument durch den Prüfprozess weitergeleitet wird, oder einzelne Bestellanforderungspositionen an die geeigneten Prüfer weitergeleitet werden. Sie können auch ein Szenario erstellen, in dem die Bestellanforderung als einzelnes Dokument an einige Prüfer und ausgewählte Bestellanforderungspositionen an andere Prüfer weitergeleitet werden.  

Wenn Bestellanforderungspositionen einzeln geprüft werden, muss der Prüfungsprozess für alle Positionen abgeschlossen sein, bevor der Workflowprozess zum nächsten Schritt übergehen und der Prüfungsprozess für die Bestellanforderung als Ganzes abgeschlossen werden kann. Wenn der Prüfprozess für die Bestellanforderung und deren Positionen abgeschlossen ist, wird der Gesamtstatus der Bestellanforderung in **Genehmigt** aktualisiert.  

Sie können den Workflow so konfigurieren, dass er den Geschäftsprozess für Bestellanforderungen in der Organisation darstellt. Beachten Sie beim Konfigurieren des Workflowprozesses für Bestellanforderungen die folgenden Fragen:

-   Welche Aufwendungen müssen geprüft werden?
-   Welche Aufwendungen werden automatisch genehmigt?
-   Wer muss beantragte Aufwendungen prüfen und genehmigen? Welche Rollen sind diesen Benutzern zugewiesen?
-   Welcher Prozess muß erfolgen, wenn ein Prüfer nicht verfügbar ist?

Die folgenden Beispiele veranschaulichen zwei Arten, mit dem der Workflow für Bestellanforderungen konfiguriert werden kann.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Beispiel 1: Weiterleiten einer Bestellanforderung als einzelnes Dokument zur Prüfung
Die folgende Abbildung zeigt, wie eine Bestellanforderung als einzelnes Dokument durch den Workflowprüfprozess weitergeleitet werden kann. Die Positionen der Bestellanforderung werden nicht einzeln weitergeleitet. In diesem Beispiel umfasst der Workflowprozess die folgenden Rollen:

-   **Anfordernde Person** – Der Benutzer, von dem die Artikel oder Dienstleistungen angefordert werden. Die anfordernde Person kann die Bestellanforderung vorbereiten, oder eine andere Arbeitskraft kann die Bestellanforderung im Auftrag der anfordernden Person vorbereiten. Diese Arbeitskraft ist der Antragsteller. Der Antragsteller ist im gesamten Prüfprozess für die Verwaltung der Bestellanforderung verantwortlich. Nur der Antragsteller der Bestellanforderung kann diese ändern.

**Hinweis:** Eine Arbeitskraft muss über die entsprechenden Berechtigungen verfügen, um eine Bestellanforderung im Auftrag einer anderen Person zu erstellen. Verwenden Sie die Seite **Bestellanforderungsberechtigung**, um diese Berechtigungen einzurichten.

-   **Einkaufsvertreter** – Der Benutzer, der die Beschaffungsprüfung durchführt und das Dokument genehmigen kann.
-   **Der Vorgesetzte der anfordernden Person** – Der Benutzer, der die Prüfung auf Managerebene durchführt und das Dokument genehmigen kann.

![Workflowüberprüfungsprozess für Bestellanforderungen](./media/purchreqworkflowoverview_submission.gif)  
In diesem Beispiel umfasst der Workflowprozess für die Bestellanforderung die folgenden Schritte:

1.  Der Antragsteller übermittelt eine Bestellanforderung zur Prüfung.
2.  Der Einkaufsvertreter erhält eine Benachrichtigung. Die Benachrichtigung fordert den Einkaufsvertreter auf, die Informationen in der Bestellanforderung zu überprüfen. Falls notwendige Informationen fehlen, kann der Einkaufsvertreter die Informationen entweder hinzufügen oder die Bestellanforderung an den Antragsteller zurücksenden, damit dieser die fehlenden Informationen ergänzt. Nachdem alle erforderlichen Informationen ausgefüllt wurden, kann die Bestellanforderung mit dem nächsten Schritt im Prüfprozess fortgesetzt werden.
3.  Der Vorgesetzte der anfordernden Person prüft die Bestellanforderung. Die Bestellanforderung kann an den Vorgesetzten der anfordernden Person weitergeleitet werden, wenn z. B. der Betrag der Bestellanforderung das Ausgabenlimit für Bestellanforderungen der anfordernden Person übersteigt. Der Vorgesetzte der anfordernden Person kann die Bestellanforderung genehmigen oder ablehnen oder zwecks Änderung an den Antragsteller zurücksenden.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Beispiel 2: Weiterleiten einzelner Bestellanforderungspositionen zur Prüfung
Die folgende Abbildung zeigt, wie einzelne Bestellanforderungspositionen durch einen Workflow weitergeleitet werden können. Im Allgemeinen entspricht der Prozess für jede einzelne Position dem Prozess für eine Bestellanforderung, die als einzelnes Dokument geprüft wird. Zuerst müssen jedoch alle Positionen den Workflowprozess einzeln durchlaufen, bevor der Workflow für die gesamte Bestellanforderung abgeschlossen werden kann.  

In diesem Beispiel erfasst eine Arbeitskraft eine Bestellanforderung für Poster und T-Shirts für eine Marketingkampagne. Die Kosten der Poster werden zwischen der Marketing- und der Vertriebsabteilung aufgeteilt. Wenn die Kosten der Poster oder T-Shirts das Unterzeichnungslimit der Abteilungsleiter überschreiten, muss die Bestellanforderung auch vom Gruppenleiter geprüft werden.  

In diesem Beispiel umfasst der Workflowprozess die folgenden Rollen:

-   **Anfordernde Person** – Der Benutzer, von dem die Artikel oder Dienstleistungen angefordert werden. Die anfordernde Person kann die Bestellanforderung vorbereiten, oder eine andere Arbeitskraft kann die Bestellanforderung im Auftrag der anfordernden Person vorbereiten. Diese Arbeitskraft ist der Antragsteller. Der Antragsteller ist im gesamten Prüfprozess für die Verwaltung der Bestellanforderung verantwortlich. Nur der Antragsteller der Bestellanforderung kann diese ändern.

**Hinweis:** Eine Arbeitskraft muss über die entsprechenden Berechtigungen verfügen, um eine Bestellanforderung im Auftrag einer anderen Person zu erstellen. Verwenden Sie die Seite **Bestellanforderungsberechtigung**, um diese Berechtigungen einzurichten.

-   **Einkaufsvertreter** – Der Benutzer, der die Beschaffungsprüfung durchführt und das Dokument genehmigen kann.
-   **Der Vorgesetzte der anfordernden Person** – Der Benutzer, der die Prüfung auf Managerebene durchführt und das Dokument genehmigen kann.
-   **Abteilungsleiter** – Der Benutzer, der eine Aufwendungsprüfung durchführt und das Dokument genehmigen kann.
-   **Gruppenleiter** – Der Benutzer, der eine Prüfung als Unterzeichnungsberechtigter durchführt und das Dokument genehmigen kann.

![Workflowüberprüfungsprozess für Bestellanforderungspositionen](./media/purchreqlineworkflowoverview.gif)  
In diesem Beispiel umfasst der Workflowprozess für die Bestellanforderungspositionen die folgenden Schritte:

1.  Der Antragsteller übermittelt eine Bestellanforderung zur Prüfung. Jede Position wird an den Prüfer weitergeleitet, der im Workflowprozess als Empfänger konfiguriert ist.
2.  Der Einkaufsvertreter erhält eine Benachrichtigung. Die Benachrichtigung fordert den Einkaufsvertreter auf, die Informationen in der Bestellanforderung und in den Bestellanforderungspositionen zu überprüfen. Wenn eine Bestellanforderung durch den Einkaufsvertreter geöffnet wird, werden alle Zeilen angezeigt, aber eine visuelle Anzeige zeigt, welche Positionen zur Überprüfung an den Einkaufsvertreter gesendet wurden. Falls notwendige Informationen fehlen, kann der Einkaufsvertreter die Informationen entweder hinzufügen oder die Bestellanforderungspositionen an den Antragsteller zurücksenden, damit dieser die fehlenden Informationen ergänzt. Nachdem alle erforderlichen Informationen ausgefüllt wurden, kann die Bestellanforderungsposition mit dem nächsten Schritt im Prüfprozess fortgesetzt werden. Bestellanforderungspositionen können den Prüfprozess unabhängig voneinander durchlaufen.
3.  Der Linienmanager der anfordernden Person prüft und genehmigt die Bestellanforderungspositionen. Die Genehmigung kann an den Vorgesetzten der anfordernden Person weitergeleitet werden, wenn z. B. der Betrag der Bestellanforderungsposition das Ausgabenlimit der anfordernden Person für Bestellanforderungspositionen übersteigt. Der Vorgesetzte kann eine oder beide Bestellanforderungspositionen genehmigen oder ablehnen.
4.  Der Abteilungsleiter der Marketingabteilung prüft die Bestellanforderungspositionen sowohl für sowohl die Poster als auch die T-Shirts. Der Leiter der Vertriebsabteilung prüft nur die Bestellanforderungsposition für die Poster, da die Vertriebsabteilung nur mit diesen Kosten belastet wird.
5.  Der Gruppenleiter prüft und genehmigt die Bestellanforderungsposition für die T-Shirts nur, wenn eine Gruppenleitergenehmigung erforderlich ist, da beispielsweise der Betrag der Bestellanforderungsposition das Genehmigungslimit des Abteilungsleiters überschreitet. Der Gruppenleiter muss nicht die Bestellanforderungsposition für die Poster genehmigen.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Konfigurieren eines Workflows für Bestellanforderungen
Bevor eine Bestellanforderung zur Prüfung weitergeleitet werden kann, müssen die Workflowprozesse für Bestellanforderungen konfiguriert werden. Mit dem Workflowprozess wird die Interaktion zwischen dem Benutzer, von dem die Artikel angefordert wurden (die anfordernde Person), und dem Prüfer und der genehmigenden Person innerhalb des Workflows definiert. Die Weiterleitung der Bestellanforderung hängt von den Bedingungen ab, die in der Workflowkonfiguration angegeben werden. Beispielsweise bestimmen diese Bedingungen, ob die Bestellanforderung weitergeleitet werden soll, den Benutzer oder die Rolle, zu dem oder der sie weitergeleitet werden soll und die Aktivitäten, die Benutzer treffen können.  

Die Beispiele in diesem Thema zeigen, wie eine Bestellanforderung durch den Workflow als einzelnes Dokument und in Form einzelner Bestellanforderungspositionen weitergeleitet werden kann. Sie können den Workflow für Bestellanforderungen auch gemäß der zu internen Kontrollzwecken vorgesehenen Bestellanforderungsprüfung konfigurieren, die für die Organisation definiert ist.  

Die Teilnehmer oder der Prüfer, denen eine Aufgabe in einem Workflow zugewiesen ist, können Mitglieder einer bestimmten Benutzergruppe, Benutzer einer bestimmten Sicherheitsrolle, Benutzer, die dem Antragsteller in einer Verwaltungshierarchie zugeordnet sind, Benutzer mit Namen oder Benutzer mit bestimmten Aufwendungenszuständigkeiten sein.

### <a name="purchase-requisition-expenditure-reviewers"></a>Prüfer von Aufwendungen in Zusammenhang mit Bestellanforderungen

Mit Konfigurationen für Aufwendungsprüfer können Sie Aufwendungen zur Prüfung dynamisch weiterleiten, basierend auf dem Benutzer, der einer Projektrolle oder einer Finanzdimension zugewiesen ist, der die Aufwendung berechnet wird. Im Workflowprozess wird die angegebene Projektrolle oder der Besitzer der Finanzdimension verwendet, um zu bestimmen, an wen die Aufwendungen weitergeleitet werden sollen.  

Sie können eine oder mehrere Konfigurationen für Aufwendungsprüfer definieren und anschließend beim Erstellen eines Workflows eine Konfiguration auswählen. Sie können die Werte für Aufwendungsprüfer für jede juristische Person in der Organisation konfigurieren. Nachdem Sie die Konfigurationen für Aufwendungsprüfer definiert haben, weisen Sie die Konfiguration einer Workflowaufgabe zu.  

Sie müssen keine Konfiguration für Aufwendungsprüfer definieren. Stattdessen können Sie beim Definieren des Workflows einen bestimmten Benutzer oder eine bestimmte Benutzergruppe als Prüfer zuordnen. In einer komplexen Organisation können jedoch Aufwendungsprüfer die Effizienz des Genehmigungsprozesses steigern. Wenn Sie darüber hinaus Aufwendungsprüfer einrichten, müssen Sie Workflowprüferzuordnungen nicht jedes Mal aktualisieren, wenn sich der Tätigkeitsbereich eines Prüfers ändert.  

Sie können die Aufwendungsprüfer auf der Seite **Aufwendungsprüfer für Bestellanforderungen** einrichten. Erstellen Sie eine Konfiguration für Aufwendungsprüfer und geben Sie für jede juristische Person in Ihrem Unternehmen Werte ein. Für Bestellungen, die einem Projekt zugeordnet werden, können Sie die Rolle angeben, die für die Prüfung der Anforderungen zuständig ist: Projektmanager-, Projektcontroller oder Projektverkaufsleiter. Aufwendungen werden an den Benutzer weitergeleitet, der angegebenen Rolle zugewiesen ist. Sie können auch die Aufwendungen an den Besitzer der Finanzdimension weiterleiten, indem Sie das Kontrollkästchen der entsprechenden Finanzdimension auf der Registerkarte **Organisationsverteilungen** aktivieren.  

Um einen der Aufwendungsprüfer zu verwenden, den Sie in einem Workflow eingerichtet haben, müssen Sie die Option **Art von Teilnehmer** auf **Aufwendungsbeteiligte** in den Eigenschaften**Zuweisung** für das relevante Workflowelement festlegen.

<a name="see-also"></a>Siehe auch
--------

[Erstellen einer Anforderung für Verbrauch (Aufgabenleitfaden)](https://ax.help.dynamics.com/en/wiki/create-a-requisition-for-consumption/)

[Definieren von geschäftlichen Prozessworkflows für Bestellanforderungen.](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Beschaffungsworkflows](procurement-sourcing-workflows.md)

[Bestellanforderungsüberblick](purchase-requisitions-overview.md)




