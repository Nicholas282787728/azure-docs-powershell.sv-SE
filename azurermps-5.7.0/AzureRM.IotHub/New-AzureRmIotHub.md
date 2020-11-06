---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: c24f8f9e95db65b464da6586d9e3499358fc3edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584332"
---
# <span data-ttu-id="e2d14-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="e2d14-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="e2d14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2d14-102">SYNOPSIS</span></span>
<span data-ttu-id="e2d14-103">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="e2d14-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2d14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2d14-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2d14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2d14-105">DESCRIPTION</span></span>
<span data-ttu-id="e2d14-106">Skapar en ny IotHub.</span><span class="sxs-lookup"><span data-stu-id="e2d14-106">Creates a new IotHub.</span></span>
<span data-ttu-id="e2d14-107">Du kan skapa IotHub med antingen standard egenskaperna eller ange indata-Proerties.</span><span class="sxs-lookup"><span data-stu-id="e2d14-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="e2d14-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2d14-108">EXAMPLES</span></span>

### <span data-ttu-id="e2d14-109">Exempel 1 Skapa en ny IotHub med standard egenskaper</span><span class="sxs-lookup"><span data-stu-id="e2d14-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="e2d14-110">Skapar en ny IotHub med namnet "myiothub" för SKU "S1", Capacity 1 och location "northeurope".</span><span class="sxs-lookup"><span data-stu-id="e2d14-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="e2d14-111">Exempel 2 Skapa en ny IotHub med MaxDeliveryCount för CloudtoDevice-kön inställd på 20</span><span class="sxs-lookup"><span data-stu-id="e2d14-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="e2d14-112">Skapar en ny IotHub med namnet "myiothub" för SKU: n "S1", Capacity 1 och location "northeurope" med avancerade egenskaper som representeras av $properties.</span><span class="sxs-lookup"><span data-stu-id="e2d14-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="e2d14-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. commands. Management. IotHub. Models. PSCloudToDeviceProperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. kommandona Management. IotHub. Models. PSIotHubInputProperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-name "myiothub"-SkuName "S1"-enheter 1-location "northeurope"-egenskaper $properties</span><span class="sxs-lookup"><span data-stu-id="e2d14-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="e2d14-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2d14-114">PARAMETERS</span></span>

### <span data-ttu-id="e2d14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d14-115">-DefaultProfile</span></span>
<span data-ttu-id="e2d14-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e2d14-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="e2d14-117">-Location</span></span>
<span data-ttu-id="e2d14-118">Plats där IoT Hub måste skapas.</span><span class="sxs-lookup"><span data-stu-id="e2d14-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e2d14-119">-Name</span></span>
<span data-ttu-id="e2d14-120">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="e2d14-120">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-121">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="e2d14-121">-Properties</span></span>
<span data-ttu-id="e2d14-122">Egenskaper för IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e2d14-122">Properties of the IoT hub.</span></span> 

```yaml
Type: PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d14-123">-ResourceGroupName</span></span>
<span data-ttu-id="e2d14-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e2d14-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e2d14-125">-SkuName</span></span>
<span data-ttu-id="e2d14-126">Namn på SKU</span><span class="sxs-lookup"><span data-stu-id="e2d14-126">Name of the sku</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-127">-Enheter</span><span class="sxs-lookup"><span data-stu-id="e2d14-127">-Units</span></span>
<span data-ttu-id="e2d14-128">Antal enheter</span><span class="sxs-lookup"><span data-stu-id="e2d14-128">Number of units</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e2d14-129">-Confirm</span></span>
<span data-ttu-id="e2d14-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e2d14-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2d14-131">-WhatIf</span></span>
<span data-ttu-id="e2d14-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e2d14-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2d14-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e2d14-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d14-134">CommonParameters</span></span>
<span data-ttu-id="e2d14-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2d14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d14-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d14-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d14-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2d14-137">INPUTS</span></span>

### <span data-ttu-id="e2d14-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2d14-138">System.String</span></span>
<span data-ttu-id="e2d14-139">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubSku system. Int64 Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubInputProperties</span><span class="sxs-lookup"><span data-stu-id="e2d14-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="e2d14-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2d14-140">OUTPUTS</span></span>

### <span data-ttu-id="e2d14-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2d14-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e2d14-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2d14-142">NOTES</span></span>

## <span data-ttu-id="e2d14-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2d14-143">RELATED LINKS</span></span>

