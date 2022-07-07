---
title: Kreditlimits für Debitoren
description: Dieser Artikel stellt eine Übersicht der Kreditlimitprüfung in Dynamics 365 Supply Chain Management bereit.
author: Henrikan
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4a98b90491093f55ce6974b9b11ff326c0c2f5c
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015317"
---
# <a name="credit-limits-for-customers"></a>Kreditlimits für Debitoren

[!include [banner](../includes/banner.md)]

Beim Festlegen eines Kreditlimits können Sie den Höchstbetrag des Kredits angeben, der den Debitoren gewährt wird. Wenn ein Kreditlimit angegeben wurde, wird es automatisch geprüft, wenn ein Benutzer versucht, ein Dokument zu aktualisieren. Wenn das Kreditlimit überschritten wird, wird eine Meldung für den Benutzer angezeigt. Dieses Thema bietet einen Überblick darüber, wie Kreditlimits in  funktionieren und beantwortet die folgenden Fragen:

-   Für welche Dokumente und Prozesse kann ich Kreditlimit prüfen?

-   Wo konfiguriere ich die Methode, nach der der verbleibende Kredit des Debitors berechnet wird?

-   Wo werden Informationen zu dem verbleibenden Kredit eines Debitors verwendet?

-   Wo gebe ich an, ob Kennung erforderlich ist, damit eine Gutschrift einem Debitor gewährt werden kann, und auch den Kreditbetrag, der Identifikation erfordert?

-   Wo gebe ich an, ob eine Warnung oder ein Fehler angezeigt wird, wenn das Kreditlimit überschritten wird?

-   Wie gebe ich das Kreditlimit für einen bestimmten Debitor an?

-   Wie überprüfe ich Kreditlimits für Aufträge manuell?

**Für welche Dokumente und Prozesse kann ich Kreditlimit prüfen?**

Verwenden Sie das Formular **Debitorenparameter**, um anzugeben, welche Dokumente Kreditlimiten überprüfen. Sie müssen Mitglied der Systemadministrator (-SYSADMIN-)-Sicherheitsrolle sein, wenn Sie die Änderungen in diesem Formular vorzunehmen. Sie können Kreditlimits für die folgenden Dokumente und Prozesse prüfen:

-   Rechnungen für Aufträge, wenn Sie die Rechnungen buchen

-   Lieferscheine für Aufträge, wenn Sie Lieferscheine aktualisieren

-   Aufträge, wenn Sie Positionen im Formular **Verkaufsaufträge** hinzufügen

-   Aufträge, wenn sie über einen Dienst erstellt werden

-   Freitextrechnungen, wenn Sie die Rechnungen erstellen

Kreditlimits werden automatisch überprüft, wenn eine der folgenden Optionen festgelegt ist:

-   Durch die **Art der Krediteinstellungen** im Formular **Debitorenparameter** wird bestimmt, ob dieses Feld erforderlich ist oder auf **Nein** gesetzt werden kann. Kreditlimits werden für alle Debitoren geprüft.

-   Im **Debitorenparameter** Formular wird das Feld **Kreditlimit-Typ** auf **Kein** festgelegt, jedoch wird der **Kreditlimit erforderlich** für einen Debitor im Formular **Debitoren** ausgewählt. Kreditlimits werden nur für bestimmte Debitoren geprüft.

Um Kreditlimits für die folgenden Dokumente zu überprüfen, müssen Sie zusätzliche Einstellungen angeben.

|    Dokument                                    |    Zusätzliche Einstellung                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Freitextrechnung                         |    Parameter für die Kreditlimitprüfung können Sie auf der Registerkarte Kreditwürdigkeit des Formulars Debitorenparameter festlegen.     |
|    Auftrag (manuell eingegeben)            |    Parameter für die Kreditlimitprüfung können Sie auf der Registerkarte Kreditwürdigkeit des Formulars Verkaufsauftrag festlegen.           |
|    Auftrag (elektronisch empfangen)     |    Im Formular Debioten im AIF-Bereich wählen Sie Kreditlimit für Verkaufsauftrag aus.                     |

**Wo konfiguriere ich die Methode, nach der der verbleibende Kredit eines Debitors berechnet wird?**

Sie können Dynamics 365 konfigurieren, um den verbleibenden Kredit eines Debitors nach einer der folgenden Methoden zu berechnen:

-   Vergleichen Sie das Kreditlimit mit dem Debitorensaldo

-   Vergleichen Sie das Kreditlimit gegen die Debitoren- und Lieferscheinbeträge.

-   Vergleichen Sie das Kreditlimit gegen Debitorensaldo und alle Aktivitäten mit offenen Posten. Dazu gehören Lieferscheinbeträge und Auftragsbeträge.

