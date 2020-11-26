---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323874"
---
# <span data-ttu-id="d330b-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="d330b-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="d330b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d330b-102">SYNOPSIS</span></span>
<span data-ttu-id="d330b-103">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="d330b-103">Gets information about a server.</span></span>

## <span data-ttu-id="d330b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d330b-104">SYNTAX</span></span>

### <span data-ttu-id="d330b-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="d330b-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d330b-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d330b-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d330b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d330b-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d330b-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d330b-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d330b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d330b-109">DESCRIPTION</span></span>
<span data-ttu-id="d330b-110">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="d330b-110">Gets information about a server.</span></span>

## <span data-ttu-id="d330b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d330b-111">EXAMPLES</span></span>

### <span data-ttu-id="d330b-112">Exempel 1: skaffa MySql server med standard kontext</span><span class="sxs-lookup"><span data-stu-id="d330b-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d330b-113">Denna cmdlet får MySql-server med standard kontext.</span><span class="sxs-lookup"><span data-stu-id="d330b-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="d330b-114">Exempel 2: skaffa MySql Server efter resurs grupp och Server namn</span><span class="sxs-lookup"><span data-stu-id="d330b-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d330b-115">Denna cmdlet hämtar MySql-servern efter resurs grupp och Server namn.</span><span class="sxs-lookup"><span data-stu-id="d330b-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="d330b-116">Exempel 3: listar alla MySql-servrar i angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d330b-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d330b-117">Denna cmdlet visar alla MySql-servrar i angiven resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d330b-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="d330b-118">Exempel 4: skaffa MySql-servern efter identitet</span><span class="sxs-lookup"><span data-stu-id="d330b-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="d330b-119">Med denna cmdlet-lista får du en MySql-server med identitet.</span><span class="sxs-lookup"><span data-stu-id="d330b-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="d330b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d330b-120">PARAMETERS</span></span>

### <span data-ttu-id="d330b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d330b-121">-DefaultProfile</span></span>
<span data-ttu-id="d330b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d330b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d330b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d330b-123">-InputObject</span></span>
<span data-ttu-id="d330b-124">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d330b-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d330b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d330b-125">-Name</span></span>
<span data-ttu-id="d330b-126">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d330b-126">The name of the server.</span></span>

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

### <span data-ttu-id="d330b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d330b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d330b-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d330b-128">The name of the resource group.</span></span>
<span data-ttu-id="d330b-129">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d330b-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d330b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d330b-130">-SubscriptionId</span></span>
<span data-ttu-id="d330b-131">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d330b-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d330b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d330b-132">CommonParameters</span></span>
<span data-ttu-id="d330b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d330b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d330b-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d330b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d330b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d330b-135">INPUTS</span></span>

### <span data-ttu-id="d330b-136">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d330b-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d330b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d330b-137">OUTPUTS</span></span>

### <span data-ttu-id="d330b-138">Microsoft. Azure. PowerShell. cmdletar. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="d330b-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d330b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d330b-139">NOTES</span></span>

<span data-ttu-id="d330b-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d330b-140">ALIASES</span></span>

<span data-ttu-id="d330b-141">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d330b-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d330b-142">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d330b-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d330b-143">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d330b-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d330b-144">INPUTOBJECT <IMySqlIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d330b-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d330b-145">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="d330b-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d330b-146">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d330b-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d330b-147">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d330b-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d330b-148">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d330b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d330b-149">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="d330b-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d330b-150">`[ResourceGroupName <String>]`: Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d330b-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d330b-151">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="d330b-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d330b-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="d330b-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d330b-153">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d330b-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d330b-154">`[SubscriptionId <String>]`: Mål prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="d330b-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d330b-155">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d330b-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d330b-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d330b-156">RELATED LINKS</span></span>
