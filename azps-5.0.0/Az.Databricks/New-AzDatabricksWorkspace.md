---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320215"
---
# <span data-ttu-id="df524-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="df524-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="df524-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df524-102">SYNOPSIS</span></span>
<span data-ttu-id="df524-103">Skapar en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="df524-103">Creates a new workspace.</span></span>

## <span data-ttu-id="df524-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df524-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df524-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df524-105">DESCRIPTION</span></span>
<span data-ttu-id="df524-106">Skapar en ny arbets yta.</span><span class="sxs-lookup"><span data-stu-id="df524-106">Creates a new workspace.</span></span>

## <span data-ttu-id="df524-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df524-107">EXAMPLES</span></span>

### <span data-ttu-id="df524-108">Exempel 1: skapa en Databricks-arbetsyta</span><span class="sxs-lookup"><span data-stu-id="df524-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="df524-109">Det här kommandot skapar en Databricks-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="df524-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="df524-110">Exempel 2: skapa en Databricks-arbetsyta med ett anpassat virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="df524-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="df524-111">Det här kommandot skapar en Databricks-arbetsyta med anpassat virtuellt nätverk i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="df524-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="df524-112">Exempel 3: skapa en Databricks-arbetsyta med Aktivera kryptering</span><span class="sxs-lookup"><span data-stu-id="df524-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="df524-113">Det här kommandot skapar en Databricks-arbetsyta och anger att den ska förberedas för kryptering.</span><span class="sxs-lookup"><span data-stu-id="df524-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="df524-114">Se exemplen på Update-AzDatabricksWorkspace för att få fler inställningar för kryptering.</span><span class="sxs-lookup"><span data-stu-id="df524-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="df524-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df524-115">PARAMETERS</span></span>

### <span data-ttu-id="df524-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df524-116">-AsJob</span></span>
<span data-ttu-id="df524-117">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="df524-117">Run the command as a job</span></span>

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

### <span data-ttu-id="df524-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df524-118">-DefaultProfile</span></span>
<span data-ttu-id="df524-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df524-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df524-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="df524-120">-Location</span></span>
<span data-ttu-id="df524-121">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="df524-121">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df524-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="df524-123">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df524-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="df524-124">-Name</span></span>
<span data-ttu-id="df524-125">Namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="df524-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="df524-126">-NoWait</span></span>
<span data-ttu-id="df524-127">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="df524-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df524-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="df524-128">-PrepareEncryption</span></span>
<span data-ttu-id="df524-129">Förbereda arbets ytan för kryptering.</span><span class="sxs-lookup"><span data-stu-id="df524-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="df524-130">Aktiverar hanterad identitet för hanterat lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="df524-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="df524-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="df524-131">-PrivateSubnetName</span></span>
<span data-ttu-id="df524-132">Namnet på det privata under nätet i det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="df524-132">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="df524-133">-PublicSubnetName</span></span>
<span data-ttu-id="df524-134">Namnet på ett offentligt undernät i det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="df524-134">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="df524-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="df524-136">Ett booleskt värde som anger om DBFS-rot fil systemet kommer att aktive ras med sekundärt krypterings nivå med Platform-hanterade nycklar för data på rest.</span><span class="sxs-lookup"><span data-stu-id="df524-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="df524-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df524-137">-ResourceGroupName</span></span>
<span data-ttu-id="df524-138">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="df524-138">The name of the resource group.</span></span>
<span data-ttu-id="df524-139">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="df524-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="df524-140">-Sku</span></span>
<span data-ttu-id="df524-141">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="df524-141">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df524-142">-SubscriptionId</span></span>
<span data-ttu-id="df524-143">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="df524-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="df524-144">-Tag</span></span>
<span data-ttu-id="df524-145">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="df524-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="df524-146">-VirtualNetworkId</span></span>
<span data-ttu-id="df524-147">ID för ett virtuellt nätverk där detta Databricks-kluster ska skapas.</span><span class="sxs-lookup"><span data-stu-id="df524-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df524-148">-Confirm</span></span>
<span data-ttu-id="df524-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df524-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df524-150">-WhatIf</span></span>
<span data-ttu-id="df524-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df524-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df524-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df524-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df524-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df524-153">CommonParameters</span></span>
<span data-ttu-id="df524-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df524-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df524-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df524-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df524-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df524-156">INPUTS</span></span>

## <span data-ttu-id="df524-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df524-157">OUTPUTS</span></span>

### <span data-ttu-id="df524-158">Microsoft. Azure. PowerShell. cmdletar. Databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="df524-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="df524-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df524-159">NOTES</span></span>

<span data-ttu-id="df524-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="df524-160">ALIASES</span></span>

## <span data-ttu-id="df524-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df524-161">RELATED LINKS</span></span>
