---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: 392f9362df1cafdb6c047020b3381a7b16320607
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525997"
---
# <span data-ttu-id="1a789-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="1a789-101">New-AzIotHub</span></span>

## <span data-ttu-id="1a789-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a789-102">SYNOPSIS</span></span>
<span data-ttu-id="1a789-103">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="1a789-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="1a789-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a789-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a789-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a789-105">DESCRIPTION</span></span>
<span data-ttu-id="1a789-106">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="1a789-106">Creates a new IotHub.</span></span>
<span data-ttu-id="1a789-107">Du kan skapa IotHub med antingen standard egenskaperna eller ange indata.</span><span class="sxs-lookup"><span data-stu-id="1a789-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="1a789-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a789-108">EXAMPLES</span></span>

### <span data-ttu-id="1a789-109">Exempel 1 Skapa en ny IotHub med standard egenskaper</span><span class="sxs-lookup"><span data-stu-id="1a789-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Tag $tags
```

<span data-ttu-id="1a789-110">Skapar en ny IotHub med namnet "myiothub" för SKU: n "S1", Capacity 1 och location "northeurope" med taggar.</span><span class="sxs-lookup"><span data-stu-id="1a789-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" included with Tags.</span></span>

### <span data-ttu-id="1a789-111">Exempel 2 Skapa en ny IotHub med MaxDeliveryCount för CloudToDevice-kön inställd på 20</span><span class="sxs-lookup"><span data-stu-id="1a789-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="1a789-112">Skapar en ny IotHub med namnet "myiothub" för SKU: n "S1", Capacity 1 och location "northeurope" med avancerade egenskaper som representeras av $properties.</span><span class="sxs-lookup"><span data-stu-id="1a789-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="1a789-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. kommandona Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-name "myiothub"-SkuName "S1"-enheter 1-location "northeurope"-egenskaper $properties</span><span class="sxs-lookup"><span data-stu-id="1a789-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="1a789-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a789-114">PARAMETERS</span></span>

### <span data-ttu-id="1a789-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a789-115">-DefaultProfile</span></span>
<span data-ttu-id="1a789-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1a789-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a789-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="1a789-117">-Location</span></span>
<span data-ttu-id="1a789-118">Plats där IoT Hub måste skapas.</span><span class="sxs-lookup"><span data-stu-id="1a789-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a789-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a789-119">-Name</span></span>
<span data-ttu-id="1a789-120">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="1a789-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="1a789-121">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="1a789-121">-Properties</span></span>
<span data-ttu-id="1a789-122">Egenskaper för IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="1a789-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a789-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a789-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a789-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1a789-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1a789-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1a789-125">-SkuName</span></span>
<span data-ttu-id="1a789-126">Namn på SKU</span><span class="sxs-lookup"><span data-stu-id="1a789-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a789-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1a789-127">-Tag</span></span>
<span data-ttu-id="1a789-128">IoT Hub instance-taggar.</span><span class="sxs-lookup"><span data-stu-id="1a789-128">IoT hub instance tags.</span></span> <span data-ttu-id="1a789-129">Egenskaps uppsättning i nyckel värde par i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1a789-129">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="1a789-130">-Enheter</span><span class="sxs-lookup"><span data-stu-id="1a789-130">-Units</span></span>
<span data-ttu-id="1a789-131">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="1a789-131">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a789-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1a789-132">-Confirm</span></span>
<span data-ttu-id="1a789-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1a789-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a789-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a789-134">-WhatIf</span></span>
<span data-ttu-id="1a789-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1a789-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a789-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1a789-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a789-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a789-137">CommonParameters</span></span>
<span data-ttu-id="1a789-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a789-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a789-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a789-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a789-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a789-140">INPUTS</span></span>

### <span data-ttu-id="1a789-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1a789-141">System.String</span></span>

## <span data-ttu-id="1a789-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a789-142">OUTPUTS</span></span>

### <span data-ttu-id="1a789-143">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1a789-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="1a789-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a789-144">NOTES</span></span>

## <span data-ttu-id="1a789-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a789-145">RELATED LINKS</span></span>
