---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 769cb913c04c435071c6b743f0d3de533128986f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584804"
---
# <span data-ttu-id="e8a15-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8a15-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e8a15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8a15-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a15-103">Hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e8a15-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8a15-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8a15-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a15-106">Cmdleten **Get-AzureRmAvailabilitySet** hämtar Azure Availability-uppsättningar i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e8a15-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="e8a15-107">Du kan ange namnet på en specifik tillgänglighets uppsättning som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="e8a15-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="e8a15-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8a15-108">EXAMPLES</span></span>

### <span data-ttu-id="e8a15-109">Exempel 1: skaffa en specifik tillgänglighets uppsättning</span><span class="sxs-lookup"><span data-stu-id="e8a15-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="e8a15-110">Det här kommandot får tillgänglighets uppsättningen som heter AvailablitySet03 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e8a15-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="e8a15-111">Exempel 2: Hämta alla tillgänglighets uppsättningar</span><span class="sxs-lookup"><span data-stu-id="e8a15-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e8a15-112">Det här kommandot får alla tillgänglighets uppsättningar i resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="e8a15-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e8a15-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8a15-113">PARAMETERS</span></span>

### <span data-ttu-id="e8a15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a15-114">-DefaultProfile</span></span>
<span data-ttu-id="e8a15-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a15-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8a15-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8a15-116">-Name</span></span>
<span data-ttu-id="e8a15-117">Anger namnet på en tillgänglighets uppsättning som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e8a15-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a15-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a15-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8a15-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e8a15-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e8a15-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a15-120">CommonParameters</span></span>
<span data-ttu-id="e8a15-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a15-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a15-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8a15-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a15-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8a15-123">INPUTS</span></span>

## <span data-ttu-id="e8a15-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8a15-124">OUTPUTS</span></span>

## <span data-ttu-id="e8a15-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8a15-125">NOTES</span></span>

## <span data-ttu-id="e8a15-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8a15-126">RELATED LINKS</span></span>

[<span data-ttu-id="e8a15-127">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8a15-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e8a15-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e8a15-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


