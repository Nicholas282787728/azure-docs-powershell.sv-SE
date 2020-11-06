---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586208"
---
# <span data-ttu-id="f2ba8-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ba8-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="f2ba8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ba8-103">Skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ba8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2ba8-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ba8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ba8-106">Cmdleten **New-AzureRmAvailabilitySet** skapar en Azure Availability-uppsättning.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="f2ba8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ba8-108">Exempel 1: skapa en tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="f2ba8-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="f2ba8-109">Det här kommandot skapar en tillgänglighets uppsättning med namnet AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f2ba8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2ba8-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ba8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ba8-111">-DefaultProfile</span></span>
<span data-ttu-id="f2ba8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ba8-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="f2ba8-113">-Location</span></span>
<span data-ttu-id="f2ba8-114">Anger platsen för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-114">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="f2ba8-115">-Hanteras</span><span class="sxs-lookup"><span data-stu-id="f2ba8-115">-Managed</span></span>
<span data-ttu-id="f2ba8-116">Hanterad tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="f2ba8-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2ba8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2ba8-117">-Name</span></span>
<span data-ttu-id="f2ba8-118">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f2ba8-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="f2ba8-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="f2ba8-120">Anger antalet plattformar för Platform Fault.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="f2ba8-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="f2ba8-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="f2ba8-122">Anger antalet plattformar för plattforms uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="f2ba8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ba8-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2ba8-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f2ba8-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2ba8-125">-Sku</span></span>
<span data-ttu-id="f2ba8-126">Namnet på SKU</span><span class="sxs-lookup"><span data-stu-id="f2ba8-126">The Name of Sku</span></span>
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

### <span data-ttu-id="f2ba8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ba8-127">CommonParameters</span></span>
<span data-ttu-id="f2ba8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ba8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ba8-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ba8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ba8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2ba8-130">INPUTS</span></span>

## <span data-ttu-id="f2ba8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2ba8-131">OUTPUTS</span></span>

## <span data-ttu-id="f2ba8-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2ba8-132">NOTES</span></span>

## <span data-ttu-id="f2ba8-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2ba8-133">RELATED LINKS</span></span>

[<span data-ttu-id="f2ba8-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ba8-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f2ba8-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f2ba8-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


