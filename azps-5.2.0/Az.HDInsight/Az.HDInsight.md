---
Module Name: Az.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Az.HDInsight.md
ms.openlocfilehash: e3c3bb9d4d8225823ec84750c8292288ce25c15b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415800"
---
# AZ. HDInsight-modul
## Problembeskrivning
Avsnitten i det här avsnittet innehåller Azure PowerShell-cmdlets för Microsoft Azure HDInsight i ramverket Azure Resource Manager (ARM). Dessa cmdletar används för att hantera HDInsight-kluster och de jobb som körs på dem. Det finns cmdlets i Microsoft. Azure. commands. HDInsight-namn området.

## Cmdlets för AZ. HDInsight
### [Add-AzHDInsightClusterIdentity](Add-AzHDInsightClusterIdentity.md)
Lägger till en kluster identitet till ett kluster konfigurations objekt.

### [Add-AzHDInsightComponentVersion](Add-AzHDInsightComponentVersion.md)
Lägger till en version för en tjänst som körs i ett kluster till ett kluster konfigurations objekt.

### [Add-AzHDInsightConfigValue](Add-AzHDInsightConfigValue.md)
Lägger till ett konfigurations värde för Hadoop-konfigurering och/eller en struktur för ett kluster konfigurations objekt.

### [Add-AzHDInsightMetastore](Add-AzHDInsightMetastore.md)
Lägger till en SQL-databas som ska fungera som en registrerings-eller Oozie-metastore till ett kluster konfigurations objekt.

### [Add-AzHDInsightScriptAction](Add-AzHDInsightScriptAction.md)
Lägger till en skript åtgärd i ett kluster konfigurations objekt.

### [Add-AzHDInsightSecurityProfile](Add-AzHDInsightSecurityProfile.md)
Lägger till en säkerhets profil till ett kluster konfigurations objekt.

### [Add-AzHDInsightStorage](Add-AzHDInsightStorage.md)
Lägger till en Azure-lagringsenhet till ett kluster konfigurations objekt.

### [Disable-AzHDInsightMonitoring](Disable-AzHDInsightMonitoring.md)
Inaktiverar övervakning i ett HDInsight-kluster och relevanta loggar slutar att flöda till arbets ytan övervakning som anges under aktivera.

### [Enable-AzHDInsightMonitoring](Enable-AzHDInsightMonitoring.md)
Aktiverar övervakning i ett HDInsight-kluster och relevanta loggar skickas till övervaknings arbets ytan som anges vid aktivering.

### [Get-AzHDInsightCluster](Get-AzHDInsightCluster.md)
Hämtar och visar alla Azure HDInsight-kluster som är kopplade till det aktuella abonnemanget eller en angiven resurs grupp, eller hämtar ett specifikt kluster.

### [Get-AzHDInsightClusterAutoscaleConfiguration](Get-AzHDInsightClusterAutoscaleConfiguration.md)
Hämtar autoskalan för HDInsight-klustret.

### [Get-AzHDInsightHost](Get-AzHDInsightHost.md)
Visar värderna för HDInsight-klustret.

### [Get-AzHDInsightJob](Get-AzHDInsightJob.md)
Hämtar listan med jobb från ett kluster och visar dem i omvänd kronologisk ordning, eller hämtar ett specifikt jobb.

### [Get-AzHDInsightJobOutput](Get-AzHDInsightJobOutput.md)
Hämtar loggens utdata för ett jobb från det lagrings konto som är kopplat till ett angivet kluster.

### [Get-AzHDInsightMonitoring](Get-AzHDInsightMonitoring.md)
Hämtar status för övervakning av installationen i klustret.

### [Get-AzHDInsightPersistedScriptAction](Get-AzHDInsightPersistedScriptAction.md)
Hämtar de beständiga skript åtgärderna för ett kluster och visar dem i kronologisk ordning, eller hämtar information om en viss beständiga skript åtgärd.

### [Get-AzHDInsightProperty](Get-AzHDInsightProperty.md)
Hämtar egenskaper för HDInsight-tjänsten, till exempel tillgängliga platser och kapacitet.

### [Get-AzHDInsightScriptActionHistory](Get-AzHDInsightScriptActionHistory.md)
Hämtar skript åtgärds historiken för ett kluster och visar den i omvänd kronologisk ordning, eller hämtar information om en tidigare körd skript åtgärd.

