---
title: Fremdarbeit
description: Dieses Thema können Sie eine, einschließlich Zulieferung exemplarischen Vorgehensweise der bei der Herstellung in Dynamics 365 Supply Chain Managementerstellen.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981455"
---
# <a name="subcontracting"></a>Fremdarbeit

[!include [banner](../includes/banner.md)]

Dieses Thema können Sie eine, einschließlich Zulieferung exemplarischen Vorgehensweise der bei der Herstellung in Microsoft Dynamics 365 Supply Chain Management erstellen. Der erste Teil dieses Themas beschreibt die Einstellungen der Daten. Der zweite Teil führt Sie durch die Schritte der exemplarischen Vorgehensweise.

## <a name="target-audience"></a>Zielgruppe

In diesem Thema erfahren Sie, wie Fremdarbeit der Herstellung eingerichtet wird. Sie können vorhandene Daten in der HQUS-juristischen Person nutzen, um die Basiseinstellungen eines Fremdarbeitsaktivitätsflusses einzurichten. Die Demodaten in der HQUS-juristischen Person enthält Einstellungsparameter, die vorab eingerichtet wurden, um die Schritte in der exemplarischen Vorgehensweise zu unterstützen. Obwohl die exemplarische Vorgehensweise zentrale Probleme und Herausforderungen für verschiedene Rollen adressiert, kann dies vom Systemadministrator ausgeführt werden. können.

## <a name="demo-scenario"></a>Vorführungsszenario

In der HQUS-juristischen Person sind Spitzenlautsprecher hergestellt. Während des Fertigungsprozesses durchlaufen die Lautsprecher die drei folgenden Arbeitsgänge.

- **Vormontage** – Das Lautsprechergehäuse wird zusammengestellt. Das Material für das Gehäuse wird dem Formular Lagerort entnommen, bevor der Arbeitsgang gestartet wird.
- **Beschichten** – Wenn das Lautsprechergehäuse zusammengestellt wurde, muss es überzogen sein. Dieser Arbeitsgang wird von einem Lieferanten (Zulieferer) ausgeführt. Das vormontierte Lautsprechergehäuse wird zusammen mit dem Beschichtungszulieferer mit zwei Materialien geliefert.
- **Fertig stellen** – Wenn das vormontierte Lautsprechergehäuse durch den Zulieferer beschichtet wurde, wird es an die HQUS-juristische Person zurückgegeben, sodass die Endmontage des Lautsprechers abgeschlossen werden kann.

Die folgende Abbildung zeigt die drei Arbeitsgängen und das Material an, das sie brauchen.

