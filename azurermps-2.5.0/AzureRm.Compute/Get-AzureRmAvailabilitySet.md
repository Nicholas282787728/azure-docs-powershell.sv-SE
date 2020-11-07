---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929118"
---
# <span data-ttu-id="9d18f-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d18f-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="9d18f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d18f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d18f-103">Hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9d18f-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d18f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d18f-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d18f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d18f-105">DESCRIPTION</span></span>
<span data-ttu-id="9d18f-106">Cmdleten **Get-AzureRmAvailabilitySet** hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9d18f-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="9d18f-107">Du kan ange namnet på en specifik tillgänglighets uppsättning som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="9d18f-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="9d18f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d18f-108">EXAMPLES</span></span>

### <span data-ttu-id="9d18f-109">Exempel 1: skaffa en specifik tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="9d18f-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="9d18f-110">Det här kommandot får tillgänglighets uppsättningen som heter AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9d18f-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="9d18f-111">Exempel 2: Hämta alla tillgänglighets uppsättningar</span><span class="sxs-lookup"><span data-stu-id="9d18f-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9d18f-112">Det här kommandot får alla tillgänglighets uppsättningar i resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="9d18f-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9d18f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d18f-113">PARAMETERS</span></span>

### <span data-ttu-id="9d18f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d18f-114">-DefaultProfile</span></span>
<span data-ttu-id="9d18f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d18f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d18f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d18f-116">-Name</span></span>
<span data-ttu-id="9d18f-117">Anger namnet på en tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="9d18f-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d18f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d18f-118">-ResourceGroupName</span></span>
<span data-ttu-id="9d18f-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9d18f-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d18f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d18f-120">CommonParameters</span></span>
<span data-ttu-id="9d18f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d18f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d18f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d18f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d18f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d18f-123">INPUTS</span></span>

### <span data-ttu-id="9d18f-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="9d18f-124">None</span></span>
<span data-ttu-id="9d18f-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9d18f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d18f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d18f-126">OUTPUTS</span></span>

### <span data-ttu-id="9d18f-127">Microsoft. Azure. commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d18f-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="9d18f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d18f-128">NOTES</span></span>

## <span data-ttu-id="9d18f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d18f-129">RELATED LINKS</span></span>

[<span data-ttu-id="9d18f-130">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d18f-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="9d18f-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9d18f-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


