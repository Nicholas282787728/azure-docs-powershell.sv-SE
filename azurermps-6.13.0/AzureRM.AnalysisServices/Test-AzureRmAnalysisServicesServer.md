---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 7f47d800fd0eab51edae321f9d21260f50075b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576356"
---
# <span data-ttu-id="181f8-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="181f8-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="181f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="181f8-102">SYNOPSIS</span></span>
<span data-ttu-id="181f8-103">Testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="181f8-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="181f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="181f8-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="181f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="181f8-105">DESCRIPTION</span></span>
<span data-ttu-id="181f8-106">Test-AzureRmAnalysisServicesServer-cmdleten testar förekomsten av en instans av Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="181f8-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="181f8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="181f8-107">EXAMPLES</span></span>

### <span data-ttu-id="181f8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="181f8-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="181f8-109">Det här kommandot testar om det finns en server med namnet testserver i resourcegroup testgroup</span><span class="sxs-lookup"><span data-stu-id="181f8-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="181f8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="181f8-110">PARAMETERS</span></span>

### <span data-ttu-id="181f8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181f8-111">-DefaultProfile</span></span>
<span data-ttu-id="181f8-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="181f8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="181f8-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="181f8-113">-Name</span></span>
<span data-ttu-id="181f8-114">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="181f8-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="181f8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181f8-115">-ResourceGroupName</span></span>
<span data-ttu-id="181f8-116">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="181f8-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="181f8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181f8-117">CommonParameters</span></span>
<span data-ttu-id="181f8-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181f8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181f8-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181f8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181f8-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="181f8-120">INPUTS</span></span>

### <span data-ttu-id="181f8-121">System. String</span><span class="sxs-lookup"><span data-stu-id="181f8-121">System.String</span></span>

## <span data-ttu-id="181f8-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="181f8-122">OUTPUTS</span></span>

### <span data-ttu-id="181f8-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="181f8-123">System.Boolean</span></span>

## <span data-ttu-id="181f8-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="181f8-124">NOTES</span></span>
<span data-ttu-id="181f8-125">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="181f8-125">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="181f8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="181f8-126">RELATED LINKS</span></span>

[<span data-ttu-id="181f8-127">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="181f8-127">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="181f8-128">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="181f8-128">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
