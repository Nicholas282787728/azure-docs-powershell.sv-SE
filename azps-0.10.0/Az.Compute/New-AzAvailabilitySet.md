---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925097"
---
# <span data-ttu-id="ad361-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad361-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="ad361-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad361-102">SYNOPSIS</span></span>
<span data-ttu-id="ad361-103">Skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="ad361-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="ad361-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad361-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad361-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad361-105">DESCRIPTION</span></span>
<span data-ttu-id="ad361-106">Cmdleten **New-AzAvailabilitySet** skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="ad361-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="ad361-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad361-107">EXAMPLES</span></span>

### <span data-ttu-id="ad361-108">Exempel 1: skapa en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="ad361-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="ad361-109">Det här kommandot skapar en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad361-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ad361-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad361-110">PARAMETERS</span></span>

### <span data-ttu-id="ad361-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad361-111">-AsJob</span></span>
<span data-ttu-id="ad361-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ad361-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad361-113">-DefaultProfile</span></span>
<span data-ttu-id="ad361-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad361-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad361-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="ad361-115">-Location</span></span>
<span data-ttu-id="ad361-116">Anger platsen för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ad361-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-117">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="ad361-117">-Managed</span></span>
<span data-ttu-id="ad361-118">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="ad361-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad361-119">-Name</span></span>
<span data-ttu-id="ad361-120">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ad361-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="ad361-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="ad361-122">Anger antalet plattformar för Platform Fault.</span><span class="sxs-lookup"><span data-stu-id="ad361-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="ad361-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="ad361-124">Anger antalet plattformar för plattforms uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="ad361-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad361-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad361-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ad361-126">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="ad361-127">-Sku</span></span>
<span data-ttu-id="ad361-128">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="ad361-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad361-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad361-129">CommonParameters</span></span>
<span data-ttu-id="ad361-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad361-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad361-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad361-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad361-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad361-132">INPUTS</span></span>

### <span data-ttu-id="ad361-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="ad361-133">None</span></span>
<span data-ttu-id="ad361-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ad361-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad361-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad361-135">OUTPUTS</span></span>

### <span data-ttu-id="ad361-136">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad361-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ad361-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad361-137">NOTES</span></span>

## <span data-ttu-id="ad361-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad361-138">RELATED LINKS</span></span>

[<span data-ttu-id="ad361-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad361-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="ad361-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ad361-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


