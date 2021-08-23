---
title: Migration vom Währungsdatentyp für duales Schreiben
description: In diesem Thema wird beschrieben, wie Sie die Anzahl der Dezimalstellen ändern, die duales Schreiben für die Währung unterstützt.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 1bfb719b20694db9af8a2a013786b8309c23c9d963c8746346930bbde96e9bbb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725135"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migration vom Währungsdatentyp für duales Schreiben

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Sie können die Anzahl der Dezimalstellen, die für Währungswerte unterstützt werden, auf maximal 10 erhöhen. Die Standardgrenze liegt bei vier Dezimalstellen. Indem Sie die Anzahl der Dezimalstellen erhöhen, können Sie Datenverluste vermeiden, wenn Sie zum Synchronisieren von dualem Schreiben verwenden. Die Erhöhung der Anzahl der Dezimalstellen ist eine Opt-In-Änderung. Um es zu implementieren, müssen Sie Unterstützung von Microsoft anfordern.

Das Ändern der Anzahl der Dezimalstellen erfolgt in zwei Schritten:

1. Fordern Sie die Migration von Microsoft an.
2. Ändern Sie die Anzahl der Dezimalstellen in Dataverse.

Die Finance and Operations App und Dataverse muss die gleiche Anzahl von Dezimalstellen in Währungswerten unterstützen. Andernfalls kann es zu Datenverlust kommen, wenn diese Informationen zwischen Apps synchronisiert werden. Der Migrationsprozess konfiguriert die Art und Weise neu, in der Währungs- und Wechselkurswerte gespeichert werden, ändert jedoch keine Daten. Nach Abschluss der Migration kann die Anzahl der Dezimalstellen für Währungscodes und Preise erhöht werden, und die Daten, die Benutzer eingeben und anzeigen, können dezimaler sein.

Die Migration ist optional. Wenn Sie möglicherweise mehr Dezimalstellen unterstützen, empfehlen wir Ihnen, die Migration in Betracht zu ziehen. Organisationen, die keine Werte mit mehr als vier Dezimalstellen benötigen, müssen nicht migrieren.

## <a name="requesting-migration-from-microsoft"></a>Fordern Sie die Migration von Microsoft an

Speicherung für vorhandene Währungsspalten in Dataverse kann nicht mehr als vier Dezimalstellen unterstützen. Daher werden während des Migrationsprozesses Währungswerte in neue interne Spalten in der Datenbank kopiert. Dieser Vorgang wird kontinuierlich ausgeführt, bis alle Daten migriert wurden. Intern ersetzen am Ende der Migration die neuen Speichertypen die alten Speichertypen, die Datenwerte bleiben jedoch unverändert. Die Währungsspalten können dann bis zu 10 Dezimalstellen unterstützen. Während des Migrationsprozesses kann Dataverse ohne Unterbrechung weiter verwendet werden.

Gleichzeitig werden die Wechselkurse so geändert, dass sie bis zu 12 Dezimalstellen anstelle der aktuellen Grenze von 10 unterstützen. Diese Änderung ist erforderlich, damit die Anzahl der Dezimalstellen in der Finance and Operations App und Dataverse gleich ist.

Die Migration ändert keine Daten. Nach der Konvertierung der Währungs- und Wechselkursspalten können Administratoren das System so konfigurieren, dass bis zu 10 Dezimalstellen für Währungsspalten verwendet werden, indem die Anzahl der Dezimalstellen für jede Transaktionswährung und die Preisgestaltung angegeben werden.

### <a name="request-a-migration"></a>Fordern Sie eine Migration an

Um diese Funktion verfügbar zu machen, senden Sie eine E-Mail **CDSExpandDecimal@microsoft.com** und schließen Sie die folgenden Informationen ein:

+ **Gegenstand:** Anforderung zur Aktivierung der erweiterten Dezimalunterstützung für \<organizationID\>
+ **Körper:** Ich möchte die erweiterte Dezimalunterstützung für meine Organisation \<organizationID\> aktivieren.

Ein Microsoft-Vertreter wird Sie innerhalb von zwei bis drei Werktagen für die nächsten Schritte kontaktieren.

