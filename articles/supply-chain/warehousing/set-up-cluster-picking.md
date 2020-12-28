---
title: Clusterkommissionierung einrichten
description: In diesem Thema wird beschrieben, wie die Clusterentnahme eingerichtet und wie Artikelbestätigung mit Clusterentnahme angewendet wird.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 009345e608c26887fedbe4a9c268367080593da2
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4429121"
---
# <a name="set-up-cluster-picking"></a>Clusterkommissionierung einrichten

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Arbeitskräften ermöglicht wird, ihre mobilen Geräte zu verwenden, um Entnahmearbeit in Cluster zu gruppieren, sodass sie Artikel von einem einzelnen Lagerplatz für mehrere Arbeitsaufträge gleichzeitig entnehmen können. Dies wird als *Clusterkommissionierung* bezeichnet.

## <a name="about-cluster-picking"></a>Zur Clusterkommissionierung

Nachdem Arbeitsaufträge für den Lagerort freigegeben sind, kann die Arbeitskraft ein mobiles Gerät verwenden, um die Aufträge einem Cluster zuzuweisen. Das Cluster organisiert die Entnahmerbeit für die Arbeitskraft. Wenn einem Cluster ein Arbeitsauftrag zugewiesen wird, muss die Arbeitskraft Clusterkommissionierung verwenden, um die Entnahmearbeit für den Auftrag auszuführen. Die Arbeitskraft kann anderen Entnahmemethoden nicht verwenden. Wenn einem Cluster ein Arbeitsauftrag versehentlich zugewiesen wird, muss die Arbeitskraft den Cluster unterbrechen und ihn anschließend neu erstellen.

Bei Bedarf kann eine Arbeitskraft einen Cluster an eine andere Arbeitskraft weiterleiten. Dieses ändert den Clusterstatus zu Erfolgreich. Wenn die Arbeitskraft ein mobiles Gerät verwendet, um anzugeben, dass die Entnahme und die Entnahmearbeit abgeschlossen ist, müssen die Lieferung oder die Ladung im Client bestätigt werden.

## <a name="enable-cluster-picking"></a>Clusterkommissionierung aktivieren

Um Clusterentnahme zu aktivieren, müssen Sie Folgendes einrichten:

- **Clusterprofile** - Geben Sie an, ob automatisch Clusterkennungen generiert werden, die Anzahl der zu verwendenden Positionen, wann Cluster abgebrochen werden und wie die Entnahmearbeit sequenziert und geprüft wird.

- **Arbeitsvorlagen** – Definieren Sie, wie die Entnahmearbeit für Clusterkommissionierung erstellt wird.

- **Standortweisungen** - Geben Sie an, von wo Artikel entnommen werden und wo sie eingelagert werden.

- **Mobile Geräte-Menüartikel** - Konfigurieren einer Menüoption des Mobilgeräts, um vorhandene Arbeit zu verwenden, die durch Clusterkommissionierung geleitet wird. Sie müssen die Menüoption einem Menü des mobilen Geräts hinzufügen, damit es auf mobilen Geräten angezeigt wird.

- **Lagerortverwaltungsparameter** - Geben Sie den Nummernkreis an, der verwendet wird, wenn Sie Kennungen für Cluster generieren möchten.

## <a name="set-up-a-cluster-profile"></a>Einrichten eines Clusterprofils

Gehen Sie zum Einrichten eines Clusterprofils folgendermaßen vor:

1. Klicken Sie auf **Lagerortverwaltung** \> **Einstellungen** \> **Mobiles Gerät** \> **Clusterprofile**.

1. Klicken Sie auf **Neu**, um ein neues Profil zu erstellen.

1. Klicken Sie **Erstellen Sie Cluster**, und unter **Clustersortieren**, klicken Sie **Neu**, um der Sortierkriterien für den Cluster einzurichten. Die Sortierkriterien steuern die Reihenfolge, in dem die Arbeitskraft die Entnahmearbeit ausführt. Sie können beliebig viele Kriterien hinzufügen.

1. Geben Sie im Feld **Sequenzzahl** die Anzahl ein, um die Reihenfolge zu definieren, in der die Sortierkriterien verarbeitet werden sollen.

1. Wählen Sie im Feld **Feldname** das Feld aus, das die Sortierung bestimmt. Wenn Sie beispielsweise das Feld **WMSLocationId** aktiviert haben, wird die Arbeit nach Lagerplatz sortiert.

1. Wählen Sie im Feld **Sortieren** eine der folgenden Optionen aus:

| **Option**     | **Beschreibung**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Aufsteigend**  | Die Entnahmearbeit wird in einer aufsteigenden Reihenfolge auf Basis der Sortierkriterien geordnet. Wenn Sie beispielsweise das Feld **WMSLocationId** als Sortierkriterium verwenden, und Ihre Lagerplatz Kennungen sind 1, 2, 3, 4, entnehmen Sie von Lagerplatz 4 zuerst. |
| **Absteigend** | Die Entnahmearbeit wird in einer absteigenden Reihenfolge auf Basis der Sortierkriterien geordnet. Wenn Sie beispielsweise das Feld **WMSLocationId** als Sortierkriterium verwenden, und Ihre Lagerplatz Kennungen sind 1, 2, 3, 4, entnehmen Sie von Lagerplatz 1 zuerst. |

## <a name="item-confirmation"></a>Artikelbestätigung

Wann die Clusterentnahme angewendet wird, ist die Artikelbestätigung wichtig, um die Artikel zu prüfen, die den Clustern hinzugefügt werden. Sie können Artikel in der Clusterentnahme während des Clusterentnahmevorgangs überprüfen. Die Einrichtung basiert auf dem Produktstrichcode-Einrichtung.

### <a name="set-up-item-verification-with-cluster-picking"></a>Einrichten der Artikelprüfung mit Clusterentnahme

1. Öffnen Sie über ein Menüelement des mobilen Geräts das Einstellungsformular für Arbeitsbestätigung: **Lagerortverwaltung** \> **Lagerortverwaltung** \> **Einstellungen** \> **Mobiles Gerät** \> **Menüelemente des mobilen Geräts**.

1. Öffnen Sie über das Menüelement des mobilen Geräts die Option **Einrichtung Arbeitsbestätigung**. Die **Produktbestätigung** ermöglicht Ihnen, beim Scannen jeden Inventurartikel über das mobile Gerät zu bestätigen.
