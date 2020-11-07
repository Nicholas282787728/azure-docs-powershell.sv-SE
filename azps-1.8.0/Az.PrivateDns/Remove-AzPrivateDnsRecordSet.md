---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c1b98f1d4408bddec94830a81bf06fa7c78baa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747494"
---
# <span data-ttu-id="60195-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="60195-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="60195-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60195-102">SYNOPSIS</span></span>
<span data-ttu-id="60195-103">Tar bort en post uppsättning från en privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="60195-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="60195-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60195-104">SYNTAX</span></span>

### <span data-ttu-id="60195-105">Fält (standard)</span><span class="sxs-lookup"><span data-stu-id="60195-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60195-106">Mixed</span><span class="sxs-lookup"><span data-stu-id="60195-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60195-107">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="60195-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60195-108">ID</span><span class="sxs-lookup"><span data-stu-id="60195-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60195-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60195-109">DESCRIPTION</span></span>
<span data-ttu-id="60195-110">Remove-AzPrivateDnsRecordSet-cmdleten tar bort angiven post uppsättning från den angivna zonen.</span><span class="sxs-lookup"><span data-stu-id="60195-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="60195-111">Du kan inte ta bort SOA-poster som skapas automatiskt vid den privata zonen.</span><span class="sxs-lookup"><span data-stu-id="60195-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="60195-112">Du kan skicka ett RecordSet-objekt till denna cmdlet med hjälp av en pipeline-operator eller som en parameter eller som en ResourceId.</span><span class="sxs-lookup"><span data-stu-id="60195-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="60195-113">Om du vill identifiera en post uppsättning efter namn och typ utan att använda ett RecordSet-objekt måste du överföra zonen som ett PSPrivateDnsZone-objekt till denna cmdlet genom att använda pipeline-operatorn eller som en parameter, eller också kan du ange parametrarna zonnamn och ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="60195-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="60195-114">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="60195-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="60195-115">När du anger en post uppsättning med hjälp av ett RecordSet-objekt raderas inte post uppsättningen om den har ändrats i Azure Private DNS sedan det lokala RecordSet-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="60195-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="60195-116">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="60195-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="60195-117">Du kan förhindra detta genom att använda parametern overwrite, som tar bort post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="60195-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="60195-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60195-118">EXAMPLES</span></span>

### <span data-ttu-id="60195-119">Exempel 1: ta bort en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="60195-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="60195-120">Det första kommandot får den angivna post uppsättningen och lagrar den sedan i $RecordSet variabel. Det andra kommandot tar bort post uppsättningen i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="60195-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="60195-121">Exempel 2: ta bort en post uppsättning och ignorera alla bekräftelser</span><span class="sxs-lookup"><span data-stu-id="60195-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="60195-122">Det första kommandot får den angivna post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="60195-122">The first command gets the specified record set.</span></span> <span data-ttu-id="60195-123">Det andra kommandot tar bort post uppsättningen, även om den har ändrats under tiden.</span><span class="sxs-lookup"><span data-stu-id="60195-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="60195-124">Bekräftelse uppmaningar ignoreras.</span><span class="sxs-lookup"><span data-stu-id="60195-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="60195-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60195-125">PARAMETERS</span></span>

### <span data-ttu-id="60195-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60195-126">-DefaultProfile</span></span>
<span data-ttu-id="60195-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="60195-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60195-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="60195-128">-Name</span></span>
<span data-ttu-id="60195-129">Namnet på posterna i post uppsättningen (i förhållande till namnet på zonen och utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="60195-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60195-130">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="60195-130">-Overwrite</span></span>
<span data-ttu-id="60195-131">Använd inte ETag-fältet i parameter uppsättning för att kontrol lera optimistiskt concurrency.</span><span class="sxs-lookup"><span data-stu-id="60195-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="60195-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60195-132">-PassThru</span></span>
<span data-ttu-id="60195-133">Används för att skicka resultatet (boolesk) för åtgärden ta bort den privata zonen längre ned i pipeline.</span><span class="sxs-lookup"><span data-stu-id="60195-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="60195-134">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="60195-134">-RecordSet</span></span>
<span data-ttu-id="60195-135">Den post uppsättning där posten ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="60195-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60195-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="60195-136">-RecordType</span></span>
<span data-ttu-id="60195-137">Typen för privata DNS-poster i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="60195-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60195-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60195-138">-ResourceGroupName</span></span>
<span data-ttu-id="60195-139">Den resurs grupp som zonen tillhör.</span><span class="sxs-lookup"><span data-stu-id="60195-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="60195-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60195-140">-ResourceId</span></span>
<span data-ttu-id="60195-141">Privata DNS-RecprdSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="60195-141">Private DNS RecprdSet ResourceID.</span></span>

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

### <span data-ttu-id="60195-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="60195-142">-Zone</span></span>
<span data-ttu-id="60195-143">PrivateDnsZone-objektet som representerar den zon där du vill skapa post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="60195-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60195-144">-Zonnamn</span><span class="sxs-lookup"><span data-stu-id="60195-144">-ZoneName</span></span>
<span data-ttu-id="60195-145">Den zon där post uppsättningen finns (utan en avslutande punkt).</span><span class="sxs-lookup"><span data-stu-id="60195-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="60195-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="60195-146">-Confirm</span></span>
<span data-ttu-id="60195-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="60195-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60195-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60195-148">-WhatIf</span></span>
<span data-ttu-id="60195-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="60195-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60195-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="60195-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60195-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60195-151">CommonParameters</span></span>
<span data-ttu-id="60195-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60195-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60195-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60195-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60195-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60195-154">INPUTS</span></span>

### <span data-ttu-id="60195-155">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="60195-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="60195-156">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="60195-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="60195-157">System. String</span><span class="sxs-lookup"><span data-stu-id="60195-157">System.String</span></span>

## <span data-ttu-id="60195-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60195-158">OUTPUTS</span></span>

### <span data-ttu-id="60195-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60195-159">System.Boolean</span></span>

## <span data-ttu-id="60195-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60195-160">NOTES</span></span>

## <span data-ttu-id="60195-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60195-161">RELATED LINKS</span></span>