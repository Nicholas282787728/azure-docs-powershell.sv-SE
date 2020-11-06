---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5bf4f178ee3343b5100dad87836c3215fba4cfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582568"
---
# <span data-ttu-id="91f78-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="91f78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91f78-102">SYNOPSIS</span></span>
<span data-ttu-id="91f78-103">Uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="91f78-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91f78-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91f78-105">DESCRIPTION</span></span>
<span data-ttu-id="91f78-106">Cmdleten **set-AzureRmOperationalInsightsDataSource** uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="91f78-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="91f78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91f78-107">EXAMPLES</span></span>

## <span data-ttu-id="91f78-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91f78-108">PARAMETERS</span></span>

### <span data-ttu-id="91f78-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-109">-DataSource</span></span>
<span data-ttu-id="91f78-110">Anger den data källa som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="91f78-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f78-111">-DefaultProfile</span></span>
<span data-ttu-id="91f78-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="91f78-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f78-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f78-113">CommonParameters</span></span>
<span data-ttu-id="91f78-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f78-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f78-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f78-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f78-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91f78-116">INPUTS</span></span>

### <span data-ttu-id="91f78-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>
<span data-ttu-id="91f78-118">Parametrar: DataSource (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91f78-118">Parameters: DataSource (ByValue)</span></span>

## <span data-ttu-id="91f78-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91f78-119">OUTPUTS</span></span>

### <span data-ttu-id="91f78-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="91f78-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91f78-121">NOTES</span></span>
* <span data-ttu-id="91f78-122">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="91f78-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="91f78-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91f78-123">RELATED LINKS</span></span>

[<span data-ttu-id="91f78-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="91f78-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="91f78-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


