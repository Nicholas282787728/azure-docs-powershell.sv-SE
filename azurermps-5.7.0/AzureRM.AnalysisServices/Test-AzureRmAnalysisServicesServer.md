---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585227"
---
# <span data-ttu-id="b20d5-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b20d5-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b20d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b20d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b20d5-103">Testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="b20d5-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b20d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b20d5-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b20d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b20d5-105">DESCRIPTION</span></span>
<span data-ttu-id="b20d5-106">Test-AzureRmAnalysisServicesServer-cmdleten testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="b20d5-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="b20d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b20d5-107">EXAMPLES</span></span>

### <span data-ttu-id="b20d5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b20d5-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="b20d5-109">Det här kommandot testar om det finns en server med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="b20d5-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="b20d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b20d5-110">PARAMETERS</span></span>

### <span data-ttu-id="b20d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b20d5-111">-DefaultProfile</span></span>
<span data-ttu-id="b20d5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b20d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b20d5-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="b20d5-113">-Name</span></span>
<span data-ttu-id="b20d5-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="b20d5-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b20d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b20d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="b20d5-116">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="b20d5-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b20d5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20d5-117">CommonParameters</span></span>
<span data-ttu-id="b20d5-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b20d5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20d5-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b20d5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20d5-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b20d5-120">INPUTS</span></span>

### <span data-ttu-id="b20d5-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="b20d5-121">None</span></span>
<span data-ttu-id="b20d5-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b20d5-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b20d5-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b20d5-123">OUTPUTS</span></span>

### <span data-ttu-id="b20d5-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b20d5-124">System.Boolean</span></span>

## <span data-ttu-id="b20d5-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b20d5-125">NOTES</span></span>
<span data-ttu-id="b20d5-126">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b20d5-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="b20d5-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b20d5-127">RELATED LINKS</span></span>

[<span data-ttu-id="b20d5-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b20d5-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="b20d5-129">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b20d5-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
