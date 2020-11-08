---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088728"
---
# <span data-ttu-id="8d523-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="8d523-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d523-102">SYNOPSIS</span></span>
<span data-ttu-id="8d523-103">Uppdaterar en privat DNS-zon från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8d523-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="8d523-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d523-104">SYNTAX</span></span>

### <span data-ttu-id="8d523-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="8d523-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d523-106">ID</span><span class="sxs-lookup"><span data-stu-id="8d523-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d523-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="8d523-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d523-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d523-108">DESCRIPTION</span></span>
<span data-ttu-id="8d523-109">Cmdleten **set-AzPrivateDnsZone** uppdaterar en DNS-zon (Private Domain Name System) från en angiven resurs grupp permanent.</span><span class="sxs-lookup"><span data-stu-id="8d523-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="8d523-110">Du kan skicka ett **PrivateDnsZone** -objekt med *PrivateZone* -parametern eller med hjälp av pipeline-operatorn eller så kan du ange *namn* och *ResourceGroupName* -parametrar.</span><span class="sxs-lookup"><span data-stu-id="8d523-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8d523-111">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8d523-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8d523-112">När du anger zonen med ett **PrivateDnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) uppdateras inte zonen om den har ändrats i Azure DNS sedan det lokala **PrivateDnsZone** -objektet hämtades (endast åtgärder som utförs direkt i DNS-zontypen antal som ändringar, åtgärder på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="8d523-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="8d523-113">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="8d523-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="8d523-114">Det här kan utelämnas med hjälp av parametern *Overwrite* som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="8d523-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="8d523-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d523-115">EXAMPLES</span></span>

### <span data-ttu-id="8d523-116">Exempel 1: uppdaterar en privat zon</span><span class="sxs-lookup"><span data-stu-id="8d523-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="8d523-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d523-117">PARAMETERS</span></span>

### <span data-ttu-id="8d523-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d523-118">-DefaultProfile</span></span>
<span data-ttu-id="8d523-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8d523-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d523-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d523-120">-Name</span></span>
<span data-ttu-id="8d523-121">Anger namnet på den privata DNS-zon som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="8d523-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="8d523-122">Du måste också ange parametern *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="8d523-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="8d523-123">Alternativt kan du ange den privata DNS-zonen med parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="8d523-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8d523-124">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="8d523-124">-Overwrite</span></span>
<span data-ttu-id="8d523-125">När du anger zonen med ett **PrivateDnsZone** -objekt (passerat via Pipelined eller *Zone* parameter) uppdateras inte zonen om den har ändrats i Azure DNS sedan det lokala **dnsZone** -objektet hämtades (endast åtgärder som utförs direkt i DNS-zontypen antal som ändringar, åtgärder på post uppsättningar i zonen gör inte).</span><span class="sxs-lookup"><span data-stu-id="8d523-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="8d523-126">Det skyddar ändringar i den gemensamma zonen.</span><span class="sxs-lookup"><span data-stu-id="8d523-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="8d523-127">Det här kan utelämnas med hjälp av parametern *Overwrite* som uppdaterar zonen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="8d523-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="8d523-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="8d523-128">-PrivateZone</span></span>
<span data-ttu-id="8d523-129">Zone-objekt som ska anges.</span><span class="sxs-lookup"><span data-stu-id="8d523-129">The zone object to set.</span></span>

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

### <span data-ttu-id="8d523-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d523-130">-ResourceGroupName</span></span>
<span data-ttu-id="8d523-131">Anger namnet på den resurs grupp som innehåller den zon som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8d523-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="8d523-132">Du måste också ange parametern *Zonnamn* .</span><span class="sxs-lookup"><span data-stu-id="8d523-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="8d523-133">Alternativt kan du ange den privata DNS-zonen med ett **dnsZone** -objekt som skickas via pipelinen eller parametern *Zone* .</span><span class="sxs-lookup"><span data-stu-id="8d523-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8d523-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d523-134">-ResourceId</span></span>
<span data-ttu-id="8d523-135">Privat DNS-zon ResourceID.</span><span class="sxs-lookup"><span data-stu-id="8d523-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="8d523-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8d523-136">-Tag</span></span>
<span data-ttu-id="8d523-137">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="8d523-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8d523-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d523-138">-Confirm</span></span>
<span data-ttu-id="8d523-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d523-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d523-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d523-140">-WhatIf</span></span>
<span data-ttu-id="8d523-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d523-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d523-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d523-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d523-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d523-143">CommonParameters</span></span>
<span data-ttu-id="8d523-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d523-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d523-145">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d523-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d523-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d523-146">INPUTS</span></span>

### <span data-ttu-id="8d523-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8d523-147">System.String</span></span>

### <span data-ttu-id="8d523-148">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="8d523-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d523-149">OUTPUTS</span></span>

### <span data-ttu-id="8d523-150">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="8d523-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d523-151">NOTES</span></span>

## <span data-ttu-id="8d523-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d523-152">RELATED LINKS</span></span>

[<span data-ttu-id="8d523-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="8d523-154">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="8d523-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8d523-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