Verwenden Sie das Formular **Debitorenparameter**, um die Informationen zum Vergleichen anzugeben. Sie müssen Mitglied der Systemadministrator (-SYSADMIN-)-Sicherheitsrolle sein, wenn Sie die Änderungen in diesem Formular vorzunehmen. Wählen Sie im Feld **Kreditlimitart** aus, ob die automatische Überprüfung von Kreditlimits durchgeführt und welche Buchungsinformationen einzubeziehen sind, wenn das Kreditlimit geprüft wird. Folgende Optionen stehen zur Verfügung:

-   **Keine** - Kreditlimits nicht prüfen. Sie können diese Option für einen bestimmten Debitor überschreiben, indem Sie das Kontrollkästchen **Zwingende Kreditlimite** im Formular **Kunden** auswählen. Wenn Sie dies tun, wird das Kreditlimit gegen den Debitorensaldo geprüft.

-   **Saldo** – Der Debitorensaldo wird durch Vergleich mit dem Kreditlimit überprüft.

-   **Saldo + Lieferschein oder Produktzugang** – Das Kreditlimit wird durch Vergleich mit Debitorensaldo und Lieferungen überprüft.

-   **Saldo+Alles** – Das Kreditlimit wird durch Vergleich mit Debitorensaldo, Lieferungen und offenen Aufträgen überprüft.

**Wo werden Informationen zu dem verbleibenden Kredit eines Debitors verwendet?**

Informationen zum Saldo sowie den verbleibenden Habenbetrag eines Debitors werden berechnet und gespeichert, wenn Sie eine Fälligkeitsmomentaufnahme erstellen, und sie werden im Formular **Inkassi** angezeigt. Die Beträge, die im Formular **Inkassi** angezeigt werden, umfassen möglicherweise nicht alle Buchungsaktivitäten, bis eine neue Fälligkeitsmomentaufnahme erstellt wird. Weitere Informationen finden Sie unter [Inkassi und Kredit in Debitorenparametern](/dynamicsax-2012/appuser-itpro/collections-and-credit-in-accounts-receivable).

Abhängig von den Dokumenten, die ausgewählt wurden, werden Informationen zu den Saldi und verbleibenden Habenbetrag eines Debitors berechnet, wenn Aufträge, Lieferscheine und Debitorenrechnungen aktualisiert werden. Wenn der Betrag des Dokuments, mit dem Sie arbeiten, dazu führen würde, dass das Kreditlimit überschritten wird, wird eine Meldung angezeigt.

**Wo gebe ich an, ob Identifikation erforderlich ist, damit einem Debitor eine Gutschrift gewährt werden kann, und auch das Kreditlimit, das Identifikation erfordert?**

Verwenden Sie das Formular **Debitoren-Parameter**, um anzugeben, ob Identifikation erforderlich ist, und das Kreditlimit, für das Identifikation erforderlich ist.
Sie müssen Mitglied der Systemadministrator (-SYSADMIN-)-Sicherheitsrolle sein, wenn Sie die Änderungen in diesem Formular vorzunehmen.

|    Feld                                    |    Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Kennung bei Kredit erforderlich     |    Wählen Sie den Typ des Ausweises, der für Debitoren eingegeben werden muss, an die die juristische Person Kredite vergibt. Die Option, mit der Sie in diesem Feld auswählen, bestimmt, wann und welche Art von Informationen in den Behörden-Kennungsfeldern im Formular "Debitor" erforderlich ist:, - Kein von einer Behörde ausgestellter Ausweis ist, unabhängig vom Kreditlimit des Debitors. erforderlich     Ja – Es ist eine von einer Behörde ausgestellte Lizenznummer bzw. ein von einer Behörde ausgestellter Ausweis erforderlich, wenn das Kreditlimit des Debitors größer oder gleich Null ist.     Untergrenze – Es ist eine von einer Behörde ausgestellte Lizenznummer bzw. ein Ausweis erforderlich, wenn das Kreditlimit des Debitors größer oder gleich dem Limit ist, das Sie im Feld Limit in diesem Formular eingeben.        |
|    Limit                                    |    Geben Sie das Kreditlimit ein, ab dem für Debitoren eine von einer Behörde ausgestellte Lizenznummer bzw. ein von einer Behörde ausgestellter Ausweis erforderlich ist.    Sie können beispielsweise 2000 eingeben, um festzulegen, dass eine Ausweisnummer, z. B. eine Personalausweisnummer, für Debitoren mit einem Kreditlimit von 2.000 oder höher eingegeben werden muss.    Dieses Feld ist nur verfügbar, wenn Sie die Option Untergrenze im Feld Ausweisnummer bei Kredit erforderlich ausgewählt haben.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Wo gebe ich an, ob eine Warnung oder ein Fehler angezeigt wird, wenn das Kreditlimit überschritten wird?**

