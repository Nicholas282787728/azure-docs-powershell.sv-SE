---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: e301873b191a47be32298505b98eecd88cab9ac6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748091"
---
# <span data-ttu-id="6446c-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6446c-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="6446c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6446c-102">SYNOPSIS</span></span>
<span data-ttu-id="6446c-103">Skapar ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6446c-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="6446c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6446c-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6446c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6446c-105">DESCRIPTION</span></span>
<span data-ttu-id="6446c-106">New-AzDdosProtectionPlan-cmdleten skapar ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6446c-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="6446c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6446c-107">EXAMPLES</span></span>

### <span data-ttu-id="6446c-108">Exempel 1: skapa och koppla ett DDoS skydds abonnemang till ett nytt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="6446c-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzvirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="6446c-109">Först skapar vi ett nytt DDoS skydds abonnemang med kommandot **ny-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="6446c-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="6446c-110">Sedan skapar vi ett nytt virtuellt nätverk med **New-AzvirtualNetwork** och anger ID för det nya abonnemanget i parametern **DdosProtectionPlanId**.</span><span class="sxs-lookup"><span data-stu-id="6446c-110">Then, we create a new virtual network with **New-AzvirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="6446c-111">I det här fallet, eftersom vi associerar det virtuella nätverket med en plan, kan vi också ange parametern **EnableDdoSProtection**.</span><span class="sxs-lookup"><span data-stu-id="6446c-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="6446c-112">Exempel 2: skapa och koppla ett DDoS skydds abonnemang till ett befintligt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="6446c-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="6446c-113">Först skapar vi ett nytt DDoS skydds abonnemang med kommandot **ny-AzDdosProtectionPlan** .</span><span class="sxs-lookup"><span data-stu-id="6446c-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="6446c-114">För det andra får vi den senaste versionen av det virtuella nätverk vi vill associera med abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6446c-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="6446c-115">Vi uppdaterar egenskapen **DdosProtectionPlan** med ett **PSResourceId** -objekt som innehåller en referens till det ID för det nya abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6446c-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="6446c-116">I det här fallet kan vi även ange flaggan **EnableDdosProtection** till sant om vi associerar det virtuella nätverket med ett DDoS.</span><span class="sxs-lookup"><span data-stu-id="6446c-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="6446c-117">Slutligen sparar vi den nya statusen genom att översätta den lokala variabeln till **set-AzVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="6446c-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="6446c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6446c-118">PARAMETERS</span></span>

### <span data-ttu-id="6446c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6446c-119">-AsJob</span></span>
<span data-ttu-id="6446c-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6446c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6446c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6446c-121">-DefaultProfile</span></span>
<span data-ttu-id="6446c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6446c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="6446c-123">-Location</span></span>
<span data-ttu-id="6446c-124">Anger platsen för det DDoS som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6446c-124">Specifies the location of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="6446c-125">-Name</span></span>
<span data-ttu-id="6446c-126">Anger namnet på det DDoS som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6446c-126">Specifies the name of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6446c-127">-ResourceGroupName</span></span>
<span data-ttu-id="6446c-128">Anger resurs gruppen för det DDoS skydds abonnemang som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6446c-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6446c-129">-Tag</span></span>
<span data-ttu-id="6446c-130">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="6446c-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6446c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6446c-131">-Confirm</span></span>
<span data-ttu-id="6446c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6446c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6446c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6446c-133">-WhatIf</span></span>
<span data-ttu-id="6446c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6446c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6446c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6446c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6446c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6446c-136">CommonParameters</span></span>
<span data-ttu-id="6446c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6446c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6446c-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6446c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6446c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6446c-139">INPUTS</span></span>

### <span data-ttu-id="6446c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6446c-140">System.String</span></span>

### <span data-ttu-id="6446c-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6446c-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6446c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6446c-142">OUTPUTS</span></span>

### <span data-ttu-id="6446c-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6446c-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="6446c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6446c-144">NOTES</span></span>

## <span data-ttu-id="6446c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6446c-145">RELATED LINKS</span></span>

[<span data-ttu-id="6446c-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6446c-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="6446c-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="6446c-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="6446c-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6446c-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="6446c-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6446c-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="6446c-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6446c-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)