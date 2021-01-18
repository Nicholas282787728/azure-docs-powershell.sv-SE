---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521072"
---
# <span data-ttu-id="a02e9-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a02e9-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="a02e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a02e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a02e9-103">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a02e9-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a02e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a02e9-104">SYNTAX</span></span>

### <span data-ttu-id="a02e9-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a02e9-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a02e9-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a02e9-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a02e9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a02e9-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a02e9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a02e9-108">DESCRIPTION</span></span>
<span data-ttu-id="a02e9-109">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a02e9-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="a02e9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a02e9-110">EXAMPLES</span></span>

### <span data-ttu-id="a02e9-111">Exempel 1: lista alla konfigurationer i angiven MySql-Server</span><span class="sxs-lookup"><span data-stu-id="a02e9-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a02e9-112">Denna cmdlet visar alla konfigurationer i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="a02e9-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="a02e9-113">Exempel 2: Hämta angiven MySql-konfiguration efter namn</span><span class="sxs-lookup"><span data-stu-id="a02e9-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a02e9-114">Denna cmdlet anger MySql-konfiguration efter namn.</span><span class="sxs-lookup"><span data-stu-id="a02e9-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="a02e9-115">Exempel 3: lista konfiguration efter identitet</span><span class="sxs-lookup"><span data-stu-id="a02e9-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="a02e9-116">Denna cmdlet konfigurerar MySql-konfigurationen efter identitet.</span><span class="sxs-lookup"><span data-stu-id="a02e9-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="a02e9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a02e9-117">PARAMETERS</span></span>

### <span data-ttu-id="a02e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a02e9-118">-DefaultProfile</span></span>
<span data-ttu-id="a02e9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a02e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a02e9-120">-InputObject</span></span>
<span data-ttu-id="a02e9-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a02e9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="a02e9-122">-Name</span></span>
<span data-ttu-id="a02e9-123">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="a02e9-123">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a02e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a02e9-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-125">The name of the resource group.</span></span>
<span data-ttu-id="a02e9-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a02e9-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a02e9-127">-ServerName</span></span>
<span data-ttu-id="a02e9-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a02e9-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a02e9-129">-SubscriptionId</span></span>
<span data-ttu-id="a02e9-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a02e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a02e9-131">CommonParameters</span></span>
<span data-ttu-id="a02e9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a02e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a02e9-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a02e9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a02e9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a02e9-134">INPUTS</span></span>

### <span data-ttu-id="a02e9-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a02e9-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="a02e9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a02e9-136">OUTPUTS</span></span>

### <span data-ttu-id="a02e9-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a02e9-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="a02e9-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a02e9-138">NOTES</span></span>

<span data-ttu-id="a02e9-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a02e9-139">ALIASES</span></span>

<span data-ttu-id="a02e9-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a02e9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a02e9-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a02e9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a02e9-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a02e9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a02e9-143">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a02e9-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a02e9-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="a02e9-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a02e9-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a02e9-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="a02e9-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a02e9-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a02e9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a02e9-148">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="a02e9-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="a02e9-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a02e9-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a02e9-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="a02e9-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="a02e9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="a02e9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a02e9-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a02e9-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a02e9-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="a02e9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a02e9-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="a02e9-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a02e9-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a02e9-156">RELATED LINKS</span></span>

