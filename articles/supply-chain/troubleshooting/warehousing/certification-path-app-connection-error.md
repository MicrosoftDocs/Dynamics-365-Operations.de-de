---
title: Zertifizierungspfadfehler beim Einrichten der App-Verbindung
description: Wenn die Warehouse Management-App den Fehler „Vertrauensanker für Zertifizierungspfad nicht gefunden“ anzeigt, verwenden Sie diese Seite, um das Problem zu beheben oder zu umgehen.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476447"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Der Vertrauensanker für den Zertifizierungspfad wurde beim Einrichten der App-Verbindung nicht gefunden.

## <a name="symptoms"></a>Symptome

Wenn Sie versuchen, eine Verbindung zu Supply Chain Management herzustellen, zeigt die Warehouse Management-App möglicherweise folgende Fehlermeldung an:

> java.security.cert.certPathValidatorException: Vertrauensanker für Zertifizierungspfad wurde nicht gefunden.

Dieses Problem kann Geräte mit den folgenden Eigenschaften betreffen:

- **Betriebssystemversion**: Android 4.4.x (wie z. B. Zebra TC55). Dies ist kein Problem in den letzten Android-Versionen.
- **Ort für Supply Chain Management**: Cloud
- **Verbindungsmodus**: geheimer Clientschlüssel oder Zertifikat

## <a name="possible-cause"></a>Mögliche Ursache

Microsoft hat möglicherweise die von Supply Chain Management verwendeten Server-SSL-Zertifikate aktualisiert. Infolgedessen kann sich das Stammzertifikat und/oder eines der Zwischenzertifikate geändert haben, sodass das neue Zertifikat nicht auf der Liste der vertrauenswürdigen Systemzertifikate für das mobile Gerät steht. Neuere Versionen von Android aktualisieren die Listen der vertrauenswürdigen Zertifikate automatisch, Android 4.4.x hingegen nicht.

## <a name="resolution"></a>Lösung

Führen Sie einen der folgenden Schritte aus, um dieses Problem zu beheben:

- Verwenden Sie die im nächsten Abschnitt beschriebene Problemumgehung, um jedes relevante Gerät zu aktualisieren.
- Es *könnte* möglich sein, sich an Zebra oder Google zu wenden, um aktualisierte Zertifikate von der Zertifizierungsstelle (CA) zu erhalten, der des Systems vertraut. Dies konnten wir jedoch nicht bestätigen.
- Ziehen Sie es nach Möglichkeit in Betracht, ältere Geräte durch solche zu ersetzen, auf denen eine neuere Version von Android ausgeführt wird (die vertrauenswürdige CA-Zertifikate automatisch aktualisiert).

### <a name="workaround"></a>Problemumgehung

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Schritt 1: Exportieren des neuen Stammzertifikats aus Supply Chain Management

Laden Sie das neue Stammzertifikat manuell über Ihren Internetbrowser herunter, indem Sie wie folgt vorgehen:

1. Melden Sie sich bei Dynamics Supply Chain Management an und öffnen Sie die Startseite.

1. Wählen Sie in der Adressleiste Ihres Browsers das Schlosssymbol aus, um das Dialogfeld **Verbindung ist sicher** anzuzeigen.
1. Wählen Sie im Dialogfeld die Option **Zertifikat (gültig)** aus, um das Fenster **Zertifikat** für dieses Zertifikat zu öffnen.
1. Öffnen Sie die Registerkarte **Zertifizierungspfad** im Fenster **Zertifikat**.
1. Wählen Sie das oberste Zertifikat in der Hierarchie aus. (Dies ist das Stammzertifikat.)
1. Öffnen Sie die Registerkarte **Details** im Fenster **Zertifikat**.
1. Wählen Sie die Schaltfläche **In Datei kopieren** unten auf der Registerkarte **Details** aus.
1. Der **Zertifikatexport-Assistent** wird geöffnet. Wählen Sie **Weiter** aus, um fortzufahren.
1. Die Seite **Dateiformat exportieren** wird geöffnet. Wählen Sie **DER-codiertes binäres X.509 (.CER)** aus. Wählen Sie anschließend **Weiter** aus, um fortzufahren.
1. Die Seite **Zu exportierende Dateien** wird geöffnet. Geben Sie einen Dateinamen und einen Speicherort an. Wählen Sie anschließend **Weiter** aus, um fortzufahren.
1. Die Seite **Zertifikatexport-Assistenten beenden** wird geöffnet und zeigt das Ergebnis Ihres Exports an. Wählen Sie **Fertig stellen** aus.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Schritt 2: Installieren des heruntergeladenen Zertifikats auf den betroffenen Geräten

Installieren Sie das heruntergeladene Zertifikat wie folgt:

1. Übertragen Sie das im vorherigen Schritt heruntergeladene Zertifikat auf das Gerät, das Sie aktualisieren möchten. Sie können beispielsweise eine SD-Karte oder eine Netzwerkverbindung verwenden, um die Datei auf Ihrem Gerät verfügbar zu machen.
1. Öffnen Sie die Sicherheitseinstellungen für Ihr Gerät und wählen Sie die Menüoption zum Installieren eines Zertifikats aus einer Datei aus. (Die genauen Schritte hierfür variieren je nach Gerät und Betriebssystemversion.)
1. Das neue Zertifikat sollte jetzt auf der Registerkarte **Benutzer** für vertrauenswürdige Zertifikate angezeigt werden.
1. Wiederholen Sie diese Schritte für alle betroffenen Geräte.
