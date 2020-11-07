---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 7298612cf64b4f90f65ebaa2943b38102b5ae1ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743444"
---
# <span data-ttu-id="c9b85-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9b85-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="c9b85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9b85-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b85-103">Testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9b85-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="c9b85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9b85-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9b85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9b85-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b85-106">Test-AzAnalysisServicesServer-cmdleten testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9b85-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="c9b85-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9b85-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b85-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9b85-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="c9b85-109">Det här kommandot testar om det finns en server med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="c9b85-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="c9b85-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9b85-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b85-111">-DefaultProfile</span></span>
<span data-ttu-id="c9b85-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9b85-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c9b85-113">-Name</span></span>
<span data-ttu-id="c9b85-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="c9b85-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="c9b85-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b85-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9b85-116">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="c9b85-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b85-117">CommonParameters</span></span>
<span data-ttu-id="c9b85-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b85-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b85-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b85-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9b85-120">INPUTS</span></span>

### <span data-ttu-id="c9b85-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b85-121">System.String</span></span>

## <span data-ttu-id="c9b85-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9b85-122">OUTPUTS</span></span>

### <span data-ttu-id="c9b85-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9b85-123">System.Boolean</span></span>

## <span data-ttu-id="c9b85-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9b85-124">NOTES</span></span>
<span data-ttu-id="c9b85-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="c9b85-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="c9b85-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9b85-126">RELATED LINKS</span></span>

[<span data-ttu-id="c9b85-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9b85-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="c9b85-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="c9b85-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)