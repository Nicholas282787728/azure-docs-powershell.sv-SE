---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260653"
---
# <span data-ttu-id="81675-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="81675-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="81675-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81675-102">SYNOPSIS</span></span>
<span data-ttu-id="81675-103">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81675-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="81675-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81675-104">SYNTAX</span></span>

### <span data-ttu-id="81675-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="81675-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81675-106">Lära</span><span class="sxs-lookup"><span data-stu-id="81675-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="81675-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="81675-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="81675-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81675-108">DESCRIPTION</span></span>
<span data-ttu-id="81675-109">Hämtar information om en Server konfiguration.</span><span class="sxs-lookup"><span data-stu-id="81675-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="81675-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81675-110">EXAMPLES</span></span>

### <span data-ttu-id="81675-111">Exempel 1: lista alla konfigurationer i PostgreSql Server</span><span class="sxs-lookup"><span data-stu-id="81675-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="81675-112">Denna cmdlet visar alla konfigurationer i angiven PostgreSql-Server.</span><span class="sxs-lookup"><span data-stu-id="81675-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="81675-113">Exempel 2: Hämta angiven PostgreSql-konfiguration efter namn</span><span class="sxs-lookup"><span data-stu-id="81675-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="81675-114">Denna cmdlet anger PostgreSql-konfigurationen efter namn.</span><span class="sxs-lookup"><span data-stu-id="81675-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="81675-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81675-115">PARAMETERS</span></span>

### <span data-ttu-id="81675-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81675-116">-DefaultProfile</span></span>
<span data-ttu-id="81675-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81675-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81675-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81675-118">-InputObject</span></span>
<span data-ttu-id="81675-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="81675-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81675-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="81675-120">-Name</span></span>
<span data-ttu-id="81675-121">Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="81675-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="81675-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81675-122">-ResourceGroupName</span></span>
<span data-ttu-id="81675-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81675-123">The name of the resource group.</span></span>
<span data-ttu-id="81675-124">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="81675-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="81675-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81675-125">-ServerName</span></span>
<span data-ttu-id="81675-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="81675-126">The name of the server.</span></span>

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

### <span data-ttu-id="81675-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81675-127">-SubscriptionId</span></span>
<span data-ttu-id="81675-128">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="81675-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="81675-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81675-129">CommonParameters</span></span>
<span data-ttu-id="81675-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81675-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81675-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81675-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81675-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81675-132">INPUTS</span></span>

### <span data-ttu-id="81675-133">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="81675-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="81675-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81675-134">OUTPUTS</span></span>

### <span data-ttu-id="81675-135">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="81675-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="81675-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81675-136">NOTES</span></span>

<span data-ttu-id="81675-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="81675-137">ALIASES</span></span>

<span data-ttu-id="81675-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="81675-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81675-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="81675-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81675-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81675-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81675-141">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="81675-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81675-142">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="81675-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="81675-143">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="81675-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="81675-144">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="81675-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="81675-145">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="81675-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81675-146">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="81675-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="81675-147">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="81675-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="81675-148">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="81675-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="81675-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="81675-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="81675-150">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="81675-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="81675-151">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="81675-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="81675-152">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="81675-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="81675-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81675-153">RELATED LINKS</span></span>

