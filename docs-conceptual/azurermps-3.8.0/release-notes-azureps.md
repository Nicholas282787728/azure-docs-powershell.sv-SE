---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 04f89e8d47d0825d46cb1b8817efbcc0cafa0acd
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

## <a name="version-380"></a>Version 3.8.0
* Compute
  - Fel i Get-*-cmdletar har åtgärdats så att det går att hämta flera sidor med data (mer än 120 objekt)
* DataLakeAnalytics
  - Hjälpen för vissa kommandon har åtgärdats så att den innehåller rätt ord och exempel.
* DataLakeStore
  - Tillagt stöd för start och slut för `Get-AzureRMDataLakeStoreItemContent`-cmdleten. Detta gör att de översta N eller sista N nya radavgränsade raderna visas.
* HDInsight
  - Stöd för RServer-klustertypen har lagts till
    + Edgenode VM-storlek kan anges för RServer-kluster i New-AzureRmHDInsightCluster eller New-AzureRmHDInsightClusterConfig
    + RServer är nu ett konfigurationsalternativ i Add-AzureRmHDInsightConfigValues. Det gör att RStudio-flaggan kan anges för att indikera att R Studio måste installeras.
* LogicApp
  - Cmdletarna Set-AzureRmIntegrationAccountSchema och Set-AzureRmIntegrationAccountMap har åtgärdats angående ett contentlink-problem (både content och contentlink angavs vilket resulterade i ett uppdateringsfel).
* Nätverk
  - Stöd för nya funktioner för brandvägg för webbaserade program har lagts till i Application Gateways
    + New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig har lagts till
    + Get-AzureRmApplicationGatewayAvailableWafRuleSets har lagts till (alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)
    + New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration har uppdaterats: Parametrarna -RuleSetType, -RuleSetVersion och -DisabledRuleGroups har lagts till
    + Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration har uppdaterats: Parametrarna -RuleSetType, -RuleSetVersion och -DisabledRuleGroups har lagts till
  - Stöd för IPSec-principer har lagts till i gatewayanslutningar för virtuella nätverk
  - New-AzureRmIpsecPolicy har lagts till
  - New-AzureRmVirtualNetworkGatewayConnection har uppdaterats: Parametrarna -IpsecPolicies och -UsePolicyBasedTrafficSelectors har lagts till
* Profil
  - *Föråldrad*: Save-AzureRmProfile har bytt namn till Save-AzureRmContext. Det finns ett alias till det gamla cmdletnamnet och det kommer att tas bort i nästa version.
  - *Föråldrad*: Select-AzureRmProfile har bytt namn till Import-AzureRmContext. Det finns ett alias till det gamla cmdletnamnet och det kommer att tas bort i nästa version.
  - Utdatatyperna PSAzureContext och PSAzureProfile för profil-cmdletar kommer att ändras i nästa version.
  - Cmdleten Save-AzureRmContext kommer inte att ha någon OutputType i nästa version.
  - Ett fel har åtgärdats i en gemensam cmdlet-kod för att använda en FIPS-kompatibel algoritm för datahashvärden: https://github.com/Azure/azure-powershell/issues/3651
* SQL
  - Fel har åtgärdats för cmdletar för Azure-redundansgrupper
  - Korrigering för åtgärdsavsökning
  - GracePeriodWithDataLossHour-värdet har åtgärdats när Manuell anges för FailoverPolicy
* TrafficManager
  - Stöd för trafikroutningsmetoden Geographic
    + Nytt värde (Geographic) för parametern TrafficRoutingMethod i New-AzureRmTrafficManagerProfile
    + Ny parameter (GeoMapping) för New-AzureRmTrafficManagerEndpoint och Add-AzureRmTrafficManagerEndpointConfig
    + Omdirigering har åtgärdats för Get-AzureRmTrafficManagerProfile när den returnerar en samling profiler
* ServiceManagement
  - Restart-AzureVM: Parametern InitiateMaintenance har lagts till för att utföra underhåll under omstart av virtuella datorer.
  - Get-AzureVM: Fält för underhållsstatus har lagts till.
  - Nya cmdletar har lagts till för uppgradering av Recovery Services-valv
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
