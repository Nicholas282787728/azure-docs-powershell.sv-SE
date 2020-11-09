---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323100"
---
# <span data-ttu-id="cd52d-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="cd52d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd52d-102">SYNOPSIS</span></span>
<span data-ttu-id="cd52d-103">Uppdaterar/anger en virtuell nätverks länk som är kopplad till en privat zon och en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cd52d-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="cd52d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd52d-104">SYNTAX</span></span>

### <span data-ttu-id="cd52d-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="cd52d-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd52d-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="cd52d-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd52d-107">ID</span><span class="sxs-lookup"><span data-stu-id="cd52d-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd52d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd52d-108">DESCRIPTION</span></span>
<span data-ttu-id="cd52d-109">Cmdleten **set-AzPrivateDnsVirtualNetworkLink** uppdaterar en länk som är kopplad till en zon från en viss resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cd52d-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="cd52d-110">Du kan skicka ett **PSPrivateDnsVirtualNetworkLink** -objekt med parametern *Link* eller med hjälp av en pipeline-Operator, eller så kan du ange *namnet* *Zonnamn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="cd52d-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cd52d-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="cd52d-112">När du anger zonen med ett **PSPrivateDnsVirtualNetworkLink** -objekt (som skickas via pipeline-eller *länk* parameter) uppdateras inte länken om den har ändrats i Azure DNS sedan det lokala **PSPrivateDnsVirtualNetworkLink** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="cd52d-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="cd52d-113">Det skyddar mot samtidig länk ändringar.</span><span class="sxs-lookup"><span data-stu-id="cd52d-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="cd52d-114">Det här kan döljas med hjälp av parametern *Overwrite* som uppdaterar länken oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="cd52d-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="cd52d-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd52d-115">EXAMPLES</span></span>

### <span data-ttu-id="cd52d-116">Exempel 1: Ange en länk</span><span class="sxs-lookup"><span data-stu-id="cd52d-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="cd52d-117">Det här kommandot anger IsRegistrationEnabled till sant för länken som heter min länk, länkad till zonen myzone.com från resurs gruppen med namnet MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd52d-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="cd52d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd52d-118">PARAMETERS</span></span>

### <span data-ttu-id="cd52d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd52d-119">-DefaultProfile</span></span>
<span data-ttu-id="cd52d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cd52d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd52d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd52d-121">-InputObject</span></span>
<span data-ttu-id="cd52d-122">Det virtuella nätverks länk-objekt som du vill ange.</span><span class="sxs-lookup"><span data-stu-id="cd52d-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="cd52d-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="cd52d-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="cd52d-124">Booleskt värde som representerar om registrering är aktiverat för det virtuella nätverks länken.</span><span class="sxs-lookup"><span data-stu-id="cd52d-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd52d-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd52d-125">-Name</span></span>
<span data-ttu-id="cd52d-126">Anger namnet på den länk som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="cd52d-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="cd52d-127">Du måste också ange parametern *ResourceGroupName* och *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="cd52d-128">Alternativt kan du ange den privata DNS-länken med parametern *Link* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="cd52d-129">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="cd52d-129">-Overwrite</span></span>
<span data-ttu-id="cd52d-130">När du anger länken med ett **PSPrivateDnsVirtualNetworkLink** -objekt (passerat via pipeline eller *länk* parameter) tas länken inte bort om den har ändrats i Azure DNS sedan det lokala **PSPrivateDnsVirtualNetworkLink** -objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="cd52d-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="cd52d-131">Det skyddar mot samtidig länk ändringar.</span><span class="sxs-lookup"><span data-stu-id="cd52d-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="cd52d-132">Det här kan döljas med hjälp av parametern *Overwrite* , som tar bort länken oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="cd52d-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="cd52d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd52d-133">-ResourceGroupName</span></span>
<span data-ttu-id="cd52d-134">Anger namnet på den resurs grupp som innehåller länken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cd52d-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="cd52d-135">Du måste också ange parametern *Zonnamn* och *namn* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="cd52d-136">Alternativt kan du ange den virtuella nätverks länken med ett **PSPrivateDnsVirtualNetworkLink** -objekt som skickas via pipeline eller *Link* -parametern.</span><span class="sxs-lookup"><span data-stu-id="cd52d-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="cd52d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd52d-137">-ResourceId</span></span>
<span data-ttu-id="cd52d-138">Privat DNS-zon ResourceID.</span><span class="sxs-lookup"><span data-stu-id="cd52d-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="cd52d-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cd52d-139">-Tag</span></span>
<span data-ttu-id="cd52d-140">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="cd52d-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cd52d-141">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="cd52d-141">-ZoneName</span></span>
<span data-ttu-id="cd52d-142">Anger namnet på den DNS-zon som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="cd52d-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="cd52d-143">Du måste också ange parametern *namn* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="cd52d-144">Alternativt kan du ange den privata DNS-länken med parametern *Link* .</span><span class="sxs-lookup"><span data-stu-id="cd52d-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="cd52d-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd52d-145">-Confirm</span></span>
<span data-ttu-id="cd52d-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd52d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd52d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd52d-147">-WhatIf</span></span>
<span data-ttu-id="cd52d-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd52d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd52d-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd52d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd52d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd52d-150">CommonParameters</span></span>
<span data-ttu-id="cd52d-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd52d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd52d-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd52d-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd52d-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd52d-153">INPUTS</span></span>

### <span data-ttu-id="cd52d-154">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="cd52d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="cd52d-155">System.String</span></span>

## <span data-ttu-id="cd52d-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd52d-156">OUTPUTS</span></span>

### <span data-ttu-id="cd52d-157">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="cd52d-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd52d-158">NOTES</span></span>

## <span data-ttu-id="cd52d-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd52d-159">RELATED LINKS</span></span>

[<span data-ttu-id="cd52d-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="cd52d-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="cd52d-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="cd52d-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
