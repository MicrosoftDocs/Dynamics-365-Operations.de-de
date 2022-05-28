---
title: Steuerkomponenten für den Steuertyp „TDS“ einrichten
description: In diesem Thema wird erläutert, wie Sie Quellensteuerkomponenten für den die Quellenbesteuerung (Steuertyp „TDS“) einrichten. Außerdem wird erläutert, wie Sie den Schwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9c86341f7528e2c85b813e4f825ae34f10680a9b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727116"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Steuerkomponenten für den Steuertyp „TDS“ einrichten

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie Quellensteuerkomponenten für den die Quellenbesteuerung (Steuertyp „TDS“) einrichten. Die TDS-Komponenten lauten TDS, Aufpreis, PE-Sondersteuer und SHE-Sondersteuer. Außerdem wird in diesem Thema erläutert, wie Sie den Schwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird. Darüber hinaus können Sie einen Ausnahmeschwellenwert festlegen, der zur Berechnung der TDS für jede TDS-Komponente verwendet wird.

Gehen Sie folgendermaßen vor, um TDS-Komponenten einzurichten.

1. Gehen Sie zu **Steuer \> Setup \> Quellensteuer \> Quellensteuerkomponenten**.

    [![Seite „Quellensteuerkomponenten“.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Wählen Sie im Feld **Steuertyp** **TDS** aus, um Quellensteuerkomponenten für den Steuertyp TDS einzurichten.
3. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Position zu erstellen.
4. Geben Sie im Feld **Quellensteuerkomponente** einen Namen für die TDS-Komponente ein.
5. Wählen Sie im Feld **Quellensteuerkomponentengruppe** die TDS-Quellensteuerkomponentengruppe aus, mit der die TDS-Komponente verbunden werden soll.
6. Geben Sie auf dem Inforegister **Allgemein** im Feld **Beschreibung** eine Beschreibung der TDS-Komponente an.
7. Wählen Sie im Aktionsbereich die Option **Schwellenwert** aus, um die Seite **Schwellenwert** zu öffnen, damit Sie den Schwellenwert festlegen können, der zur Berechnung des TDS für die TDS-Komponente verwendet wird.
8. Verwenden Sie die Felder **Startdatum** und **Enddatum**, um den Zeitraum festzulegen, für den der Schwellenwert gilt.
9. Geben Sie im Feld **Allgemein** im Feld **Schwellenwert** den Schwellenwert ein, der zur Berechnung des TDS für die TDS-Komponente verwendet wird. Die Steuer wird an der Quelle erst abgezogen, wenn der kumulierte Rechnungsbetrag den Schwellenwert überschreitet.

    Wenn der Schwellenwert beispielsweise 10.000 beträgt, wird die TDS berechnet, nachdem der kumulierte Rechnungsbetrag 10.000 überschritten hat (mit anderen Worten, wenn er mindestens 10.001 beträgt).

10. Geben Sie im Feld **Ausnahmeschwellenwert** den Ausnahmeschwellenwert ein, der zur Berechnung des TDS für die TDS-Komponente verwendet wird. Die Steuer für eine Rechnungsposition wird an der Quelle erst abgezogen, wenn der Betrag den Ausnahmeschwellenwert überschreitet.

    Wenn der Ausnahmeschwellenwert beispielsweise 5.000 beträgt, wird die TDS für eine bestimmte Rechnungsposition berechnet, wenn der Betrag der Rechnungsposition 5.000 überschreitet (mit anderen Worten, wenn er mindestens 5.001 beträgt).

    [![Seite „Schwellenwerte“.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Der Ausnahmeschwellenwert muss kleiner oder gleich dem Schwellenwert sein.
    >
    > Die Steuer wird für eine Buchung abgezogen, wenn der Buchungsbetrag den Ausnahmeschwellenwert überschreitet, auch wenn der kumulierte Rechnungsbetrag den im Feld **Schwellenwert** angegebenen Schwellenwert nicht überschreitet.

11. Schließen Sie die Seite **Schwellenwert**, um zur Seite **Quellensteuerkomponenten** zurückzukehren.
12. Wählen Sie im Aktionsbereich **Kopieren** aus, um das Dialogfeld **Quellensteuerkomponenten kopieren** zu öffnen, damit Sie die TDS-Komponenten, die für eine TDS-Komponentengruppe eingerichtet wurden, in eine andere TDS-Komponentengruppe kopieren können.
13. Wählen Sie im Feld **Von** die TDS-Komponentengruppe aus, aus der die TDS-Komponenten kopiert werden sollen. Wählen Sie im Feld **Nach** die Quellensteuerkomponentengruppe aus, in die die TDS-Komponenten kopiert werden sollen.

    > [!NOTE]
    > Gemeinsame TDS-Komponenten, die mit beiden TDS-Komponentengruppen verbunden sind, werden nicht kopiert.

14. Wählen Sie **OK**, um TDS-Komponenten für die andere TDS-Komponentengruppe auf der Seite **Quellensteuerkomponenten** zu kopieren und die erstellen.

    [![Dialogfeld „Quellensteuerkomponenten kopieren“.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Schließen Sie die Seite.
