---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421328"
---
# <span data-ttu-id="9af11-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="9af11-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="9af11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9af11-102">SYNOPSIS</span></span>
<span data-ttu-id="9af11-103">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="9af11-103">Gets information about a server.</span></span>

## <span data-ttu-id="9af11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9af11-104">SYNTAX</span></span>

### <span data-ttu-id="9af11-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="9af11-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9af11-106">Lära</span><span class="sxs-lookup"><span data-stu-id="9af11-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9af11-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9af11-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9af11-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="9af11-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9af11-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9af11-109">DESCRIPTION</span></span>
<span data-ttu-id="9af11-110">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="9af11-110">Gets information about a server.</span></span>

## <span data-ttu-id="9af11-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9af11-111">EXAMPLES</span></span>

### <span data-ttu-id="9af11-112">Exempel 1: skaffa PostgreSql-server med standard kontext</span><span class="sxs-lookup"><span data-stu-id="9af11-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9af11-113">Denna cmdlet får PostgreSql server med standard kontext.</span><span class="sxs-lookup"><span data-stu-id="9af11-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="9af11-114">Exempel 2: skaffa PostgreSql Server efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="9af11-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9af11-115">Denna cmdlet får PostgreSql Server genom resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="9af11-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="9af11-116">Exempel 3: listar alla PostgreSql-servrar i angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="9af11-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9af11-117">Denna cmdlet visar alla PostgreSql-servrar i angiven resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9af11-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="9af11-118">Exempel 4: skaffa PostgreSql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="9af11-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="9af11-119">Med denna cmdlet-lista får du PostgreSql Server.</span><span class="sxs-lookup"><span data-stu-id="9af11-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="9af11-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9af11-120">PARAMETERS</span></span>

### <span data-ttu-id="9af11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af11-121">-DefaultProfile</span></span>
<span data-ttu-id="9af11-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9af11-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af11-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9af11-123">-InputObject</span></span>
<span data-ttu-id="9af11-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9af11-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9af11-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="9af11-125">-Name</span></span>
<span data-ttu-id="9af11-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="9af11-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af11-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af11-127">-ResourceGroupName</span></span>
<span data-ttu-id="9af11-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9af11-128">The name of the resource group.</span></span>
<span data-ttu-id="9af11-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9af11-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9af11-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9af11-130">-SubscriptionId</span></span>
<span data-ttu-id="9af11-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9af11-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af11-132">CommonParameters</span></span>
<span data-ttu-id="9af11-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af11-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9af11-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af11-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9af11-135">INPUTS</span></span>

### <span data-ttu-id="9af11-136">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9af11-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9af11-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9af11-137">OUTPUTS</span></span>

### <span data-ttu-id="9af11-138">Microsoft. Azure. PowerShell. cmdletar. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="9af11-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="9af11-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9af11-139">NOTES</span></span>

<span data-ttu-id="9af11-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9af11-140">ALIASES</span></span>

<span data-ttu-id="9af11-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="9af11-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9af11-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="9af11-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9af11-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9af11-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9af11-144">INPUTOBJECT <IPostgreSqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="9af11-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9af11-145">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="9af11-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9af11-146">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="9af11-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9af11-147">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="9af11-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9af11-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="9af11-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9af11-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="9af11-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9af11-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9af11-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9af11-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="9af11-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="9af11-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="9af11-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9af11-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="9af11-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9af11-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="9af11-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9af11-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="9af11-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9af11-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9af11-156">RELATED LINKS</span></span>

