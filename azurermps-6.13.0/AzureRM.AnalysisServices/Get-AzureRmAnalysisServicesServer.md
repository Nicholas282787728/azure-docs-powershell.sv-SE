---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576359"
---
# <span data-ttu-id="d20ae-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d20ae-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="d20ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d20ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d20ae-103">Hämtar information om en Analysis Services-server.</span><span class="sxs-lookup"><span data-stu-id="d20ae-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d20ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d20ae-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d20ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d20ae-105">DESCRIPTION</span></span>
<span data-ttu-id="d20ae-106">Get-AzureRmAnalysisServicesServer cmdlet får information om en Analysis Services-server.</span><span class="sxs-lookup"><span data-stu-id="d20ae-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="d20ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d20ae-107">EXAMPLES</span></span>

### <span data-ttu-id="d20ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d20ae-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="d20ae-109">Det här kommandot får alla Azure Analysis Services-servrar i resurs gruppen "ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d20ae-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="d20ae-110">Exempel 2: skaffa en server</span><span class="sxs-lookup"><span data-stu-id="d20ae-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="d20ae-111">Det här kommandot får Azure Analysis Services-servern med namnet testserver i resurs gruppen med namnet ResourceGroup03.</span><span class="sxs-lookup"><span data-stu-id="d20ae-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="d20ae-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d20ae-112">PARAMETERS</span></span>

### <span data-ttu-id="d20ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20ae-113">-DefaultProfile</span></span>
<span data-ttu-id="d20ae-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d20ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d20ae-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d20ae-115">-Name</span></span>
<span data-ttu-id="d20ae-116">Namn på Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="d20ae-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d20ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="d20ae-118">Namn på den Azure-adressresurs som servern tillhör</span><span class="sxs-lookup"><span data-stu-id="d20ae-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20ae-119">CommonParameters</span></span>
<span data-ttu-id="d20ae-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20ae-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20ae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20ae-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d20ae-122">INPUTS</span></span>

### <span data-ttu-id="d20ae-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d20ae-123">System.String</span></span>

## <span data-ttu-id="d20ae-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d20ae-124">OUTPUTS</span></span>

### <span data-ttu-id="d20ae-125">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d20ae-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d20ae-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d20ae-126">NOTES</span></span>
<span data-ttu-id="d20ae-127">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="d20ae-127">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="d20ae-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d20ae-128">RELATED LINKS</span></span>

[<span data-ttu-id="d20ae-129">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d20ae-129">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="d20ae-130">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="d20ae-130">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)