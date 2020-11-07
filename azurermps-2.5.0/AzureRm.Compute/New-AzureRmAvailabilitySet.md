---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929114"
---
# <span data-ttu-id="12b31-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="12b31-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="12b31-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12b31-102">SYNOPSIS</span></span>
<span data-ttu-id="12b31-103">Skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="12b31-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b31-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12b31-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12b31-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12b31-105">DESCRIPTION</span></span>
<span data-ttu-id="12b31-106">Cmdleten **New-AzureRmAvailabilitySet** skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="12b31-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="12b31-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12b31-107">EXAMPLES</span></span>

### <span data-ttu-id="12b31-108">Exempel 1: skapa en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="12b31-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="12b31-109">Det här kommandot skapar en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="12b31-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="12b31-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12b31-110">PARAMETERS</span></span>

### <span data-ttu-id="12b31-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12b31-111">-AsJob</span></span>
<span data-ttu-id="12b31-112">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="12b31-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="12b31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b31-113">-DefaultProfile</span></span>
<span data-ttu-id="12b31-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12b31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b31-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="12b31-115">-Location</span></span>
<span data-ttu-id="12b31-116">Anger platsen för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="12b31-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="12b31-117">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="12b31-117">-Managed</span></span>
<span data-ttu-id="12b31-118">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="12b31-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="12b31-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="12b31-119">-Name</span></span>
<span data-ttu-id="12b31-120">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="12b31-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="12b31-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="12b31-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="12b31-122">Anger antalet plattformar för Platform Fault.</span><span class="sxs-lookup"><span data-stu-id="12b31-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="12b31-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="12b31-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="12b31-124">Anger antalet plattformar för plattforms uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="12b31-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="12b31-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b31-125">-ResourceGroupName</span></span>
<span data-ttu-id="12b31-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="12b31-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="12b31-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="12b31-127">-Sku</span></span>
<span data-ttu-id="12b31-128">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="12b31-128">The Name of Sku</span></span>
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

### <span data-ttu-id="12b31-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b31-129">CommonParameters</span></span>
<span data-ttu-id="12b31-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b31-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b31-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b31-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b31-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12b31-132">INPUTS</span></span>

### <span data-ttu-id="12b31-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="12b31-133">None</span></span>
<span data-ttu-id="12b31-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="12b31-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="12b31-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12b31-135">OUTPUTS</span></span>

### <span data-ttu-id="12b31-136">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="12b31-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="12b31-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12b31-137">NOTES</span></span>

## <span data-ttu-id="12b31-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12b31-138">RELATED LINKS</span></span>

[<span data-ttu-id="12b31-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="12b31-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="12b31-140">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="12b31-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


