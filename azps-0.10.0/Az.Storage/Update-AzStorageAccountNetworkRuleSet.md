---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: b92da8f6128ecc58a8e85d5e8f3f92347fd8dce1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923402"
---
# <span data-ttu-id="52020-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="52020-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="52020-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52020-102">SYNOPSIS</span></span>
<span data-ttu-id="52020-103">Uppdatera egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="52020-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="52020-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52020-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52020-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52020-105">DESCRIPTION</span></span>
<span data-ttu-id="52020-106">Cmdleten **Update-AzStorageAccountNetworkRuleSet** uppdaterar egenskapen NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="52020-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="52020-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52020-107">EXAMPLES</span></span>

### <span data-ttu-id="52020-108">Exempel 1: uppdatera alla egenskaper för NetworkRule, inmatnings regler med JSON</span><span class="sxs-lookup"><span data-stu-id="52020-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="52020-109">Det här kommandot uppdaterar alla egenskaper för NetworkRule, inmatnings regler med JSON.</span><span class="sxs-lookup"><span data-stu-id="52020-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="52020-110">Exempel 2: förbigå egenskapen bypass för NetworkRule</span><span class="sxs-lookup"><span data-stu-id="52020-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="52020-111">Den här kommando uppdateringen förbigå egenskap för NetworkRule (andra egenskaper ändras inte).</span><span class="sxs-lookup"><span data-stu-id="52020-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="52020-112">Exempel 3: Rensa regler med NetworkRule för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="52020-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="52020-113">Det här kommandot rensar bort NetworkRule för ett lagrings konto (andra egenskaper inte ändras).</span><span class="sxs-lookup"><span data-stu-id="52020-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="52020-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52020-114">PARAMETERS</span></span>

### <span data-ttu-id="52020-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52020-115">-AsJob</span></span>
<span data-ttu-id="52020-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="52020-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52020-117">-Kringgå</span><span class="sxs-lookup"><span data-stu-id="52020-117">-Bypass</span></span>
<span data-ttu-id="52020-118">Det värde som ska kringgås för att uppdatera egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="52020-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="52020-119">Tillåtet värde är ingen eller någon kombination av: • loggning • mått • Azureservices</span><span class="sxs-lookup"><span data-stu-id="52020-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="52020-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="52020-120">-DefaultAction</span></span>
<span data-ttu-id="52020-121">Värdet för DefaultAction uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="52020-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="52020-122">Tillåtna alternativ: • Tillåt • neka</span><span class="sxs-lookup"><span data-stu-id="52020-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="52020-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52020-123">-DefaultProfile</span></span>
<span data-ttu-id="52020-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52020-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52020-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="52020-125">-IPRule</span></span>
<span data-ttu-id="52020-126">Matrisen med IpRule-objekt som ska uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="52020-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="52020-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="52020-127">-Name</span></span>
<span data-ttu-id="52020-128">Anger namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="52020-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="52020-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52020-129">-ResourceGroupName</span></span>
<span data-ttu-id="52020-130">Anger namnet på resurs gruppen som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="52020-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="52020-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52020-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="52020-132">Matrisen med VirtualNetworkRule-objekt som ska uppdateras till egenskapen NetworkRule för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="52020-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="52020-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52020-133">-Confirm</span></span>
<span data-ttu-id="52020-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52020-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52020-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52020-135">-WhatIf</span></span>
<span data-ttu-id="52020-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52020-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52020-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52020-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52020-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52020-138">CommonParameters</span></span>
<span data-ttu-id="52020-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52020-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52020-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52020-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52020-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52020-141">INPUTS</span></span>

### <span data-ttu-id="52020-142">System. String</span><span class="sxs-lookup"><span data-stu-id="52020-142">System.String</span></span>

### <span data-ttu-id="52020-143">Microsoft. Azure. commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="52020-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="52020-144">Parametrar: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52020-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="52020-145">Microsoft. Azure. commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="52020-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="52020-146">Parametrar: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52020-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="52020-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52020-147">OUTPUTS</span></span>

### <span data-ttu-id="52020-148">Microsoft. Azure. commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="52020-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="52020-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52020-149">NOTES</span></span>

## <span data-ttu-id="52020-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52020-150">RELATED LINKS</span></span>