Verwenden Sie das Formular **Debitoren-Parameter,** um anzugeben, ob eine Warnung oder ein Fehler angezeigt wird, wenn das Kreditlimit überschritten wird. Diese Warnung oder ein Fehler wird angezeigt, wenn ein Benutzer Informationen eingibt oder bucht, oder es ist in ein Protokoll einbezogen, wenn die Dokumente von einem elektronischen Dienst verarbeitet werden. Sie müssen Mitglied der Systemadministrator (-SYSADMIN-)-Sicherheitsrolle sein, wenn Sie die Änderungen in diesem Formular vorzunehmen.

|    Feld                                                               |    Beschreibung                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Nachricht, wenn das Kreditlimit überschritten wird (im Bonitätsbereich)     |    Wählen Sie aus, wie Meldungen, dass Kreditlimit überschritten werden, von Benutzern angezeigt werden. Wählen Sie aus den folgenden Optionen aus:        Fehler – Eine Fehlermeldung wird angezeigt. Dieses beendet normalerweise den aktuellen Arbeitsgang und der Konflikt muss aufgelöst werden, bevor der Prozess fortgesetzt wird.     Warnung – Es wird eine Warnmeldung angezeigt, der Prozess kann jedoch fortgesetzt werden.                     |
|    Nachricht, wenn das Kreditlimit überschritten wird (im AIF-Bereich)               |    Wählen Sie aus, wie Nachrichten zum Überschreiten des Kreditlimits in einem Protokoll zugestellt werden. Wählen Sie aus den folgenden Optionen: Fehler  - Eine Fehlermeldung wird im Formular  angezeigt, und das Dokument wird nicht verarbeitet, bis der Fehler behoben ist.     Warnung – Es wird eine Warnmeldung im Formular Ausnahmen angezeigt, der Prozess kann jedoch fortgesetzt werden.        |

**Wie gebe ich den Kreditlimitbetrag für einen bestimmten Debitor an?**

Verwenden Sie das Formular **Kunden**, um den Betrag für das Kreditlimit für einen bestimmten Debitor einzugeben. Sie müssen Mitglied einer Sicherheitsrolle ein, der die Aufgabe Masterdaten von Debitoren verwalten (CustCustomersMaintain) zugewiesen ist, um Änderungen in diesem Formular vorzunehmen.

1.  Klicken Sie auf **Debitoren** \> **Debitoren** \> **Alle Debitoren.** Doppelklicken Sie auf ein Debitorenkonto.

2.  In der **Debitoren** Formular im Aktivitätsbereich, klicken Sie **Bearbeiten**.

3.  Geben Sie den Habenbetrag im Feld **Kreditlimite** ein. Dieser Wert muss größer als Null (0) sein und wird als Betrag für das Kreditlimit verwendet.

4.  Falls erforderlich, geben Sie eine Führerscheinnummer oder sonstige behördliche Identifikation im Feld R **Regierungskennung** ein.

> [!NOTE]
> Weitere Informationen finden Sie unter **Debitorenparametern**, in der Regel wird ein Kreditlimittyp gewählt. Wenn jedoch der Kreditlimit-Typ zu **Nein** festgelegt ist, müssen Sie das Kontrollkästchen **Zwingende Kreditlimite** im Formular **Kunden** auch auswählen, um das Kreditlimit des Debitors mit dem Saldo des Debitors zu überprüfen. Weitere Informationen zu Kreditlimittypen finden Sie unter, "Für welche Dokumente und Prozesse kann ich Kreditlimits überprüfen?" in diesem Thema. in diesem Artikel. 

**Wie überprüfe ich Kreditlimits für Aufträge manuell?**

Manchmal können Sie das Kreditlimit eines Debitors manuell prüfen. Beispielsweise können Sie manuell das Kreditlimit eines Debitors prüfen, bevor Sie mit der Eingabe eines Auftrags beginnen. Sie können das Formular **Verkaufsauftrag** verwenden, um Kreditlimits manuell zu überprüfen. Sie müssen Mitglied einer Sicherheitsrolle ein, der die Aufgabe Aufträge verwalten (SalesOrderMaintain) zugewiesen ist, um Änderungen in diesem Formular vorzunehmen.

1.  Klicken Sie auf **Vertrieb und Marketing** \> **Aufträge** \> **Alle Aufträge**. Doppelklicken Sie auf einen Auftrag.

2.  Klicken Sie im Aktivitätsbereich auf der Registerkarte **Verkaufsauftrag** in der Gruppe **Verwalten** auf **Kreditlimite überprüfen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]