---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258739"
---
# <span data-ttu-id="7bbc9-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="7bbc9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbc9-103">Tar bort en privat DNS-zon från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="7bbc9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bbc9-104">SYNTAX</span></span>

### <span data-ttu-id="7bbc9-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="7bbc9-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbc9-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="7bbc9-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbc9-107">ID</span><span class="sxs-lookup"><span data-stu-id="7bbc9-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bbc9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bbc9-108">DESCRIPTION</span></span>
<span data-ttu-id="7bbc9-109">Cmdleten **Remove-AzPrivateDnsZone** tar permanent bort en DNS-zon (Private Domain Name System) från en angiven resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="7bbc9-110">Alla post uppsättningar i zonen tas också bort.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="7bbc9-111">Du kan skicka ett **PrivateDnsZone** -objekt med *PrivateZone* -parametern eller med hjälp av pipeline-operatorn eller så kan du ange *namn* och *ResourceGroupName* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="7bbc9-112">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="7bbc9-113">När du anger zonen med ett **PrivateDnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **PrivateDnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="7bbc9-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7bbc9-114">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7bbc9-115">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="7bbc9-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bbc9-116">EXAMPLES</span></span>

### <span data-ttu-id="7bbc9-117">Exempel 1: ta bort en privat zon</span><span class="sxs-lookup"><span data-stu-id="7bbc9-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7bbc9-118">Det här kommandot tar bort zonen med namnet myzone.com från resurs gruppen som heter MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="7bbc9-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bbc9-119">PARAMETERS</span></span>

### <span data-ttu-id="7bbc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbc9-120">-DefaultProfile</span></span>
<span data-ttu-id="7bbc9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7bbc9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bbc9-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bbc9-122">-Name</span></span>
<span data-ttu-id="7bbc9-123">Anger namnet på den privata DNS-zon som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="7bbc9-124">Du måste också ange parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="7bbc9-125">Alternativt kan du ange DNS-zonen med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7bbc9-126">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="7bbc9-126">-Overwrite</span></span>
<span data-ttu-id="7bbc9-127">När du anger zonen med ett **PrivateDnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) tas inte zonen bort om den har ändrats i Azure DNS sedan det lokala **PrivateDnsZone** -objektet hämtades (endast operationer i DNS-resurs-räknarna är som ändringar, åtgärderna på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="7bbc9-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="7bbc9-128">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="7bbc9-129">Detta kan döljas med hjälp av parametern *Overwrite* , som tar bort zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="7bbc9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bbc9-130">-PassThru</span></span>
<span data-ttu-id="7bbc9-131">Används för att skicka resultatet (boolesk) för åtgärden ta bort den privata zonen längre ned i pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="7bbc9-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-132">-PrivateZone</span></span>
<span data-ttu-id="7bbc9-133">Objektet för den privata zonen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bbc9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbc9-134">-ResourceGroupName</span></span>
<span data-ttu-id="7bbc9-135">Anger namnet på den resurs grupp som innehåller den zon som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="7bbc9-136">Du måste också ange parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="7bbc9-137">Alternativt kan du ange DNS-zonen med ett **PrivateDnsZone** -objekt, som skickas via pipelinen eller parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="7bbc9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbc9-138">-ResourceId</span></span>
<span data-ttu-id="7bbc9-139">Privat DNS-zon ResourceID.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="7bbc9-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bbc9-140">-Confirm</span></span>
<span data-ttu-id="7bbc9-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbc9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbc9-142">-WhatIf</span></span>
<span data-ttu-id="7bbc9-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bbc9-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbc9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbc9-145">CommonParameters</span></span>
<span data-ttu-id="7bbc9-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbc9-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbc9-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bbc9-148">INPUTS</span></span>

### <span data-ttu-id="7bbc9-149">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="7bbc9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7bbc9-150">System.String</span></span>

## <span data-ttu-id="7bbc9-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bbc9-151">OUTPUTS</span></span>

### <span data-ttu-id="7bbc9-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7bbc9-152">System.Boolean</span></span>

## <span data-ttu-id="7bbc9-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bbc9-153">NOTES</span></span>

## <span data-ttu-id="7bbc9-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bbc9-154">RELATED LINKS</span></span>

[<span data-ttu-id="7bbc9-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="7bbc9-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="7bbc9-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="7bbc9-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
