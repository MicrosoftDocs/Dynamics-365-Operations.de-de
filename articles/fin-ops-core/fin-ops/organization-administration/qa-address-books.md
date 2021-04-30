---
title: Adressbücher – Häufig gestellte Fragen
description: In diesem Thema finden Sie Antworten auf häufig gestellte Fragen zu Adressbüchern.
author: msftbrking
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2f81b6c3ab60f5e0e852d2bc0ae44e6595a90c1
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906672"
---
# <a name="address-books-faq"></a>FAQs zu Adressbüchern

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Wie prüfe ich auf doppelte Verzeichnisdatensätze?

Sie können direkt über die Listenseite **Globales Adressbuch** auf Duplikatdatensätze prüfen. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Partei** in der Gruppe **Verwalten** und auf **Auf Duplikate überprüfen**. Wählen Sie dann die Werte aus, die Sie in die Duplikatprüfung einbeziehen möchten:

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Kann ich Parteidatensätze aus einem Adressbuch massenhinzufügen oder -löschen?

Ja, Sie können mehrere Parteidatensätze aus einem Adressbuch hinzufügen und mehrere Parteidatensätze entfernen.

- Wenn Sie mehrere Parteidatensätze zu einem Adressbuch hinzufügen möchten, wählen Sie auf der Listenseite **Globales Adressbuch** die Parteien in der Liste aus. Klicken Sie anschließend im Aktivitätsbereich die **Partei**-Registerkarte und klicken Sie in der Gruppe **Verwalten** auf **Parteien zuweisen**. Wählen Sie die Adressbücher, denen die ausgewählten Parteidatensätze hinzugefügt werden sollen, und klicken Sie dann auf **OK**. Alle ausgewählten Parteidatensätze werden allen ausgewählten Adressbüchern hinzugefügt.
- Wenn Sie mehrere Parteidatensätze aus einem Adressbuch entfernen möchten, wählen Sie auf der Listenseite **Globales Adressbuch** die Parteien in der Liste aus. Klicken Sie anschließend im Aktivitätsbereich die **Partei**-Registerkarte und klicken Sie in der Gruppe **Verwalten** auf **Parteien entfernen**. Wählen Sie die Adressbücher aus, aus denen die Parteien entfernt werden sollen, und klicken Sie dann auf **OK**. Alle ausgewählten Parteidatensätze aus allen ausgewählten Adressbüchern entfernt.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Kann ich den Parteityp eines Datensatzes ändern, oder muss ich den alten Datensatz löschen und ein neuen Datensatz erstellen?

Es kann vorkommen, dass Sie einen Parteityp für einen Datensatz ändern müssen, um den Parteityp von Person zu Organisation oder von Organisation zu Person zu ändern. Beispielsweise ist Nancy Mitglied des Vertriebsteams für Fabrikam Großbritannien. Auf einer Messe in London trifft sie sechs neue Interessenten. Nancy erstellt einen Interessentenparteidatensatz für die einzelnen Interessenten. Wenn Nancy die Datensätze speichert, wird jeder Datensatz auch im globalen Adressbuch erstellt. Fabrikam hat den standardmäßigen Parteityp auf Organisation festgelegt, aber zwei der neuen Interessenten sollen einen Datensatztyp Personen erhalten. Wenn Nancy von der Messe zurückkehrt, muss sie den Parteityp der beiden Interessentendatensätze ändern. Um einen Parteidatensatz von einem Parteityps in einen anderen zu ändern, müssen Sie zunächst einen neuen Parteidatensatz mit dem richtigen Typ im globalen Adressbuch erstellen. Sie ordnen dann den alten Parteidatensatz diesem neuen Datensatz zu. Nachdem Sie die neue Parteizuweisung erstellt haben, löschen Sie den ursprünglichen Parteidatensatz, der den falschen Datensatztyp hat.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Wie ändere ich den Namen oder die Adresse eines Parteidatensatzes?

Sie können den Namen eines Parteidatensatzes und die Adressen die diesem Datensatz zugeordnet sind jederzeit aktualisieren.