![Vormontage-, Beschichtungs- und Endarbeitsgänge und das Material, das sie verbrauchen](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Einrichten

Damit Sie die exemplarischen Vorgehensweise beginnen können, müssen Sie die Daten einrichten.

### <a name="set-up-the-finished-product"></a>Fertiges Produkt einrichten

Diese Verfahren führt Sie durch das Einrichten des freigegebenen Produkts D8100, "beschichtetes Gehäuse."

1. Wählen Sie **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**, um die Seite **Details für freigegebene Produkte** zu öffnen.
2. Im Schnellfilterfeld geben Sie **D8100** ein, um das vorhandene freigegebene Produkt zu suchen.

    ![Filter für D8100 freigegebenes Produkt auf der Seite der Details für freigegebene Produkte](./media/subcontract02_filtering-released-products.png)

3. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Entwickler**, wählen Sie **Arbeitsplan**, um die Seite **Arbeitsplan** zu öffnen.

    Die Seite **Arbeitsplan** enthält die acht Arbeitsplanversionen für D8100 freigegebenes Produkt. Die acht Arbeitsplanversionen werden auf vier Arbeitsplänen auf Standort 1 und 5. Standort aufgeteilt. Arbeitsplan 000400 wird für die Nachkalkulation verwendet, Arbeitsplan 00041 wird verwendet, wenn der Beschichtungsarbeitsgang ein interner Arbeitsgang und Arbeitsplan 00042 wird verwendet, wenn der Beschichtungsarbeitsgang eine externe Verarbeitung ist.

    ![Acht Arbeitsplanversionen auf der Arbeitsplanseite](./media/subcontract03_route-page.png)

4. Im oberen Bereich im Raster **Versionen**, wählen Sie **00042** Arbeitsplanversion für Standort **5** aus.
5. Im unteren Bereich auf der Registerkarte **Überblick**, Auswahloperation **20** (**Cbnt CtSc**) im Raster.

    ![Arbeitsgang 20 für Arbeitsplanversion 00042 für den Standort 5 ausgewählt.](./media/subcontract04_route-version-operation.png)

6. Wählen Sie die Registerkarte **Allgemein**.

    Beachten Sie, dass das Feld Feld **Arbeitsplantyp** auf **Lieferant** festgelegt ist. Dieser Wert gibt an, dass Arbeitsgang 20 (Cbnt CtSc) ein geregelter Arbeitsgang ist.

    ![Führen Sie den Feldtyp auf den Lieferant in der Registerkarte "Allgemeines"](./media/subcontract05_general-tab.png)

7. Wählen Sie die Registerkarte **Ressourcenanforderung**.

    Funktionen werden verwendet, um eine zutreffender Ressource bei der Produktionsplanung zu finden. Für Arbeitsgang 20 (Cbnt CtSc) beachten Sie, dass eine Ressource zwei Funktionen erfordert, nämlich **Beschichten** und **Überzogene Gehäuse**.

    ![Beschichten und überzogene Gehäusefunktionen auf der Ressourcenanforderungsregisterkarte](./media/subcontract06_resource-requirements-tab.png)

8. Wählen Sie **Anwendbare Ressourcen**, um das Dialogfeld **Anwendbare Ressourcen** zu öffnen.

    Drei Ressourcen werden gesucht, die mit den Ressourcenanforderungen für den Arbeitsgang übereinstimmen Beachten Sie, dass Ressource 8851 und 8852 vom Typ **Kreditor** sind.

    ![Drei entsprechende Ressourcen im Dialogfeld Anwendbare Ressourcen](./media/subcontract07_applicable-resources-dialog.png)

9. Wählen Sie **OK**, um das Dialogfeld **Anwendbare Ressourcen** zu schließen und zur Seite **Arbeitsplan** zurückzukehren.
10. Schließen Sie die Seite **Arbeitsplan**, um zur Seite **Details für freigegebene Produkte** zurückzukehren.

    ![Seite für freigegebene Produkte](./media/subcontract08_released-product-details-page.png)

11. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Entwickler**, wählen Sie **Stücklisten-Versionen**, um die Seite **Stücklisten-Versionen** zu öffnen.

    Die Seite **Stücklistenversionen** zeigt vier Stücklistenpositionen (BOM)- Versionen für freigegebenes Produkt D8100 an. Stückliste 000040 wird zur Nachkalkulation und Planung verwendet, Stückliste 000041 wird verwendet, wenn der Beschichtungsarbeitsgang intern erfolgt ist und Stücklisten 000042 und 000043 werden verwendet, wenn der Beschichtungsarbeitsgang abgezogen wird.

    Beachten Sie, dass Artikel S8050 ein Produkt vom Artikeltyp **Dienstleistung** ist. Dieser Artikel stellt die Fremdarbeit dar.

    ![Vier Stücklistenversionen auf der Stücklistenversionsseite](./media/subcontract09_bom-versions-page.png)

12. Auf dem Inforegister **Stücklistenpositionen** aktivieren Sie **Bearbeiten**, um das Dialogfeld **Stücklistenposition bearbeiten** zu öffnen.

    Wenn ein Produktionsauftrag für das freigegebene Produkt D8100 erstellt und vorkalkuliert wird, wird automatisch eine Bestellung für Artikel S8050 generiert. Diese Bestellung wird mit dem Produktionsauftrag verknüpft. Damit Bestellungen automatisch generiert werden können, müssen Sie das Feld **Positionstyp** auf **Lieferant** festlegen und der Kreditor für den Zulieferer ausgewählt werden. In diesem Fall ist das Kreditorenkonto US-801.

    Beachten Sie, ob die Stücklistenposition mit dem Beschichtungsarbeitsgang durch die Arbeitsgangnummer verbunden ist (in diesem Fall 20).

    ![Bearbeiten Sie das Stücklistenpositionsdialogfeld](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Erstellen Sie ein Kennwort für Lagerarbeiter

Sie müssen ein Kennwort für die Lagerarbeiter definieren, die das tragbare Gerät verwenden.

1. Wählen Sie **Lagerortverwaltung \> Einstellungen \> Arbeitskraft**, um die Seite **Arbeitsbenutzer** zu öffnen.
2. Auf dem Inforegister **Benutzer** aktivieren Sie die Zeile für Benutzer **51** aus.

    ![Arbeitsbenutzer-Seite](./media/subcontract11_work-users-page.png)

3. **Kennwortzurücksetzung** auswählen.
4. Wählen Sie in den Feldern **Kennwort** und **Kennwort bestätigen** und geben Sie **1** ein.
5. **Kennwortzurücksetzung** auswählen.

## <a name="step-by-step-walkthrough"></a>Schrittweise Vorgehensweise

**Szenario und Hintergrund**

Ein Produktionsauftrag von 10 Stück wird erstellt für Produkt D8100, "Beschichtetes Gehäuse." Die Beschichtung der Gehäuse ist ein geregelter Arbeitsgang, der beim Lieferant US-801 Kreditor geleistet wird, perfekte Beschichtungs-Lösungen. Der Produktionsauftrag besteht aus drei Arbeitsgängen. Im ersten Arbeitsgang wird das Gehäuse als interner Arbeitsgang vormontiert. Das Material für die Vormontage ist für Entnahme im Rohmateriallagerort freigegeben. Nachdem die Vormontage abgeschlossen wurde, wird das vormontierte Gehäuse zu den perfekten Beschichtungs-Lösungen zusammen mit zwei Materialien gesendet, die für den Beschichtungsarbeitsgang erforderlich sind. Wenn das beschichtete Gehäuse vom Lieferant zurückkommt, geht es abschließenden zur internen Assemblierung, bevor es als fertig gemeldet wird.

1. Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.
2. Klicken Sie im Aktivitätsbereich und wählen Sie **Neuer Produktionsauftrag**, um das Dialogfeld **Produktionsauftrag erstellen** zu öffnen.

    ![Dialogfeld "Geplanten Produktionsauftrag erstellen".](./media/subcontract12_create-production-order-dialog.png)

3. Wählen Sie im Feld **Artikelnummer** die Option **D8100** aus.
4. Das Feld "Lagerungsdimensionen" wird angezeigt, wenn Sie die Artikelnummer auswählen. Im Feld **Farbe** wählen Sie **Chrome** aus.

    Ein Meldungsfeld angezeigt wird, die fragt, ob die aktive Versionen für die Stückliste und den Arbeitsplan eingefügt werden sollen.

    ![Meldungsfeld](./media/subcontract13_message-box.png)

5. Wählen Sie **Ja** aus. 

    Im Dialogfeld **Produktionsauftrag erstellen** werden die aktiven Versionen der Stückliste und der Arbeitsplan für Produkt D8100 automatisch in den Feldern **Stücklistennummer** und **Arbeitsplannummer** ausgewählt. In diesem Fall werden Stückliste **000040** und Arbeitsplan **000040** ausgewählt.
    
    > [!NOTE]
    > Für die Stückliste und Arbeitsplan wird Version 000040 zur Nachkalkulation und Planung verwendet.

6. Im Feld **Standort** wählen Sei **5** aus.
7. Im Feld **Lagerort** wählen Sie **51** aus.
8. In den Feldern **Stücklistennummer** und **Arbeitsplannummer** ändern Sie den Wert, der automatisch für **000042** ausgewählt wurde.

    > [!NOTE]
    > Für die Stückliste und den Arbeitsplan wird Version 000042 verwendet, um die Beschichtung des Gehäuses für Lieferant US-801 zu regeln.

    ![Werte festgelegt im Dialogfeld Produktionsauftrag](./media/subcontract14_create-production-order-dialog-set.png)

9. Wählen Sie **Erstellen**, um den Produktionsauftrag zu erstellen und zur Seite **Alle Produktionsaufträge** zurückzukehren.

    ![Neuer Produktionsauftrag auf der Seite alle Produktionsaufträge](./media/subcontract15_new-production-order.png)

10. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Schätzung**, um das Dialogfeld **Schätzung** zu öffnen.

    ![Dialogfeld Vorkalkulation](./media/subcontract16_estimate-dialog.png)

11. Wählen Sie **Ok**, um die Vorkalkulation zu bestätigen und kehren Sie zur Seite **Alle Produktionsaufträge** zurück.

    > [!NOTE]
    > Wenn der Produktionsauftrag vorkalkuliert wird, ist die Bestellung für Dienstleistungsartikel S8050 für Kreditor US-801 generiert.

12. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Produktionsauftrag**, wählen Sie **Stückliste**, um die Seite **Stückliste** zu öffnen, in der die Stücklistenpositionen für den Produktionsauftrag angezeigt werden können.

    Für Dienstleistungsartikel S8050 beachten Suem, dass es eine Referenz zur Bestellung gibt, die erstellt wurde, als der Produktionsauftrag vorkalkuliert wurde.

    ![Produktionsauftrags-Stücklistenposition auf der Seite Stückliste](./media/subcontract17_production-order-bom-lines.png)

13. Schließen Sie die Seite **Stückliste**, um zur Seite **Alle Produktionsaufträge** zurückzukehren.
14. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Zeitplan** und wählen **Aufträge planen**, um das Dialogfeld **Auftragsplanung** zu öffnen.
15. Füllen Sie die folgenden Werte aus:

    - Wählen Sie im Feld **Planungsrichtung** **Vorwärts ab Lieferdatum** aus.
    - Hier können Sie die Option **Begrenzte Kapazität** auf **Ja** festlegen.

    ![Dialogfeld Feinterinierung](./media/subcontract18_job-scheduling-dialog.png)

16. Wählen Sie **OK**, um das Dialogfeld **Feinterminierung** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.
17. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Planung**, wählen Sie **Gantt**, um die Seite **Gantt-Diagramm - Ressourcenansicht** zu öffnen.

    Im Gantt-Diagramm wird eine visuelle Übersicht bereitgestellt, die zeigt, wie Produktions-Einzelvorgänge für die Ressourcen geplant werden. Beachten Sie, dass der externe Beschichtungsarbeitsgang aus drei Einzelvorgängen besteht: Ein Bearbeitungseinzelvorgänge, ein Abschluss und ein Wartezeiteinzelvorgang.

    ![Gantt-Diagramm auf der Gantt-Diagramm-Ressourcenansichtsseite](./media/subcontract19_gantt-chart.png)

18. Schließen Sie die Seite **Gantt-Diagramm - Ressourcenansicht**, um zur Seite **Alle Produktionsaufträge** zurückzukehren.
19. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Freigabe**, um das Dialogfeld **Freigabe** zu öffnen.

    ![Dialogfeld Freigabe](./media/subcontract20_release-dialog.png)

20. Klicken Sie auf **OK**, um das Dialogfeld **Freigabe** zu schließen.
21. Wählen Sie **Produktionssteuerung \> Periodische Aufgaben \> Freigabe Lagerort \> Automatische Version der Stückliste und der Formelpositionen**, um das Dialogfeld **Automatische Version der Stückliste und der Formelpositionen** zu öffnen.

    ![Dialogfeld automatische Freigabe von Stücklisten- und Formelpositionen](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Wählen Sie **OK** aus, um die automatische Freigabe des Stücklisten- und Formelpositionseinzelvorgangs auszuführen.

    Dieser Einzelvorgang gibt Entnahmearbeit für Rohmaterialen an den Lagerort frei.

23. Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.
24. Verwenden Sie d die Schnellfilterung, um den Produktionsauftrag auszuwählen, an dem Sie gearbeitet haben.
25. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Lagerhaus**, wählen Sie **Arbeitsdetails**, um die Seite **Arbeit** zu öffnen.

    Beachten Sie, dass die Seite zwei Sätze Arbeit für Rohmaterialentnahmen anzeigt. Die erste Arbeit ist für Material M8100 und M8101. Deise Materialien werden auch vom Vorgang 10 verbraucht. Die zweite Arbeit ist für Material M8202 und M8250. Diese Materialien werden von Arbeitsgang 20 verbraucht, welcher ein geregelter Arbeitsgang ist.

    ![Zwei Sätze Arbeit für Rohmaterialentnahmen auf der Seite Arbeit](./media/subcontract22_work-page.png)

26. Starten Sie die Lagerort-App, um die Lagerortarbeit für Arbeitsgang 10 zu verarbeiten.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Wählen Sie **Produktionssteuerung \> Produktionsaufträge \> Alle Produktionsaufträge**, um die Seite **Alle Produktionsaufträge** zu öffnen.
28. Verwenden Sie d die Schnellfilterung, um den Produktionsauftrag auszuwählen, an dem Sie gearbeitet haben.
29. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Start**, um das Dialogfeld **Start** zu öffnen.
30. Definieren Sie auf der Registerkarte **Allgemeines** die folgenden Werte

    - Im **Von Arbeitsgangnr.** Feld wählen Sie **10**.
    - Im **Zu Arbeitsgangnr.** Feld wählen Sie **10**.

    ![Werte festgelegt auf der Registerkarte "Allgemeines"](./media/subcontract23_start-dialog.png)

31. Wählen Sie **OK**, um das Dialogfeld **Start** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.

    Beachten Sie, dass der Status des Produktionsauftrags nun **Gestartet** ist. Die Materialien für Arbeitsgang 10 werden durch eine automatische Buchung der Kommissionierlistenerfassung verbraucht. Der Zeitverbrauch für Arbeitsgang 10 wird durch eine automatische Buchung einer Arbeitsplanlisten-Erfassung angegeben.

32. Starten Sie die Lagerort-App, um die Lagerortarbeit für Arbeitsgang 20 zu verarbeiten.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Klicken Sie im Aktivitätsbereich auf die Registerkarte **Produktionsauftrag** und wählen **Start**, um das Dialogfeld **Start** zu öffnen.
34. Definieren Sie auf der Registerkarte **Allgemeines** die folgenden Werte

    - Im **Von Arbeitsgangnr.** Feld wählen Sie **20**.
    - Im **Zu Arbeitsgangnr.** Feld wählen Sie **20**.
    - Geben Sie im Feld **Menge** den Wert **10** ein.
    - Wählen Sie im Feld **Kommissionierliste jetzt buchen** die Antwort **Nein** aus.

    ![Werte festgelegt auf der Registerkarte "Allgemeines"](./media/subcontract24_general-tab.png)

35. Wählen Sie **OK**, um das Dialogfeld **Start** zu schließen und zur Seite **Alle Produktionsaufträge** zurückzukehren.

    Eine Kommissionierliste wird für die Materialien, die für den Beschichtungsarbeitsgang verwendet werden und für Dienstleistungsartikel erstellt. Der Dienstleistungsartikel stellt die Kosten des geregelten Arbeitsgangs dar.

36. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Ansicht**, wählen Sie **Kommissionierliste**, um die Seite **Kommissionierliste** zu öffnen.
37. Wählen Sie die Kommissionierliste, die nicht gebucht wurde, und wählen Sie dann die Erfassungsnummer aus, um die Erfassungspositionen anzuzeigen.

    ![Erfassungsposition auf der Seite Kommissionierliste](./media/subcontract25_picking-list.png)

38. Klicken Sie im Aktivitätsbereich **Drucken** \> wählen Sie **Kommissionierlistenbericht**, um das Dialogfeld **Kommissionierlistenbericht** zu öffnen.
39. Hier können Sie die Option **Lieferscheinlayout verwenden** auf **Ja** festlegen.

    ![Dialogfeld Kommissionierlistenbericht](./media/subcontract26_picking-list-report-dialog.png)

40. Wählen Sie **OK**, um den **Kommissionierlisten**-Bericht zu erstellen.

    In diesem Fall wird ein Lieferschein des Kreditors aus der Produktionskommissionierlistenerfassung gedruckt. Der Lieferschein zeigt die Materialien an, die an den Kreditor gesendet werden, der den Beschichtungsarbeitsgang durchführt.

    ![Bericht 'Kommissionierliste'](./media/subcontract27_picking-list-report.png)

41. Beenden Sie den Bericht **Kommissionierliste**, um zur Seite **Kommissionierliste** zurückzukehren.
42. Im Aktivitätsbereich wählen Sie **Buchen**, um das Dialogfeld **Erfassung buchen** zu öffnen.

    ![Dialogfeld Erfassung buchen](./media/subcontract28_post-journal-dialog.png)

43. Klicken Sie auf **OK**, um das Dialogfeld **Erfassung buchen** zu schließen.
44. Bestellpositionen öffnen.

    ![Seite Bestellungen](./media/subcontract29_purchase-order-page.png)

45. Klicken Sie im Aktivitätsbereich auf der Registerkarte auf **Einkauf** und wählen Sie **Bestätigen**.
46. Klicken Sie auf **Buchen**, um das Dialogfeld **Erfassung buchen** zu schließen.
47. Wählen Sie **OK**, um das Dialogfeld **Erfassung buchen** zu schließen und zur Seite **Alle Bestellungen** zurückzukehren.
48. Ändern Sie den Preis je Einheit von **33** in **40**.

    ![Preis je Einheit auf der Bestellungsseite geändert](./media/subcontract30_unit-price.png)

49. Dient zur erneuten Bestätigung der Bestellung.
50. Produktzugang.

    ![Dialogfeld Buchen des Produktzugangs](./media/subcontract31_posting-product-receipt-dialog.png)

51. Rechnung Bestellung
52. Status des Abgleichs aktualisieren.

    ![Seite Kreditorenrechnung](./media/subcontract32_vendor-invoice-page.png)

53. Fertigmeldung.

    ![Dialogfeld Fertigmeldung](./media/subcontract33_report-as-finished-dialog.png)

54. Beenden.

    ![Dialogfeld beenden](./media/subcontract34_end-dialog.png)

55. Kostenvergleich.

    ![Diagramme Kostenvergleich](./media/subcontract35_cost-comparison-charts.png)

Fehlende Daten in Unternehmensdaten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]