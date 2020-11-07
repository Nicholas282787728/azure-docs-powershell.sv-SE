---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsRecordSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 7c4f76b9731e82bd134be7ae38461a7d74e31e6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747490"
---
# <span data-ttu-id="d641f-101">Set-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d641f-101">Set-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d641f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d641f-102">SYNOPSIS</span></span>
<span data-ttu-id="d641f-103">Uppdaterar/anger en post uppsättning i en privat DNS-zon.</span><span class="sxs-lookup"><span data-stu-id="d641f-103">Updates/Sets a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="d641f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d641f-104">SYNTAX</span></span>

```
Set-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d641f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d641f-105">DESCRIPTION</span></span>
<span data-ttu-id="d641f-106">Set-AzPrivateDnsRecordSet cmdlet uppdaterar en post uppsättning i Azure Private DNS-tjänsten från ett lokalt RecordSet-objekt.</span><span class="sxs-lookup"><span data-stu-id="d641f-106">The Set-AzPrivateDnsRecordSet cmdlet updates a record set in the Azure Private DNS service from a local RecordSet object.</span></span> <span data-ttu-id="d641f-107">Du kan skicka ett RecordSet-objekt som en parameter eller med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d641f-107">You can pass a RecordSet object as a parameter or by using the pipeline operator.</span></span> <span data-ttu-id="d641f-108">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d641f-108">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="d641f-109">Post uppsättningen uppdateras inte om den har ändrats i Azure Private DNS sedan det lokala RecordSet-objektet hämtades.</span><span class="sxs-lookup"><span data-stu-id="d641f-109">The record set is not updated if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="d641f-110">Det skyddar mot samtidig ändringar.</span><span class="sxs-lookup"><span data-stu-id="d641f-110">This provides protection for concurrent changes.</span></span> <span data-ttu-id="d641f-111">Du kan dölja den här funktionen med hjälp av parametern overwrite, som uppdaterar post uppsättningen oavsett samtidig ändring.</span><span class="sxs-lookup"><span data-stu-id="d641f-111">You can suppress this behavior using the Overwrite parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="d641f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d641f-112">EXAMPLES</span></span>

### <span data-ttu-id="d641f-113">Exempel 1: uppdatera en post uppsättning</span><span class="sxs-lookup"><span data-stu-id="d641f-113">Example 1: Update a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzPrivateDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 172.16.0.0, 172.31.255.255}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d641f-114">Det första kommandot använder cmdleten Get-AzPrivateDnsRecordSet för att hämta angiven post uppsättning och lagrar den sedan i $RecordSet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d641f-114">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d641f-115">De andra och tredje kommandona är offline-operationer för att lägga till två poster i post uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="d641f-115">The second and third commands are off-line operations to add two A records to the record set.</span></span> <span data-ttu-id="d641f-116">Det sista kommandot använder cmdleten Set-AzPrivateDnsRecordSet för att bekräfta uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="d641f-116">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to commit the update.</span></span>

### <span data-ttu-id="d641f-117">Exempel 2: uppdatera en SOA-post</span><span class="sxs-lookup"><span data-stu-id="d641f-117">Example 2: Update an SOA record</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SOA/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : Myresourcegroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SOA
Records           : {[internal.cloudapp.net,admin.myzone.com,3600,300,2419200,300]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="d641f-118">Det första kommandot använder cmdleten Get-AzPrivateDnsRecordSet för att hämta angiven post uppsättning och lagrar den sedan i $RecordSet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="d641f-118">The first command uses the Get-AzPrivateDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="d641f-119">Det andra kommandot uppdaterar den angivna SOA-posten i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d641f-119">The second command updates the specified SOA record in $RecordSet.</span></span> <span data-ttu-id="d641f-120">Det sista kommandot använder cmdleten Set-AzPrivateDnsRecordSet för att sprida uppdateringen i $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="d641f-120">The final command uses the Set-AzPrivateDnsRecordSet cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="d641f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d641f-121">PARAMETERS</span></span>

### <span data-ttu-id="d641f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d641f-122">-DefaultProfile</span></span>
<span data-ttu-id="d641f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d641f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d641f-124">-Skriver över</span><span class="sxs-lookup"><span data-stu-id="d641f-124">-Overwrite</span></span>
<span data-ttu-id="d641f-125">Använd inte ETag-fältet i parameter uppsättning för att kontrol lera optimistiskt concurrency.</span><span class="sxs-lookup"><span data-stu-id="d641f-125">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="d641f-126">-Post uppsättning</span><span class="sxs-lookup"><span data-stu-id="d641f-126">-RecordSet</span></span>
<span data-ttu-id="d641f-127">Den post uppsättning där posten ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="d641f-127">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d641f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d641f-128">-Confirm</span></span>
<span data-ttu-id="d641f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d641f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d641f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d641f-130">-WhatIf</span></span>
<span data-ttu-id="d641f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d641f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d641f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d641f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d641f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d641f-133">CommonParameters</span></span>
<span data-ttu-id="d641f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d641f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d641f-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d641f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d641f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d641f-136">INPUTS</span></span>

### <span data-ttu-id="d641f-137">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d641f-137">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d641f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d641f-138">OUTPUTS</span></span>

### <span data-ttu-id="d641f-139">Microsoft. Azure. commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d641f-139">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="d641f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d641f-140">NOTES</span></span>

## <span data-ttu-id="d641f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d641f-141">RELATED LINKS</span></span>