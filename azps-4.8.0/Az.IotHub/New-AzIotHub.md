---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: ad9c032a4384a82e03704529796a209e8c88f4c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262639"
---
# <span data-ttu-id="dfbca-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="dfbca-101">New-AzIotHub</span></span>

## <span data-ttu-id="dfbca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfbca-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbca-103">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="dfbca-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="dfbca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfbca-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfbca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfbca-105">DESCRIPTION</span></span>
<span data-ttu-id="dfbca-106">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="dfbca-106">Creates a new IotHub.</span></span>
<span data-ttu-id="dfbca-107">Du kan skapa IotHub med antingen standard egenskaperna eller ange indata.</span><span class="sxs-lookup"><span data-stu-id="dfbca-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="dfbca-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfbca-108">EXAMPLES</span></span>

### <span data-ttu-id="dfbca-109">Exempel 1 Skapa en ny IotHub med standard egenskaper</span><span class="sxs-lookup"><span data-stu-id="dfbca-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="dfbca-110">Skapar en ny IotHub med namnet "myiothub" för SKU "S1", Capacity 1 och location "northeurope".</span><span class="sxs-lookup"><span data-stu-id="dfbca-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="dfbca-111">Exempel 2 Skapa en ny IotHub med MaxDeliveryCount för CloudToDevice-kön inställd på 20</span><span class="sxs-lookup"><span data-stu-id="dfbca-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="dfbca-112">Skapar en ny IotHub med namnet "myiothub" för SKU: n "S1", Capacity 1 och location "northeurope" med avancerade egenskaper som representeras av $properties.</span><span class="sxs-lookup"><span data-stu-id="dfbca-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="dfbca-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. kommandona Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-name "myiothub"-SkuName "S1"-enheter 1-location "northeurope"-egenskaper $properties</span><span class="sxs-lookup"><span data-stu-id="dfbca-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="dfbca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfbca-114">PARAMETERS</span></span>

### <span data-ttu-id="dfbca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbca-115">-DefaultProfile</span></span>
<span data-ttu-id="dfbca-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dfbca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfbca-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="dfbca-117">-Location</span></span>
<span data-ttu-id="dfbca-118">Plats där IoT Hub måste skapas.</span><span class="sxs-lookup"><span data-stu-id="dfbca-118">Location where the IoT hub needs to be created.</span></span> 

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

### <span data-ttu-id="dfbca-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfbca-119">-Name</span></span>
<span data-ttu-id="dfbca-120">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="dfbca-120">Name of the IotHub</span></span>

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

### <span data-ttu-id="dfbca-121">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="dfbca-121">-Properties</span></span>
<span data-ttu-id="dfbca-122">Egenskaper för IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="dfbca-122">Properties of the IoT hub.</span></span> 

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

### <span data-ttu-id="dfbca-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbca-123">-ResourceGroupName</span></span>
<span data-ttu-id="dfbca-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dfbca-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dfbca-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dfbca-125">-SkuName</span></span>
<span data-ttu-id="dfbca-126">Namn på SKU</span><span class="sxs-lookup"><span data-stu-id="dfbca-126">Name of the sku</span></span>

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

### <span data-ttu-id="dfbca-127">-Enheter</span><span class="sxs-lookup"><span data-stu-id="dfbca-127">-Units</span></span>
<span data-ttu-id="dfbca-128">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="dfbca-128">Number of units</span></span>

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

### <span data-ttu-id="dfbca-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dfbca-129">-Confirm</span></span>
<span data-ttu-id="dfbca-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dfbca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbca-131">-WhatIf</span></span>
<span data-ttu-id="dfbca-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dfbca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbca-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dfbca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbca-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbca-134">CommonParameters</span></span>
<span data-ttu-id="dfbca-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbca-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbca-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbca-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbca-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfbca-137">INPUTS</span></span>

### <span data-ttu-id="dfbca-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dfbca-138">System.String</span></span>

## <span data-ttu-id="dfbca-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfbca-139">OUTPUTS</span></span>

### <span data-ttu-id="dfbca-140">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dfbca-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="dfbca-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfbca-141">NOTES</span></span>

## <span data-ttu-id="dfbca-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfbca-142">RELATED LINKS</span></span>