Wenn Sie eine Migration anfordern, sollten Sie die folgenden Details kennen und entsprechend planen:

+ Die für die Migration der Daten erforderliche Zeit hängt von der Datenmenge im System ab. Die Migration großer Datenbanken kann mehrere Tage dauern.
+ Die Größe der Datenbank nimmt vorübergehend zu, während die Migration ausgeführt wird, da für Indizes zusätzlicher Speicherplatz benötigt wird. Der größte Teil des zusätzlichen Speicherplatzes wird freigegeben, wenn die Migration abgeschlossen ist.
+ Wenn während des Migrationsprozesses Fehler auftreten, die den Abschluss der Migration verhindern, gibt das System Warnungen an den Microsoft-Support aus, damit die Support-Mitarbeiter eingreifen können. Selbst wenn während der Migration Fehler auftreten, bleibt Dataverse für den regelmäßigen Gebrauch voll verfügbar.
+ Der Migrationsprozess ist nicht umkehrbar.

## <a name="changing-the-number-of-decimal-places"></a>Ändern Sie die Anzahl der Dezimalstellen

Nachdem die Migration abgeschlossen ist, kann Dataverse Zahlen mit mehr Dezimalstellen speichern. Administratoren können auswählen, wie viele Dezimalstellen für bestimmte Währungscodes und für die Preisgestaltung verwendet werden. Benutzer von Microsoft Power Apps, Power BI und Power Automate können dann Zahlen mit mehr Dezimalstellen anzeigen und verwenden.

Um diese Änderung vorzunehmen, müssen Sie die folgenden Einstellungen in Power Apps aktualisieren:

+ **Systemeinstellungen: Währungsgenauigkeit für die Preisgestaltung** – Die Spalte **Legen Sie die Währungsgenauigkeit fest, die für die Preisgestaltung im gesamten System verwendet wird** definiert, wie sich die Währung für die Organisation verhält, wenn **Preisgenauigkeit** ausgewählt ist.
+ **Geschäftsführung: Währungen** – In der Spalte **Währungspräzision** können Sie eine benutzerdefinierte Anzahl von Dezimalstellen für eine bestimmte Währung angeben. Es gibt einen Fallback für die organisationsweite Einstellung.

Im Folgenden finden Sie einige Beschränkungen:

+ Sie können die Währungsspalte in einer Tabelle nicht konfigurieren.
+ Sie können mehr als vier Dezimalstellen auf den Ebenen **Preisgestaltung** und **Transaktionswährung** angeben.

### <a name="system-settings-currency-precision-for-pricing"></a>Systemeinstellungen: Währungsgenauigkeit für die Preisgestaltung

Nach Abschluss der Migration können Administratoren die Währungsgenauigkeit festlegen. Gehen Sie zu **Einstellungen \> Verwaltung** und wählen Sie **Systemeinstellungen**. Dann auf der Registerkarte **Allgemein** ändern Sie den Wert der Spalte **Legen Sie die Währungsgenauigkeit fest, die für die Preisgestaltung im gesamten System verwendet wird** wie in der folgenden Abbildung gezeigt.

![Systemeinstellungen für Währung.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Geschäftsdokumentverwaltung: Währungen

Wenn Sie verlangen, dass die Währungsgenauigkeit für eine bestimmte Währung von der Währungsgenauigkeit abweicht, die für die Preisgestaltung verwendet wird, können Sie sie ändern. Gehen Sie zu **Einstellungen \> Geschäftsführung**, wählen **Währungen** und wählen die zu ändernde Währung aus. Dann stellen Sie die Spalte **Währungspräzision** auf die Anzahl der gewünschten Dezimalstellen ein, wie in der folgenden Abbildung gezeigt.

![Währungseinstellungen für ein bestimmtes Gebietsschema.](media/specific-currency.png)

### <a name="tables-currency-column"></a>Tabellen: Währungsspalte

Die Anzahl der Dezimalstellen, die für bestimmte Währungsspalten konfiguriert werden können, ist auf vier begrenzt.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]