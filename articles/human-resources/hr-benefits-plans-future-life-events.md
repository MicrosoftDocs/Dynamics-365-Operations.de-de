---
title: Zukünftige Lebensereignisse konfigurieren
description: Dieser Artikel beschreibt, wie Sie zukünftige Lebensereignisse in Dynamics 365 Human Resources planen.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2cb3ca03e0d9d7e5423a405f1eb0372e1c19588d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227984"
---
# <a name="configure-future-life-events"></a>Zukünftige Lebensereignisse konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [banner](../includes/preview-banner.md)]

Sie können in Dynamics 365 Human Resources zukünftige Lebensereignisse planen.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Zukünftige Lebensereignisse**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | Datum des Lebensereignisses | Das System verarbeitet alle Ereignisse während der Registrierungsperiode, die bis zu diesem Datum auftreten. |
   | Lebensereignis protokolliert | Datum und Uhrzeit, zu denen das Lebensereignis protokolliert wird. |
   | Protokolltyp | Zeigt an, ob die Aktivität einem der folgenden Werte entspricht:</br></br>- **Aktualisieren** – Änderung an einem vorhandenen Datensatz, in dem Lebensereignisse aufgezeichnet werden</br></br>- **Einfügen** – Erstellung eines neuen Lebensereignisdatensatzes |
   | Kennung des Lebensereignistyps | Der eindeutige Bezeichner für den Lebensereignistyp. |
   | Lebensereignistyp | Ein Katalysator für die Aktualisierung der Vorteilsregistrierung eines Mitarbeiters. Weitere Informationen finden Sie im Abschnitt „Auslöser für Lebensereignisse“. |
   | Status | Gibt an, ob das Lebensereignis verarbeitet wurde. |
   | Position | Die Positionsnummer des zukünftigen Lebensereignisses. |

4. Wählen Sie **Speichern** aus. 

Sie können zukünftige Lebensereignisse löschen. Wenn ein verarbeitetes zukünftiges Lebensereignis gelöscht wird, wird auch der zukünftige Datensatz gelöscht. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