### [Invoke-AzHDInsightHiveJob](Invoke-AzHDInsightHiveJob.md)
Skickar en struktur fråga till ett HDInsight-kluster och hämtar frågeresultat i en åtgärd.

### [New-AzHDInsightCluster](New-AzHDInsightCluster.md)
Skapar ett Azure HDInsight-kluster i den angivna resurs gruppen för det aktuella abonnemanget.

### [New-AzHDInsightClusterAutoscaleConfiguration](New-AzHDInsightClusterAutoscaleConfiguration.md)
Skapar ett icke bevarat objekt som beskriver autoskalans konfiguration för ett Azure HDInsight-kluster.

### [New-AzHDInsightClusterAutoscaleScheduleCondition](New-AzHDInsightClusterAutoscaleScheduleCondition.md)
Skapar ett schema baserat autoskalning.

### [New-AzHDInsightClusterConfig](New-AzHDInsightClusterConfig.md)
Skapar ett icke beständigt kluster konfigurations objekt som beskriver en Azure HDInsight-kluster konfiguration.

### [New-AzHDInsightHiveJobDefinition](New-AzHDInsightHiveJobDefinition.md)
Skapar ett Hive Job-objekt.

### [New-AzHDInsightMapReduceJobDefinition](New-AzHDInsightMapReduceJobDefinition.md)
Skapar ett MapReduce.

### [New-AzHDInsightPigJobDefinition](New-AzHDInsightPigJobDefinition.md)
Skapar ett gris-Job-objekt.

### [New-AzHDInsightSqoopJobDefinition](New-AzHDInsightSqoopJobDefinition.md)
Skapar ett Sqoop.

### [New-AzHDInsightStreamingMapReduceJobDefinition](New-AzHDInsightStreamingMapReduceJobDefinition.md)
Skapar ett Job-MapReduce.

### [Remove-AzHDInsightCluster](Remove-AzHDInsightCluster.md)
Tar bort angivet HDInsight-kluster från aktuell prenumeration.

### [Remove-AzHDInsightClusterAutoscaleConfiguration](Remove-AzHDInsightClusterAutoscaleConfiguration.md)
Tar bort autoskalan för HDInsight-klustret.

### [Remove-AzHDInsightPersistedScriptAction](Remove-AzHDInsightPersistedScriptAction.md)
Tar bort en beständiga skript åtgärd från ett HDInsight-kluster.

### [Restart-AzHDInsightHost](Restart-AzHDInsightHost.md)
Startar om de specifika värderna för HDInsight-klustret.

### [Set-AzHDInsightClusterAutoscaleConfiguration](Set-AzHDInsightClusterAutoscaleConfiguration.md)
Ställer in automatisk skalnings konfiguration för ett Azure HDInsight-kluster.

### [Set-AzHDInsightClusterDiskEncryptionKey](Set-AzHDInsightClusterDiskEncryptionKey.md)
Roterar disk krypterings tangenten för det angivna HDInsight-klustret.

### [Set-AzHDInsightClusterSize](Set-AzHDInsightClusterSize.md)
Anger antalet arbets tagare i ett angivet kluster.

### [Set-AzHDInsightDefaultStorage](Set-AzHDInsightDefaultStorage.md)
Anger standardinställning för lagrings konto i ett kluster konfigurations objekt.

### [Set-AzHDInsightGatewayCredential](Set-AzHDInsightGatewayCredential.md)
Anger HTTP-autentiseringsuppgifter för gateway för ett Azure HDInsight-kluster.

### [Set-AzHDInsightPersistedScriptAction](Set-AzHDInsightPersistedScriptAction.md)
Anger att en tidigare körd skript åtgärd ska vara en bestående skript åtgärd.

### [Start-AzHDInsightJob](Start-AzHDInsightJob.md)
Startar ett definierat Azure HDInsight-jobb i ett angivet kluster.

### [Stopp-AzHDInsightJob](Stop-AzHDInsightJob.md)
Stoppar ett angivet pågående jobb i ett kluster.

### [Skicka-AzHDInsightScriptAction](Submit-AzHDInsightScriptAction.md)
Skickar en ny skript åtgärd till ett Azure HDInsight-kluster.

### [Use-AzHDInsightCluster](Use-AzHDInsightCluster.md)
Väljer ett kluster som ska användas med Invoke-RmAzureHDInsightHiveJob cmdlet.

### [Wait-AzHDInsightJob](Wait-AzHDInsightJob.md)
Väntar på att ett visst jobb ska slutföras eller misslyckande.

