---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410192"
---
# <span data-ttu-id="09123-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="09123-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="09123-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09123-102">SYNOPSIS</span></span>
<span data-ttu-id="09123-103">Hämtar information om en databas.</span><span class="sxs-lookup"><span data-stu-id="09123-103">Gets information about a database.</span></span>

## <span data-ttu-id="09123-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09123-104">SYNTAX</span></span>

### <span data-ttu-id="09123-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="09123-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09123-106">Lära</span><span class="sxs-lookup"><span data-stu-id="09123-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="09123-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="09123-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="09123-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09123-108">DESCRIPTION</span></span>
<span data-ttu-id="09123-109">Hämtar information om en databas.</span><span class="sxs-lookup"><span data-stu-id="09123-109">Gets information about a database.</span></span>

## <span data-ttu-id="09123-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09123-110">EXAMPLES</span></span>

### <span data-ttu-id="09123-111">Exempel 1: skaffa en MySql-databas per resurs namn</span><span class="sxs-lookup"><span data-stu-id="09123-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="09123-112">Denna cmdlet hämtar MySql-servern efter resurs namn.</span><span class="sxs-lookup"><span data-stu-id="09123-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="09123-113">Exempel 2: skaffa MySql-databaser med identitet</span><span class="sxs-lookup"><span data-stu-id="09123-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="09123-114">Med den här cmdleten får du en MySql-server med identitet.</span><span class="sxs-lookup"><span data-stu-id="09123-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="09123-115">Exempel 3: listar alla MySql-databaser på den angivna servern</span><span class="sxs-lookup"><span data-stu-id="09123-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="09123-116">Denna cmdlet listar alla MySql-servrar i angiven server.</span><span class="sxs-lookup"><span data-stu-id="09123-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="09123-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09123-117">PARAMETERS</span></span>

### <span data-ttu-id="09123-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09123-118">-DefaultProfile</span></span>
<span data-ttu-id="09123-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09123-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09123-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09123-120">-InputObject</span></span>
<span data-ttu-id="09123-121">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="09123-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="09123-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="09123-122">-Name</span></span>
<span data-ttu-id="09123-123">Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="09123-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09123-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09123-124">-ResourceGroupName</span></span>
<span data-ttu-id="09123-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="09123-125">The name of the resource group.</span></span>
<span data-ttu-id="09123-126">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="09123-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="09123-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="09123-127">-ServerName</span></span>
<span data-ttu-id="09123-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="09123-128">The name of the server.</span></span>

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

### <span data-ttu-id="09123-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09123-129">-SubscriptionId</span></span>
<span data-ttu-id="09123-130">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="09123-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="09123-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09123-131">CommonParameters</span></span>
<span data-ttu-id="09123-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09123-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09123-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09123-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09123-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09123-134">INPUTS</span></span>

### <span data-ttu-id="09123-135">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="09123-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="09123-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09123-136">OUTPUTS</span></span>

### <span data-ttu-id="09123-137">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="09123-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="09123-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09123-138">NOTES</span></span>

<span data-ttu-id="09123-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="09123-139">ALIASES</span></span>

<span data-ttu-id="09123-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="09123-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09123-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="09123-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09123-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09123-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09123-143">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="09123-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09123-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="09123-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="09123-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="09123-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="09123-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="09123-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="09123-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="09123-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09123-148">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="09123-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="09123-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="09123-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="09123-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="09123-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09123-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="09123-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="09123-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="09123-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="09123-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="09123-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="09123-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="09123-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09123-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="09123-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="09123-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09123-156">RELATED LINKS</span></span>