- Um Sie den Namen eines Parteidatensatzes zu aktualisieren, öffnen Sie den Parteidatensatz und klicken dann auf **Bearbeiten**. Geben Sie auf dem **Allgemeines**-Inforegister den neuen Namen für die Partei ein, und speichern Sie anschließend den Datensatz.
- Wenn Sie eine Adresse für einen Parteidatensatz aktualisieren möchten, öffnen Sie den Parteidatensatz und wählen dann auf dem Inforegister **Adressen** die zur aktualisierende Adresse aus. Klicken Sie auf **Bearbeiten** und führen Sie dann auf der Seite **Adresse bearbeiten** die erforderlichen Änderungen an der Adresse oder den Adressenparametern durch.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Kann ich zwei oder mehr Parteidatensätze in einen Datensatz zusammenführen?

In bestimmten Fällen sollten Sie zwei oder Parteidatensätze in einem Datensatz zusammenführen. Dies kann vorkommen, wenn Sie absichtlich oder unabsichtlich zwei oder mehr doppelte Parteidatensätze erstellt haben. Wählen Sie beim Zusammenführen von Parteidatensätzen einen Datensatz aus, der beibehalten wird. Die Informationen aus den anderen Datensätzen werden in diesem Datensatz zusammengeführt. Angenommen, Sie stellen fest, dass Informationen zu Fabrikam in den drei Parteidatensätzen A, B und C gespeichert sind. Sie legen fest, dass Parteidatensatz A beibehalten wird. Daher werden die in den Parteidatensätzen B und C gespeicherten Informationen im Parteidatensatz A zusammengeführt. Es gibt Situationen, in denen Sie Parteidatensätze nicht zusammenführen können:

- Es können keine Parteidatensätze zusammengeführt werden, die derselben Parteirolle, wie Debitor oder Kreditor, in derselben juristischen Person zugeordnet sind. Angenommen, Partei A ist einem Debitor in der juristischen Person 123 und Partei B ist einem anderen Debitor in der juristischen Person 123 zugeordnet. Diese Parteidatensätze können nicht zusammengeführt werden, da der zusammengeführte Parteidatensatz mehreren Debitoren in derselben juristischen Person zugeordnet wäre, was nicht zulässig ist. Die Datensätze können jedoch zusammengeführt werden, wenn Partei B einem Debitor in der juristischen Person 123 oder einem Debitor in einer anderen juristischen Person zugeordnet ist.
- Datensätze von internen Parteiorganisationen können nicht in derselben juristischen Person, Organisationseinheit oder im selben Team zusammengeführt werden.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Soll ich einen Parteidatensatz im globalen Adressbuch oder an einem anderen Ort (z. B. auf der Debitoren- oder Kreditorenseite) erstellen?

Sie können Parteidatensätze entweder im globalen Adressbuch oder auf der entsprechenden Entitätsseite eingeben. Wird ein Datensatz in einem Ort hinzufügen, wird derselbe Datensatz immer am anderen Ort hinzugefügt. Wenn Sie beispielsweise einen Parteidatensatz für einen Debitor im globalen Adressbuch hinzufügen, wird der Datensatz auch auf der Seite **Debitor** hinzufügt. Wenn Sie einen Parteidatensatz auf der **Debitor**-Seite hinzufügen, wird der Datensatz ebenso zum globalen Adressbuch hinzufügt. Verwenden Sie die folgenden Richtlinien, um festzulegen, wo neue Parteidatensätze eingegeben werden sollen:

- **Erstellen eines Parteidatensatzes, wenn Sie den Entitätstyp nicht kennen**: Wenn Sie einen Parteidatensatz erstellen und den Entitätstyp nicht kennen, beispielsweise nicht wissen, wenn die Entität ein Debitor oder eine Verkaufschance ist, erstellen Sie den Datensatz im globalen Adressbuch. Sie können den Entitätstyp später auswählen.
- **Erstellen eines Parteidatensatzes, wenn Sie den Entitätstyp kennen**: Wenn Sie den Entitätstyp für die Partei kennen, können Sie einen Datensatz in der maßgeblichen Formular für diesen Typ erstellen. Beispielsweise können Sie für einen Debitor einen Datensatz im Formular **Debitor** erstellen. Wenn Sie mit dem entsprechenden Formular für eine Entität einen Datensatz erstellen und speichern, wird der Datensatz automatisch im globalen Adressbuch erstellt.

## <a name="can-i-translate-address-information-for-party-records"></a>Kann ich Adressinformationen für Parteidatensätze übersetzen?

