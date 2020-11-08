---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: b92390969c4650d60d5c4a6954520fbbf3f26c71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262139"
---
# <span data-ttu-id="72e34-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e34-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="72e34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72e34-102">SYNOPSIS</span></span>
<span data-ttu-id="72e34-103">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="72e34-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="72e34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72e34-104">SYNTAX</span></span>

### <span data-ttu-id="72e34-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="72e34-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72e34-106">Lära</span><span class="sxs-lookup"><span data-stu-id="72e34-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72e34-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72e34-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72e34-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72e34-108">DESCRIPTION</span></span>
<span data-ttu-id="72e34-109">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="72e34-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="72e34-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72e34-110">EXAMPLES</span></span>

### <span data-ttu-id="72e34-111">Exempel 1: lista alla konfigurationer i angiven MySql-Server</span><span class="sxs-lookup"><span data-stu-id="72e34-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="72e34-112">Denna cmdlet visar alla konfigurationer i angiven MySql-Server.</span><span class="sxs-lookup"><span data-stu-id="72e34-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="72e34-113">Exempel 2: Hämta angiven MySql-konfiguration efter namn</span><span class="sxs-lookup"><span data-stu-id="72e34-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="72e34-114">Denna cmdlet anger MySql-konfiguration efter namn.</span><span class="sxs-lookup"><span data-stu-id="72e34-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="72e34-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72e34-115">PARAMETERS</span></span>

### <span data-ttu-id="72e34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e34-116">-DefaultProfile</span></span>
<span data-ttu-id="72e34-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72e34-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72e34-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72e34-118">-InputObject</span></span>
<span data-ttu-id="72e34-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="72e34-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="72e34-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="72e34-120">-Name</span></span>
<span data-ttu-id="72e34-121">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="72e34-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="72e34-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e34-122">-ResourceGroupName</span></span>
<span data-ttu-id="72e34-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72e34-123">The name of the resource group.</span></span>
<span data-ttu-id="72e34-124">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="72e34-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="72e34-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72e34-125">-ServerName</span></span>
<span data-ttu-id="72e34-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="72e34-126">The name of the server.</span></span>

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

### <span data-ttu-id="72e34-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72e34-127">-SubscriptionId</span></span>
<span data-ttu-id="72e34-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="72e34-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="72e34-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e34-129">CommonParameters</span></span>
<span data-ttu-id="72e34-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e34-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e34-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72e34-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e34-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72e34-132">INPUTS</span></span>

### <span data-ttu-id="72e34-133">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="72e34-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="72e34-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72e34-134">OUTPUTS</span></span>

### <span data-ttu-id="72e34-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e34-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="72e34-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72e34-136">NOTES</span></span>

<span data-ttu-id="72e34-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="72e34-137">ALIASES</span></span>

<span data-ttu-id="72e34-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="72e34-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72e34-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="72e34-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72e34-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72e34-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72e34-141">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="72e34-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72e34-142">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="72e34-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="72e34-143">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="72e34-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="72e34-144">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="72e34-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="72e34-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="72e34-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72e34-146">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="72e34-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="72e34-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="72e34-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="72e34-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="72e34-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="72e34-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="72e34-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="72e34-150">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="72e34-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="72e34-151">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="72e34-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="72e34-152">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="72e34-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="72e34-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72e34-153">RELATED LINKS</span></span>

