---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258746"
---
# <span data-ttu-id="86952-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="86952-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="86952-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86952-102">SYNOPSIS</span></span>
<span data-ttu-id="86952-103">Tar bort en virtuell nätverks länk från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="86952-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="86952-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86952-104">SYNTAX</span></span>

### <span data-ttu-id="86952-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="86952-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86952-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="86952-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86952-107">ID</span><span class="sxs-lookup"><span data-stu-id="86952-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86952-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86952-108">DESCRIPTION</span></span>
<span data-ttu-id="86952-109">Med cmdleten **Remove-AzPrivateDnsVirtualNetworkLink** tar du bort en privat DNS-länk (Domain Name System) från en angiven resurs grupp permanent.</span><span class="sxs-lookup"><span data-stu-id="86952-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="86952-110">Du kan skicka ett **PSPrivateDnsVirtualNetworkLink** -objekt med parametern *Link* eller med hjälp av en pipeline-Operator, eller så kan du ange *namnet* *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="86952-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="86952-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="86952-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="86952-112">När du anger länken med ett **PSPrivateDnsVirtualNetworkLink** -objekt (passerat via pipeline eller *länk* parameter) tas länken inte bort om den har ändrats i Azure Private DNS sedan det lokala **PSPrivateDnsVirtualNetworkLink** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="86952-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="86952-113">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="86952-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="86952-114">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="86952-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="86952-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86952-115">EXAMPLES</span></span>

### <span data-ttu-id="86952-116">Exempel 1: ta bort en länk</span><span class="sxs-lookup"><span data-stu-id="86952-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="86952-117">Det här kommandot tar bort länken som heter hyperlänk som är länkad till zonen myzone.com från resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86952-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="86952-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86952-118">PARAMETERS</span></span>

### <span data-ttu-id="86952-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86952-119">-DefaultProfile</span></span>
<span data-ttu-id="86952-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="86952-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86952-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86952-121">-InputObject</span></span>
<span data-ttu-id="86952-122">Det virtuella nätverks länk objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="86952-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86952-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="86952-123">-Name</span></span>
<span data-ttu-id="86952-124">Anger namnet på den länk som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="86952-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="86952-125">Du måste också ange parametern *ResourceGroupName* och *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="86952-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="86952-126">Alternativt kan du ange länken med parametern *Link* .</span><span class="sxs-lookup"><span data-stu-id="86952-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-127">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="86952-127">-Overwrite</span></span>
<span data-ttu-id="86952-128">När du anger zonen med ett **PSPrivateDnsVirtualNetworkLink** -objekt (som skickas via pipeline-eller *länk* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **PSPrivateDnsVirtualNetworkLink** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="86952-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="86952-129">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="86952-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="86952-130">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="86952-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86952-131">-PassThru</span></span>
<span data-ttu-id="86952-132">Används för att skicka resultatet (boolesk) för åtgärden ta bort virtuellt nätverk längre ned.</span><span class="sxs-lookup"><span data-stu-id="86952-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="86952-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86952-133">-ResourceGroupName</span></span>
<span data-ttu-id="86952-134">Anger namnet på den resurs grupp som innehåller länken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="86952-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="86952-135">Du måste också ange parametern *Zonnamn* och *namn* .</span><span class="sxs-lookup"><span data-stu-id="86952-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="86952-136">Alternativt kan du ange DNS-zonen med ett **PSPrivateDnsVirtualNetworkLink** -objekt, som skickas via pipeline eller *Link* -parametern.</span><span class="sxs-lookup"><span data-stu-id="86952-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86952-137">-ResourceId</span></span>
<span data-ttu-id="86952-138">Anger länkens resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="86952-138">Specifies the ARM resource ID of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86952-139">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="86952-139">-ZoneName</span></span>
<span data-ttu-id="86952-140">Anger namnet på den privata DNS-zon som länken är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="86952-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="86952-141">Du måste också ange parametern *ResourceGroupName* och *Name* .</span><span class="sxs-lookup"><span data-stu-id="86952-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="86952-142">Alternativt kan du ange länken med parametern *Link* .</span><span class="sxs-lookup"><span data-stu-id="86952-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86952-143">-Confirm</span></span>
<span data-ttu-id="86952-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86952-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86952-145">-WhatIf</span></span>
<span data-ttu-id="86952-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86952-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86952-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86952-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86952-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86952-148">CommonParameters</span></span>
<span data-ttu-id="86952-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86952-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86952-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86952-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86952-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86952-151">INPUTS</span></span>

### <span data-ttu-id="86952-152">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="86952-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="86952-153">System. String</span><span class="sxs-lookup"><span data-stu-id="86952-153">System.String</span></span>

## <span data-ttu-id="86952-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86952-154">OUTPUTS</span></span>

### <span data-ttu-id="86952-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86952-155">System.Boolean</span></span>

## <span data-ttu-id="86952-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86952-156">NOTES</span></span>

## <span data-ttu-id="86952-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86952-157">RELATED LINKS</span></span>

[<span data-ttu-id="86952-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="86952-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="86952-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="86952-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="86952-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="86952-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