Sie können Übersetzungen von Adressinformationen einrichten, damit die Information in Ihrem Programm in der Sprache des Benutzers (Systemsprache) und in anderen Dokumenten, wie z. B. Aufträgen, in einer anderen Sprache angezeigt wird. Sie können Übersetzungen für Namen von Ländern/Regionen, zu Adresszwecken und Namensfolgen eingeben. Ihre Systemsprache ist z. B. Dänisch, und Sie erstellen einen Auftrag für einen Kunden in Frankreich. In diesem Fall können Sie den Debitorendatensatz auf Dänisch im Programm anzeigen, die Adressinformationen jedoch in dem gedruckten Auftrag auf französisch anzeigen. Wenn Sie Übersetzungen einrichten, sollten Sie eine Übersetzung für jeden Artikel in der Liste eingegeben. Alle Artikel, für die Sie keine Übersetzung eingeben, werden in der Systemsprache angezeigt. Ihre Systemsprache ist z. B. Dänisch, und Sie senden ein Dokument an einen Kunden in Spanien. Wenn Sie keine spanischen (ESP) Übersetzungen für die Adressdaten eingegeben haben, werden die Informationen im System und auf gedruckten Materialien auf Dänisch angezeigt.

## <a name="after-importing-addresses-when-i-access-the-records-why-am-i-unable-to-edit-imported-addresses"></a>Warum kann ich, wenn ich nach dem Importieren von Adressen auf die Datensätze zugreife, importierte Adressen nicht bearbeiten?

Beim Importieren von Adressen wird ein Feld mit der Bezeichnung **IsLocationOwner** angezeigt. Dies gibt an, ob die Partei, die dem Standort (der Adresse) zugeordnet ist, der Eigentümer der Adresse ist. Wenn die Partei der Eigentümer der Adresse ist, kann die Adresse beim Zugriff über die Partei im globalen Adressbuch oder über das Masterdatensatzformular (z. B. Debitor, Kreditor oder Arbeitskraft) bearbeitet werden. Wenn die Partei nicht der Eigentümer der Adresse ist, kann der Datensatz nicht über die zuvor aufgelisteten Formulare bearbeitet werden. Beim Importieren von Adressen sollte **IsLocationOwner** auf **Ja** eingestellt werden, wenn Sie möchten, dass die Adresse über die zugeordnete Partei bearbeitet werden kann. Es gibt jedoch Situationen, in denen dieses Feld falsch importiert wird. Um dieses Problem zu beheben, kann der Standorteigentümer im globalen Adressbuch über den Datensatz der Partei oder über die Seite **Standorteigentümer bestätigen** aktualisiert werden. Um einen einzelnen Parteidatensatz zu aktualisieren, rufen Sie **Globales Adressbuch > Adresse** auf. Wählen Sie **Bearbeiten** aus, um die Seite **Adresse bearbeiten** zu starten und den Standorteigentümer zu ändern. Wählen Sie **Standorteigentümer ändern** aus, um den vorherigen Standorteigentümer anzuzeigen, wobei die aktuell ausgewählte Partei der neue Standorteigentümer ist. Wenn kein vorheriger Standorteigentümer angegeben ist, bedeutet dies, dass kein Standorteigentümer eingerichtet wurde. Wird die Option **Erweitert** ausgewählt, öffnet sich die Seite **Adressen verwalten**, auf der der Standorteigentümer ebenfalls festgelegt werden kann. Wählen Sie den zu aktualisierenden Standort aus, und wählen Sie anschließend im Menü **Standorteigentümer festlegen** aus. Um den Standorteigentümer für mehrere Datensätze zu aktualisieren, rufen Sie **Globales Adressbuch > Standorte > Standorteigentümer bestätigen** auf. Die Liste enthält Standorte, die mit einer einzelnen Partei verknüpft sind. Diese Partei ist jedoch nicht der Eigentümer. Die Auswahl der Option **Eigentümer bestätigen** legt die **ID der vorgeschlagenen Eigentümerpartei** als den Eigentümer der verknüpften Adresse fest. Sobald die Partei als Eigentümer festgelegt wurde, kann die verknüpfte Adresse über den Datensatz der Partei bearbeitet werden. Um den Standorteigentümer ändern zu können, muss Ihnen die Berechtigung für **Standortbesitzer festlegen** auf der Seite **Sicherheitskonfiguration** zugewiesen werden.  Standardmäßig wird dem Systemadministrator diese Berechtigung gewährt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

