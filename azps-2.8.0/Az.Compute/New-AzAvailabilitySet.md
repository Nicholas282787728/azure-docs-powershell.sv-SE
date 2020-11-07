---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 50aef7afbd90580bfbae34c9131353fcf29bf2f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745118"
---
# <span data-ttu-id="341ce-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="341ce-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="341ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="341ce-102">SYNOPSIS</span></span>
<span data-ttu-id="341ce-103">Skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="341ce-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="341ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="341ce-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="341ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="341ce-105">DESCRIPTION</span></span>
<span data-ttu-id="341ce-106">Cmdleten **New-AzAvailabilitySet** skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="341ce-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="341ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="341ce-107">EXAMPLES</span></span>

### <span data-ttu-id="341ce-108">Exempel 1: skapa en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="341ce-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="341ce-109">Det här kommandot skapar en tillgänglighets uppsättning med namnet AvailabilitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="341ce-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="341ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="341ce-110">PARAMETERS</span></span>

### <span data-ttu-id="341ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="341ce-111">-AsJob</span></span>
<span data-ttu-id="341ce-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="341ce-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="341ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341ce-113">-DefaultProfile</span></span>
<span data-ttu-id="341ce-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="341ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="341ce-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="341ce-115">-Location</span></span>
<span data-ttu-id="341ce-116">Anger platsen för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="341ce-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="341ce-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="341ce-117">-Name</span></span>
<span data-ttu-id="341ce-118">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="341ce-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="341ce-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="341ce-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="341ce-120">Anger antalet plattformar för Platform Fault.</span><span class="sxs-lookup"><span data-stu-id="341ce-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="341ce-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="341ce-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="341ce-122">Anger antalet plattformar för plattforms uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="341ce-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="341ce-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="341ce-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="341ce-124">ID för ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="341ce-124">The Id of ProximityPlacementGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="341ce-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="341ce-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="341ce-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="341ce-127">-Sku</span></span>
<span data-ttu-id="341ce-128">SKU-namnet.</span><span class="sxs-lookup"><span data-stu-id="341ce-128">The Name of Sku.</span></span>
<span data-ttu-id="341ce-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="341ce-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="341ce-130">Justerad: för hanterade diskar</span><span class="sxs-lookup"><span data-stu-id="341ce-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="341ce-131">Klassisk: för ohanterade diskar</span><span class="sxs-lookup"><span data-stu-id="341ce-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="341ce-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="341ce-132">-Tag</span></span>
<span data-ttu-id="341ce-133">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="341ce-133">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="341ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341ce-134">CommonParameters</span></span>
<span data-ttu-id="341ce-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="341ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341ce-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="341ce-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341ce-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="341ce-137">INPUTS</span></span>

### <span data-ttu-id="341ce-138">System. String</span><span class="sxs-lookup"><span data-stu-id="341ce-138">System.String</span></span>

### <span data-ttu-id="341ce-139">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="341ce-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="341ce-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="341ce-140">OUTPUTS</span></span>

### <span data-ttu-id="341ce-141">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="341ce-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="341ce-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="341ce-142">NOTES</span></span>

## <span data-ttu-id="341ce-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="341ce-143">RELATED LINKS</span></span>

[<span data-ttu-id="341ce-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="341ce-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="341ce-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="341ce-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


