---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573392"
---
# <span data-ttu-id="620d3-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="620d3-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="620d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="620d3-102">SYNOPSIS</span></span>
<span data-ttu-id="620d3-103">Testar förekomsten av en instans av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="620d3-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="620d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="620d3-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="620d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="620d3-105">DESCRIPTION</span></span>
<span data-ttu-id="620d3-106">Test-AzureRmPowerBIEmbeddedCapacity-cmdleten testar förekomsten av en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="620d3-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="620d3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="620d3-107">EXAMPLES</span></span>

### <span data-ttu-id="620d3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="620d3-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="620d3-109">Det här kommandot kontrollerar om det finns en kapacitet som heter testcapacity</span><span class="sxs-lookup"><span data-stu-id="620d3-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="620d3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="620d3-110">PARAMETERS</span></span>

### <span data-ttu-id="620d3-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="620d3-111">-Name</span></span>
<span data-ttu-id="620d3-112">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="620d3-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="620d3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620d3-113">CommonParameters</span></span>
<span data-ttu-id="620d3-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620d3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620d3-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620d3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620d3-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="620d3-116">INPUTS</span></span>

### <span data-ttu-id="620d3-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="620d3-117">None</span></span>
<span data-ttu-id="620d3-118">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="620d3-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="620d3-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="620d3-119">OUTPUTS</span></span>

### <span data-ttu-id="620d3-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="620d3-120">System.Boolean</span></span>

## <span data-ttu-id="620d3-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="620d3-121">NOTES</span></span>

## <span data-ttu-id="620d3-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="620d3-122">RELATED LINKS</span></span>

[<span data-ttu-id="620d3-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="620d3-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="620d3-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="620d3-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
