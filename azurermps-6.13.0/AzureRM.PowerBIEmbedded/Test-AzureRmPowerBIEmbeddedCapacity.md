---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756140"
---
# <span data-ttu-id="b100c-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b100c-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b100c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b100c-102">SYNOPSIS</span></span>
<span data-ttu-id="b100c-103">Testar förekomsten av en instans av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="b100c-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b100c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b100c-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b100c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b100c-105">DESCRIPTION</span></span>
<span data-ttu-id="b100c-106">Test-AzureRmPowerBIEmbeddedCapacity-cmdleten testar förekomsten av en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="b100c-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="b100c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b100c-107">EXAMPLES</span></span>

### <span data-ttu-id="b100c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b100c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="b100c-109">Det här kommandot kontrollerar om det finns en kapacitet som heter testcapacity</span><span class="sxs-lookup"><span data-stu-id="b100c-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="b100c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b100c-110">PARAMETERS</span></span>

### <span data-ttu-id="b100c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b100c-111">-DefaultProfile</span></span>
<span data-ttu-id="b100c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b100c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b100c-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b100c-113">-Name</span></span>
<span data-ttu-id="b100c-114">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="b100c-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b100c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b100c-115">CommonParameters</span></span>
<span data-ttu-id="b100c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b100c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b100c-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b100c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b100c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b100c-118">INPUTS</span></span>

### <span data-ttu-id="b100c-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="b100c-119">None</span></span>

## <span data-ttu-id="b100c-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b100c-120">OUTPUTS</span></span>

### <span data-ttu-id="b100c-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b100c-121">System.Boolean</span></span>

## <span data-ttu-id="b100c-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b100c-122">NOTES</span></span>

## <span data-ttu-id="b100c-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b100c-123">RELATED LINKS</span></span>

[<span data-ttu-id="b100c-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b100c-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b100c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b100c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
