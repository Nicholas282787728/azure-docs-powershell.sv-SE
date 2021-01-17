---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388500"
---
# <span data-ttu-id="d54ef-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d54ef-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="d54ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d54ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d54ef-103">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="d54ef-103">Gets information about a server.</span></span>

## <span data-ttu-id="d54ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d54ef-104">SYNTAX</span></span>

### <span data-ttu-id="d54ef-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="d54ef-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d54ef-106">Lära</span><span class="sxs-lookup"><span data-stu-id="d54ef-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d54ef-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d54ef-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d54ef-108">Förteckning</span><span class="sxs-lookup"><span data-stu-id="d54ef-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d54ef-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d54ef-109">DESCRIPTION</span></span>
<span data-ttu-id="d54ef-110">Hämtar information om en server.</span><span class="sxs-lookup"><span data-stu-id="d54ef-110">Gets information about a server.</span></span>

## <span data-ttu-id="d54ef-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d54ef-111">EXAMPLES</span></span>

### <span data-ttu-id="d54ef-112">Exempel 1: lista alla MariaDB under en prenumeration</span><span class="sxs-lookup"><span data-stu-id="d54ef-112">Example 1: List all MariaDB under a subscriptions</span></span>
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

<span data-ttu-id="d54ef-113">Det här kommandot listar alla MariaDB under en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d54ef-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="d54ef-114">Exempel 2: lista alla MariaDB under en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d54ef-114">Example 2: List all MariaDB under a resource group</span></span>
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

<span data-ttu-id="d54ef-115">Det här kommandot listar alla MariaDB under en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d54ef-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="d54ef-116">Exempel 3: skaffa en MariaDB</span><span class="sxs-lookup"><span data-stu-id="d54ef-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="d54ef-117">Det här kommandot får en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d54ef-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="d54ef-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d54ef-118">PARAMETERS</span></span>

### <span data-ttu-id="d54ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d54ef-119">-DefaultProfile</span></span>
<span data-ttu-id="d54ef-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d54ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d54ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d54ef-121">-InputObject</span></span>
<span data-ttu-id="d54ef-122">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="d54ef-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d54ef-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="d54ef-123">-Name</span></span>
<span data-ttu-id="d54ef-124">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d54ef-124">The name of the server.</span></span>

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

### <span data-ttu-id="d54ef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d54ef-125">-ResourceGroupName</span></span>
<span data-ttu-id="d54ef-126">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d54ef-127">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d54ef-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d54ef-128">-SubscriptionId</span></span>
<span data-ttu-id="d54ef-129">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d54ef-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d54ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d54ef-130">CommonParameters</span></span>
<span data-ttu-id="d54ef-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d54ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d54ef-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d54ef-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d54ef-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d54ef-133">INPUTS</span></span>

### <span data-ttu-id="d54ef-134">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d54ef-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d54ef-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d54ef-135">OUTPUTS</span></span>

### <span data-ttu-id="d54ef-136">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="d54ef-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d54ef-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d54ef-137">NOTES</span></span>

<span data-ttu-id="d54ef-138">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d54ef-138">ALIASES</span></span>

<span data-ttu-id="d54ef-139">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="d54ef-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d54ef-140">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="d54ef-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d54ef-141">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d54ef-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d54ef-142">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="d54ef-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d54ef-143">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="d54ef-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d54ef-144">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d54ef-145">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="d54ef-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d54ef-146">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="d54ef-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d54ef-147">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d54ef-148">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d54ef-149">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d54ef-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="d54ef-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d54ef-151">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="d54ef-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d54ef-152">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="d54ef-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d54ef-153">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="d54ef-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d54ef-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d54ef-154">RELATED LINKS</span></span>

