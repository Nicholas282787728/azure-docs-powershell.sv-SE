---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585887"
---
# <span data-ttu-id="32e0b-101">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="32e0b-101">Remove-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="32e0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="32e0b-103">Tar bort ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="32e0b-103">Removes a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32e0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32e0b-104">SYNTAX</span></span>

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e0b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32e0b-105">DESCRIPTION</span></span>
<span data-ttu-id="32e0b-106">Remove-AzureRmDdosProtectionPlan cmdlet tar bort ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="32e0b-106">The Remove-AzureRmDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="32e0b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32e0b-107">EXAMPLES</span></span>

### <span data-ttu-id="32e0b-108">Exempel 1: ta bort ett tomt DDoS skydds abonnemang</span><span class="sxs-lookup"><span data-stu-id="32e0b-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="32e0b-109">I det här fallet tar vi bort ett DDoS skydds abonnemang enligt vad som angetts.</span><span class="sxs-lookup"><span data-stu-id="32e0b-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="32e0b-110">Exempel 2: ta bort ett DDoS skydds abonnemang som är associerat med ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="32e0b-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
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
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="32e0b-111">DDoS skydds planer kan inte tas bort om de är kopplade till ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="32e0b-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="32e0b-112">Det första steget är att avassociera båda objekten.</span><span class="sxs-lookup"><span data-stu-id="32e0b-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="32e0b-113">Här får vi den senaste versionen av det virtuella nätverk som är associerat med planen och vi anger egenskapen **DdosProtectionPlan** till ett tomt värde och flaggan **EnableDdosProtection** (flaggan får inte vara sann utan ett abonnemang).</span><span class="sxs-lookup"><span data-stu-id="32e0b-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="32e0b-114">Därefter behåller vi den nya statusen genom att översätta den lokala variabeln till **set-AzureRmVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="32e0b-114">Then, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span> <span data-ttu-id="32e0b-115">I det här läget är abonnemanget inte längre associerat med det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="32e0b-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="32e0b-116">Om det är den sista som är kopplad till planen kan vi ta bort DDoS skydds plan genom att använda kommandot Remove-AzureRmDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="32e0b-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzureRmDdosProtectionPlan.</span></span>

## <span data-ttu-id="32e0b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32e0b-117">PARAMETERS</span></span>

### <span data-ttu-id="32e0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e0b-118">-DefaultProfile</span></span>
<span data-ttu-id="32e0b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32e0b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32e0b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="32e0b-120">-Name</span></span>
<span data-ttu-id="32e0b-121">Anger namnet på det DDoS som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="32e0b-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="32e0b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32e0b-122">-PassThru</span></span>
<span data-ttu-id="32e0b-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="32e0b-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32e0b-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="32e0b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32e0b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32e0b-125">-ResourceGroupName</span></span>
<span data-ttu-id="32e0b-126">Anger resurs gruppen för det DDoS skydds abonnemang som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="32e0b-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="32e0b-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32e0b-127">-Confirm</span></span>
<span data-ttu-id="32e0b-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32e0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e0b-129">-WhatIf</span></span>
<span data-ttu-id="32e0b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32e0b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e0b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32e0b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e0b-132">CommonParameters</span></span>
<span data-ttu-id="32e0b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e0b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e0b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e0b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32e0b-135">INPUTS</span></span>

### <span data-ttu-id="32e0b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="32e0b-136">System.String</span></span>

## <span data-ttu-id="32e0b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32e0b-137">OUTPUTS</span></span>

### <span data-ttu-id="32e0b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32e0b-138">System.Boolean</span></span>

## <span data-ttu-id="32e0b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32e0b-139">NOTES</span></span>

## <span data-ttu-id="32e0b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32e0b-140">RELATED LINKS</span></span>

[<span data-ttu-id="32e0b-141">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="32e0b-141">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="32e0b-142">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="32e0b-142">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="32e0b-143">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32e0b-143">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="32e0b-144">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32e0b-144">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="32e0b-145">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="32e0b-145">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
