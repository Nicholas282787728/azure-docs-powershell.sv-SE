---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757431"
---
# <span data-ttu-id="ef98e-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ef98e-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ef98e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef98e-102">SYNOPSIS</span></span>
<span data-ttu-id="ef98e-103">Uppdatera egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ef98e-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef98e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef98e-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef98e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef98e-105">DESCRIPTION</span></span>
<span data-ttu-id="ef98e-106">Cmdleten **Update-AzureRmStorageAccountNetworkRuleSet** uppdaterar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ef98e-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="ef98e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef98e-107">EXAMPLES</span></span>

### <span data-ttu-id="ef98e-108">Exempel 1: uppdatera alla egenskaper för NetworkRule, inmatnings regler med JSON</span><span class="sxs-lookup"><span data-stu-id="ef98e-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="ef98e-109">Det här kommandot uppdaterar alla egenskaper för NetworkRule, inmatnings regler med JSON.</span><span class="sxs-lookup"><span data-stu-id="ef98e-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="ef98e-110">Exempel 2: förbigå egenskapen bypass för NetworkRule</span><span class="sxs-lookup"><span data-stu-id="ef98e-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="ef98e-111">Den här kommando uppdateringen förbigå egenskap för NetworkRule (andra egenskaper ändras inte).</span><span class="sxs-lookup"><span data-stu-id="ef98e-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="ef98e-112">Exempel 3: Rensa regler med NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="ef98e-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="ef98e-113">Det här kommandot rensar bort NetworkRule för ett lagrings konto (andra egenskaper inte ändras).</span><span class="sxs-lookup"><span data-stu-id="ef98e-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="ef98e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef98e-114">PARAMETERS</span></span>

### <span data-ttu-id="ef98e-115">-Kringgå</span><span class="sxs-lookup"><span data-stu-id="ef98e-115">-Bypass</span></span>
<span data-ttu-id="ef98e-116">Det värde som ska kringgås för att uppdatera egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef98e-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="ef98e-117">Tillåtet värde är ingen eller en kombination av: â € ¢-loggning â € ¢-måtten â € ¢ Azureservices</span><span class="sxs-lookup"><span data-stu-id="ef98e-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ef98e-118">-DefaultAction</span></span>
<span data-ttu-id="ef98e-119">Värdet för DefaultAction uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef98e-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="ef98e-120">Tillåtna alternativ: â € ¢ Tillåt â € ¢ neka</span><span class="sxs-lookup"><span data-stu-id="ef98e-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="ef98e-121">-IPRule</span></span>
<span data-ttu-id="ef98e-122">Matrisen med IpRule-objekt som ska uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef98e-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef98e-123">-Name</span></span>
<span data-ttu-id="ef98e-124">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ef98e-124">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef98e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef98e-126">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="ef98e-126">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ef98e-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="ef98e-128">Matrisen med VirtualNetworkRule-objekt som ska uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ef98e-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef98e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef98e-129">-Confirm</span></span>
<span data-ttu-id="ef98e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef98e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef98e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef98e-131">-WhatIf</span></span>
<span data-ttu-id="ef98e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef98e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef98e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef98e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef98e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef98e-134">-DefaultProfile</span></span>
<span data-ttu-id="ef98e-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef98e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef98e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef98e-136">CommonParameters</span></span>
<span data-ttu-id="ef98e-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef98e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef98e-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef98e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef98e-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef98e-139">INPUTS</span></span>

### <span data-ttu-id="ef98e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ef98e-140">System.String</span></span>
<span data-ttu-id="ef98e-141">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ef98e-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ef98e-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef98e-142">OUTPUTS</span></span>

### <span data-ttu-id="ef98e-143">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ef98e-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ef98e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef98e-144">NOTES</span></span>

## <span data-ttu-id="ef98e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef98e-145">RELATED LINKS</span></span>

