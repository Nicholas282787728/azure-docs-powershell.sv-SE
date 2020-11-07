---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925253"
---
# <span data-ttu-id="827f0-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827f0-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="827f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="827f0-102">SYNOPSIS</span></span>
<span data-ttu-id="827f0-103">Hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="827f0-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="827f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="827f0-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="827f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="827f0-105">DESCRIPTION</span></span>
<span data-ttu-id="827f0-106">Cmdleten **Get-AzAvailabilitySet** hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="827f0-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="827f0-107">Du kan ange namnet på en specifik tillgänglighets uppsättning som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="827f0-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="827f0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="827f0-108">EXAMPLES</span></span>

### <span data-ttu-id="827f0-109">Exempel 1: skaffa en specifik tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="827f0-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="827f0-110">Det här kommandot får tillgänglighets uppsättningen som heter AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="827f0-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="827f0-111">Exempel 2: Hämta alla tillgänglighets uppsättningar</span><span class="sxs-lookup"><span data-stu-id="827f0-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="827f0-112">Det här kommandot får alla tillgänglighets uppsättningar i resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="827f0-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="827f0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="827f0-113">PARAMETERS</span></span>

### <span data-ttu-id="827f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827f0-114">-DefaultProfile</span></span>
<span data-ttu-id="827f0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="827f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="827f0-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="827f0-116">-Name</span></span>
<span data-ttu-id="827f0-117">Anger namnet på en tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="827f0-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="827f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="827f0-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="827f0-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="827f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827f0-120">CommonParameters</span></span>
<span data-ttu-id="827f0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="827f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827f0-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="827f0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827f0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="827f0-123">INPUTS</span></span>

### <span data-ttu-id="827f0-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="827f0-124">None</span></span>
<span data-ttu-id="827f0-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="827f0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="827f0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="827f0-126">OUTPUTS</span></span>

### <span data-ttu-id="827f0-127">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827f0-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="827f0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="827f0-128">NOTES</span></span>

## <span data-ttu-id="827f0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="827f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="827f0-130">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827f0-130">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="827f0-131">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="827f0-131">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


