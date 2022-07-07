---
title: Nummernkreise für Einzelhandelsaufstellungen einrichten
description: In diesem Artikel wird beschrieben, wie Sie die Nummernkreise konfigurieren, die für Einzelhandelsaufstellungen in Microsoft Dynamics 365 Commerce erforderlich sind.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027185"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Nummernkreise für Einzelhandelsaufstellungen einrichten

[!include [banner](includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie die Nummernkreise konfigurieren, die für Einzelhandelsaufstellungen in Microsoft Dynamics 365 Commerce erforderlich sind.

In Dynamics 365 Commerce werden zwei Typen von Einzelhandelsaufstellungen verwendet: 

- **Transaktionsaufstellungen** sollen mit hoher Frequenz erstellt und gebucht werden. Sie werden verwendet, um alle nicht finanziellen Transaktionen im Store zur Dynamics 365 Commerce-Zentralverwaltung zu buchen. 
- **Finanzaufstellungen** sollen einmal pro Geschäftstag erstellt und gebucht werden. Sie enthalten nur geschlossene Schichten aus den Einzelhandelsgeschäften, die über den P-Einzelvorgang in die Commerce-Zentralverwaltung hochgeladen wurden.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Nummernkreis für Auszugsbuchung konfigurieren

Nachdem Sie die Einrichtung eines Einzelhandelsgeschäfts abgeschlossen haben, müssen Sie in der Commerce-Zentralverwaltung einen eindeutigen Nummernkreis konfigurieren, der während der Auszugserstellung für Auszüge verwendet wird.

Führen Sie die folgenden Schritte aus, um einen Nummernkreis für die Auszugsbuchung in der Commerce-Zentralverwaltung zu konfigurieren.

1. Gehen Sie zu **Organisationsverwaltung \> Nummernkreis \> Nummernkreise**.
1. Wählen Sie **Neu \> Nummernkreis**, um einen neuen Datensatz zu erstellen.
1. Geben Sie im Inforegister **Kennung** im Feld **Nummernkreiscode** einen Nummernkreiscode ein.
1. Geben Sie im Feld **Name des Nummernkreises** einen Namen ein.
1. Wählen Sie im Inforegister **Bereichsparameter** im Feld **Bereich** **Organisationseinheit** aus.
1. Wählen Sie im Feld **Organisationseinheit** den Store aus, für den der Nummernkreis verwendet werden soll.
1. Definieren Sie die Segmente im Inforegister **Segmente**.
1. Legen Sie im Inforegister **Referenzen** das Feld **Bereich** auf **Einzelhandelsgeschäft** fest.
1. Stellen Sie das Feld **Referenz** auf **Auszugsnummer** und wählen Sie dann **OK**.

    ![Inforegister „Kennung“, „Bereichsparameter“, „Segmente“ und „Referenzen“ auf der Seite „Nummernkreise“.](media/retail-statements-num-seq-setup-01.png)

1. Aktualisieren Sie im Inforegister **Allgemein** im Abschnitt **Nummernzuordnung** die Felder **Kleinste** und **Größte** so, dass sie der Länge des Segments **Alphanumerisch** entsprechen, das Sie im Inforegister **Segmente** definiert haben.
1. Im Inforegister **Leistung** empfehlen wir Ihnen, die Option **Vorabzuordnung** auf **Ja** und das Feld **Anzahl Nummern** auf **25** festzulegen.

    ![Inforegister „Allgemein“ und „Leistung“ auf der Seite „Nummernkreise“.](media/retail-statements-num-seq-setup-02.png)

1. Wählen Sie im Aktivitätsbereich **Speichern** aus, um Ihre Änderungen zu speichern, und schließen Sie die Seite.
