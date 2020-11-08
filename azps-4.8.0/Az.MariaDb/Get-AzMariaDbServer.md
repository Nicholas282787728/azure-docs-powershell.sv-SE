---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262177"
---
# <span data-ttu-id="a8ee5-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="a8ee5-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="a8ee5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ee5-103">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-103">Gets information about a server.</span></span>

## <span data-ttu-id="a8ee5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8ee5-104">SYNTAX</span></span>

### <span data-ttu-id="a8ee5-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="a8ee5-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8ee5-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a8ee5-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8ee5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a8ee5-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a8ee5-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="a8ee5-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ee5-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8ee5-109">DESCRIPTION</span></span>
<span data-ttu-id="a8ee5-110">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-110">Gets information about a server.</span></span>

## <span data-ttu-id="a8ee5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8ee5-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ee5-112">Exempel 1: lista alla MariaDB under en prenumeration</span><span class="sxs-lookup"><span data-stu-id="a8ee5-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="a8ee5-113">Det här kommandot listar alla MariaDB under en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="a8ee5-114">Exempel 2: lista alla MariaDB under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="a8ee5-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="a8ee5-115">Det här kommandot listar alla MariaDB under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="a8ee5-116">Exempel 3: skaffa en MariaDB</span><span class="sxs-lookup"><span data-stu-id="a8ee5-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="a8ee5-117">Det här kommandot får en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="a8ee5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8ee5-118">PARAMETERS</span></span>

### <span data-ttu-id="a8ee5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ee5-119">-DefaultProfile</span></span>
<span data-ttu-id="a8ee5-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ee5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ee5-121">-InputObject</span></span>
<span data-ttu-id="a8ee5-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ee5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8ee5-123">-Name</span></span>
<span data-ttu-id="a8ee5-124">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-124">The name of the server.</span></span>

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

### <span data-ttu-id="a8ee5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ee5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8ee5-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a8ee5-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a8ee5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8ee5-128">-SubscriptionId</span></span>
<span data-ttu-id="a8ee5-129">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="a8ee5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ee5-130">CommonParameters</span></span>
<span data-ttu-id="a8ee5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ee5-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8ee5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ee5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8ee5-133">INPUTS</span></span>

### <span data-ttu-id="a8ee5-134">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="a8ee5-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="a8ee5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8ee5-135">OUTPUTS</span></span>

### <span data-ttu-id="a8ee5-136">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="a8ee5-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="a8ee5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8ee5-137">NOTES</span></span>

<span data-ttu-id="a8ee5-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a8ee5-138">ALIASES</span></span>

<span data-ttu-id="a8ee5-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="a8ee5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8ee5-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8ee5-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8ee5-142">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="a8ee5-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a8ee5-143">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a8ee5-144">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a8ee5-145">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a8ee5-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="a8ee5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a8ee5-147">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a8ee5-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a8ee5-149">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a8ee5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a8ee5-151">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a8ee5-152">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="a8ee5-153">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="a8ee5-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a8ee5-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8ee5-154">RELATED LINKS</span></span>

