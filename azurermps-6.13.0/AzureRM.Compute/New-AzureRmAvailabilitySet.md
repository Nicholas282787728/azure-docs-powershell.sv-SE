---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757387"
---
# <span data-ttu-id="fe2a9-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe2a9-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="fe2a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2a9-103">Skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe2a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe2a9-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe2a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe2a9-106">Cmdleten **New-AzureRmAvailabilitySet** skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="fe2a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe2a9-107">EXAMPLES</span></span>

### <span data-ttu-id="fe2a9-108">Exempel 1: skapa en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="fe2a9-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="fe2a9-109">Det här kommandot skapar en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="fe2a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe2a9-110">PARAMETERS</span></span>

### <span data-ttu-id="fe2a9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe2a9-111">-AsJob</span></span>
<span data-ttu-id="fe2a9-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fe2a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2a9-113">-DefaultProfile</span></span>
<span data-ttu-id="fe2a9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe2a9-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe2a9-115">-Location</span></span>
<span data-ttu-id="fe2a9-116">Anger platsen för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2a9-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="fe2a9-117">-Name</span></span>
<span data-ttu-id="fe2a9-118">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2a9-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fe2a9-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fe2a9-120">Anger antalet plattformar för Platform Fault.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2a9-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="fe2a9-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="fe2a9-122">Anger antalet plattformar för plattforms uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe2a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe2a9-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fe2a9-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe2a9-125">-Sku</span></span>
<span data-ttu-id="fe2a9-126">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-126">The Name of Sku.</span></span>
<span data-ttu-id="fe2a9-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="fe2a9-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe2a9-128">Justerad: för hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="fe2a9-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="fe2a9-129">Klassisk: för ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="fe2a9-129">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2a9-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fe2a9-130">-Tag</span></span>
<span data-ttu-id="fe2a9-131">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="fe2a9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2a9-132">CommonParameters</span></span>
<span data-ttu-id="fe2a9-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2a9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2a9-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2a9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2a9-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe2a9-135">INPUTS</span></span>

### <span data-ttu-id="fe2a9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fe2a9-136">System.String</span></span>

### <span data-ttu-id="fe2a9-137">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fe2a9-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fe2a9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe2a9-138">OUTPUTS</span></span>

### <span data-ttu-id="fe2a9-139">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe2a9-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="fe2a9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe2a9-140">NOTES</span></span>

## <span data-ttu-id="fe2a9-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe2a9-141">RELATED LINKS</span></span>

[<span data-ttu-id="fe2a9-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe2a9-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="fe2a9-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="fe2a9-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


