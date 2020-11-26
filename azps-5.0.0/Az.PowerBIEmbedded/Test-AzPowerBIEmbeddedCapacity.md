---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272405"
---
# <span data-ttu-id="3cb9d-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3cb9d-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3cb9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb9d-103">Testar förekomsten av en instans av en PowerBI inbäddad kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3cb9d-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3cb9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cb9d-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb9d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cb9d-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb9d-106">Test-AzPowerBIEmbeddedCapacity-cmdleten testar förekomsten av en instans av PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="3cb9d-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3cb9d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cb9d-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb9d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cb9d-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="3cb9d-109">Det här kommandot kontrollerar om det finns en kapacitet som heter testcapacity</span><span class="sxs-lookup"><span data-stu-id="3cb9d-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="3cb9d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cb9d-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb9d-111">-DefaultProfile</span></span>
<span data-ttu-id="3cb9d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cb9d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cb9d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="3cb9d-113">-Name</span></span>
<span data-ttu-id="3cb9d-114">Namnet på PowerBI inbäddade kapacitet</span><span class="sxs-lookup"><span data-stu-id="3cb9d-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3cb9d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb9d-115">CommonParameters</span></span>
<span data-ttu-id="3cb9d-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb9d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb9d-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb9d-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb9d-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cb9d-118">INPUTS</span></span>

### <span data-ttu-id="3cb9d-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="3cb9d-119">None</span></span>

## <span data-ttu-id="3cb9d-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cb9d-120">OUTPUTS</span></span>

### <span data-ttu-id="3cb9d-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cb9d-121">System.Boolean</span></span>

## <span data-ttu-id="3cb9d-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cb9d-122">NOTES</span></span>

## <span data-ttu-id="3cb9d-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cb9d-123">RELATED LINKS</span></span>

[<span data-ttu-id="3cb9d-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3cb9d-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3cb9d-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3cb9d-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)