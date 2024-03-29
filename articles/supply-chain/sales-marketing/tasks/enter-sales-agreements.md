---
title: Verkaufsverträge eingeben
description: Dieser Artikel erklärt, wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b3aa72057753a9592fd47275dc996a3a904d86b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897486"
---
# <a name="enter-sales-agreements"></a>Verkaufsverträge eingeben

[!include [banner](../../includes/banner.md)]

Dieser Artikel erklärt, wie Sie einen Kaufvertrag erstellen, der einen Debitor verpflichtet, ein Produkt in einer bestimmten Menge über einen vorgegebenen Zeitraum zu erwerben, wobei ihm im Gegenzug Rabatte zustehen. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen.


## <a name="set-up-sales-agreement-header"></a>Kaufvertragskopfzeile einrichten
1. Gehen Sie im Navigationsbereich zu **Module > Vertrieb und Marketing > Kaufverträge > Kaufverträge**.
2. Wählen Sie **Neu** aus.
3. Wählen Sie im Feld **Kundenkonto** den gewünschten Datensatz aus dem Dropdown-Menü aus.
4. Wählen Sie im Feld **Kaufvertragsklassifizierung** den gewünschten Datensatz aus dem Dropdown-Menü aus.
5. Erweitern Sie den Abschnitt **Allgemein**.
6. Wählen Sie im Feld **Standardzusage** **Produktwertzusage** aus. Ein Zusagetyp ist ein erforderliches Kriterium, das Sie Verträgen zuweisen müssen, um zu definieren, wie Vertrag erfüllt wird. Mit den vier vordefinierten Typen können Sie das Zusageziel des Debitors einrichten (als Menge bzw. Wert). Der Mengenzusagetyp kann nur auf ein bestimmtes Produkt angewendet werden. Die wertbasierten Typen sind auf den Verkauf bestimmter und unspezifischer Produkte anwendbar.  
7. Legen Sie im Feld **Ablaufdatum** das Datum auf das zukünftige Datum fest, an dem Sie die Vereinbarung abzulaufen soll.
8. Wählen Sie **OK**.

## <a name="set-up-product-value-commitment-lines"></a>Produktwertzusagepositionen einrichten
1. Wählen Sie **Position hinzufügen** aus.
2. Wählen Sie im Feld **Artikelnummer** den gewünschten Datensatz aus dem Dropdown-Menü aus. Der Typ der Zusage, den Sie für die Vereinbarung ausgewählt haben, betrifft die Art der Informationen, die Sie für die Vereinbarungspositionen eingeben können. Für eine wertbasierte Vereinbarung müssen Sie zum Beispiel den Gesamtnettobetrag (in der vereinbarten Währung) für den der Debitor den Kauf von Waren von Ihnen zusagt angeben. In diesem Beispiel sind die Felder **Menge** und **Einheit** in der Position nicht verfügbar, da Sie eine Vereinbarung für den Kunden zum Kauf eines bestimmten Wertes für ein Produkt erstellen.   
3. Im Feld **Nettobetrag** geben Sie den Geldbetrag ein, den der Debitor für den Einkauf zugesagt hat.
4. Geben Sie im Feld **Rabattprozent** einen Prozentwert ein, der für die Auftragspositionen des Debitors gilt, die dieser Vereinbarung zugeordnet sind.
5. Erweitern Sie den Abschnitt **Positionsdetails**.
6. Wählen Sie **Ja** im Feld **Maximum wird erzwungen** aus.
    - Die Auswahl von **Maximum wird erzwungen** bedeutet, dass der Gesamtbetrag aller Auftragspositionen, die die Sonderpreise der Zusage, Rabatte und/oder Zahlungsbedingungen verwenden, den für die Zusage angegeben Betrag nicht überschreiten darf.  
    - Die minimalen und maximalen Freigabemengen geben einen Wertebereich an, für bei jedem Auftrag verkauft werden muss, der die ausgewählte Vereinbarung verwendet.   
7. Erweitern Sie den Abschnitt **Kaufvertragskopf**. Solange der Status der Vereinbarung nicht auf **Effektiv** festgelegt ist, können Aufträge nicht dem Vertrag zugeordnet werden. Sie können daher nicht zur Erfüllung dieser Vereinbarung beitragen. Der können den Status zu diesem Zeitpunkt manuell ändern. Allerdings wird der Status normalerweise geändert, wenn die Vereinbarung für den Debitor bestätigt wird.  
8. Wählen Sie im Aktivitätsbereich **Kaufvertrag** aus.
9. Wählen Sie **Bestätigung** aus. Stellen Sie sicher, dass die Option **Vertrag als 'Effektiv' kennzeichnen** auf **Ja** festgelegt ist.  
10. Wählen Sie **Ja** im Feld **Bericht drucken** aus.
11. Wählen Sie **OK**.
12. Schließen Sie die Seite. Die Vereinbarung ist jetzt wirksam. Sie können jetzt Kundenaufträge mit der Vereinbarung verknüpfen, um diese dem Zusageziel zuzurechnen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]