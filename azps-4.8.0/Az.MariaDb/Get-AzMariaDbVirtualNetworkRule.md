---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259535"
---
# <span data-ttu-id="85302-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="85302-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="85302-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85302-102">SYNOPSIS</span></span>
<span data-ttu-id="85302-103">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="85302-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="85302-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85302-104">SYNTAX</span></span>

### <span data-ttu-id="85302-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="85302-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="85302-106">Lära</span><span class="sxs-lookup"><span data-stu-id="85302-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="85302-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85302-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="85302-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85302-108">DESCRIPTION</span></span>
<span data-ttu-id="85302-109">Hämtar en regel för ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="85302-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="85302-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85302-110">EXAMPLES</span></span>

### <span data-ttu-id="85302-111">Exempel 1: lista alla virtuella nätverks regler under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="85302-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="85302-112">Det här kommandot visar alla virtuella nätverks regler under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="85302-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="85302-113">Exempel 2: Hämta ett virtuellt nätverks uttryck under en MariaDB</span><span class="sxs-lookup"><span data-stu-id="85302-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="85302-114">Det här kommandot hämtar regeln för virtuella nätverk under en MariaDB.</span><span class="sxs-lookup"><span data-stu-id="85302-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="85302-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85302-115">PARAMETERS</span></span>

### <span data-ttu-id="85302-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85302-116">-DefaultProfile</span></span>
<span data-ttu-id="85302-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85302-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85302-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85302-118">-InputObject</span></span>
<span data-ttu-id="85302-119">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="85302-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85302-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="85302-120">-Name</span></span>
<span data-ttu-id="85302-121">Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="85302-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85302-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85302-122">-PassThru</span></span>
<span data-ttu-id="85302-123">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="85302-123">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85302-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85302-124">-ResourceGroupName</span></span>
<span data-ttu-id="85302-125">Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="85302-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="85302-126">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="85302-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="85302-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="85302-127">-ServerName</span></span>
<span data-ttu-id="85302-128">Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="85302-128">The name of the server.</span></span>

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

### <span data-ttu-id="85302-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85302-129">-SubscriptionId</span></span>
<span data-ttu-id="85302-130">Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85302-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="85302-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85302-131">CommonParameters</span></span>
<span data-ttu-id="85302-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85302-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85302-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85302-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85302-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85302-134">INPUTS</span></span>

### <span data-ttu-id="85302-135">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="85302-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="85302-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85302-136">OUTPUTS</span></span>

### <span data-ttu-id="85302-137">Microsoft. Azure. PowerShell. cmdletar. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="85302-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="85302-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85302-138">NOTES</span></span>

<span data-ttu-id="85302-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="85302-139">ALIASES</span></span>

<span data-ttu-id="85302-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="85302-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85302-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="85302-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85302-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="85302-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85302-143">INPUTOBJECT <IMariaDbIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="85302-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85302-144">`[ConfigurationName <String>]`: Server konfigurationens namn.</span><span class="sxs-lookup"><span data-stu-id="85302-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="85302-145">`[DatabaseName <String>]`: Namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="85302-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="85302-146">`[FirewallRuleName <String>]`: Namnet på Server brand Väggs regeln.</span><span class="sxs-lookup"><span data-stu-id="85302-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="85302-147">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="85302-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85302-148">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="85302-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="85302-149">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller resursen.</span><span class="sxs-lookup"><span data-stu-id="85302-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="85302-150">Det här värdet kan hämtas från Azure Resource Manager API eller till portalen.</span><span class="sxs-lookup"><span data-stu-id="85302-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="85302-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Namnet på säkerhets varnings principen.</span><span class="sxs-lookup"><span data-stu-id="85302-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="85302-152">`[ServerName <String>]`: Namnet på servern.</span><span class="sxs-lookup"><span data-stu-id="85302-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="85302-153">`[SubscriptionId <String>]`: Det prenumerations-ID som identifierar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="85302-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="85302-154">`[VirtualNetworkRuleName <String>]`: Namnet på den virtuella nätverks regeln.</span><span class="sxs-lookup"><span data-stu-id="85302-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="85302-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85302-155">RELATED LINKS</span></span>
