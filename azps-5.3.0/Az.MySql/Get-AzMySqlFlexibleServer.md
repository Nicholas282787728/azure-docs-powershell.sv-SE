---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: 10a3ca97d5f4bba9bf47eff5b2e4bdbb29b8ff24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522894"
---
# <span data-ttu-id="5cae1-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5cae1-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="5cae1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cae1-102">SYNOPSIS</span></span>
<span data-ttu-id="5cae1-103">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="5cae1-103">Gets information about a server.</span></span>

## <span data-ttu-id="5cae1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cae1-104">SYNTAX</span></span>

### <span data-ttu-id="5cae1-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="5cae1-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cae1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="5cae1-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cae1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cae1-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cae1-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="5cae1-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5cae1-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cae1-109">DESCRIPTION</span></span>
<span data-ttu-id="5cae1-110">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="5cae1-110">Gets information about a server.</span></span>

## <span data-ttu-id="5cae1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cae1-111">EXAMPLES</span></span>

### <span data-ttu-id="5cae1-112">Exempel 1: skaffa MySql server med standard kontext</span><span class="sxs-lookup"><span data-stu-id="5cae1-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5cae1-113">Denna cmdlet får MySql-servrar med standard kontext.</span><span class="sxs-lookup"><span data-stu-id="5cae1-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="5cae1-114">Exempel 2: skaffa MySql Server efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="5cae1-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5cae1-115">Denna cmdlet får MySql-servrar efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="5cae1-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="5cae1-116">Exempel 3: listar alla MySql-servrar i angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="5cae1-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5cae1-117">Denna cmdlet visar alla MySql-servrar i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="5cae1-118">Exempel 4: skaffa MySql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="5cae1-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5cae1-119">Denna cmdlet-lista får MySql-servrar efter identitet.</span><span class="sxs-lookup"><span data-stu-id="5cae1-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="5cae1-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cae1-120">PARAMETERS</span></span>

### <span data-ttu-id="5cae1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cae1-121">-DefaultProfile</span></span>
<span data-ttu-id="5cae1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cae1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cae1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cae1-123">-InputObject</span></span>
<span data-ttu-id="5cae1-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5cae1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cae1-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cae1-125">-Name</span></span>
<span data-ttu-id="5cae1-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5cae1-126">The name of the server.</span></span>

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

### <span data-ttu-id="5cae1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cae1-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cae1-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-128">The name of the resource group.</span></span>
<span data-ttu-id="5cae1-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5cae1-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5cae1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cae1-130">-SubscriptionId</span></span>
<span data-ttu-id="5cae1-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5cae1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cae1-132">CommonParameters</span></span>
<span data-ttu-id="5cae1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cae1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cae1-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cae1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cae1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cae1-135">INPUTS</span></span>

### <span data-ttu-id="5cae1-136">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5cae1-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5cae1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cae1-137">OUTPUTS</span></span>

### <span data-ttu-id="5cae1-138">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5cae1-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5cae1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cae1-139">NOTES</span></span>

<span data-ttu-id="5cae1-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5cae1-140">ALIASES</span></span>

<span data-ttu-id="5cae1-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="5cae1-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cae1-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="5cae1-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cae1-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cae1-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cae1-144">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="5cae1-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cae1-145">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="5cae1-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5cae1-146">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5cae1-147">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="5cae1-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5cae1-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="5cae1-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cae1-149">`[KeyName <String>]`: Server namnet.</span><span class="sxs-lookup"><span data-stu-id="5cae1-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5cae1-150">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5cae1-151">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5cae1-152">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="5cae1-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="5cae1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="5cae1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5cae1-154">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="5cae1-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5cae1-155">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="5cae1-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5cae1-156">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="5cae1-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5cae1-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cae1-157">RELATED LINKS</span></span>

