---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417688"
---
# <span data-ttu-id="b93bd-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="b93bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b93bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b93bd-103">Uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="b93bd-103">Updates a data source.</span></span>

## <span data-ttu-id="b93bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b93bd-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b93bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b93bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b93bd-106">Cmdleten **set-AzOperationalInsightsDataSource** uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="b93bd-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="b93bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b93bd-107">EXAMPLES</span></span>

## <span data-ttu-id="b93bd-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b93bd-108">PARAMETERS</span></span>

### <span data-ttu-id="b93bd-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-109">-DataSource</span></span>
<span data-ttu-id="b93bd-110">Anger den data källa som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="b93bd-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b93bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93bd-111">-DefaultProfile</span></span>
<span data-ttu-id="b93bd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b93bd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b93bd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93bd-113">CommonParameters</span></span>
<span data-ttu-id="b93bd-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b93bd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93bd-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b93bd-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93bd-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b93bd-116">INPUTS</span></span>

### <span data-ttu-id="b93bd-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b93bd-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b93bd-118">OUTPUTS</span></span>

### <span data-ttu-id="b93bd-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b93bd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b93bd-120">NOTES</span></span>
* <span data-ttu-id="b93bd-121">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="b93bd-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b93bd-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b93bd-122">RELATED LINKS</span></span>

[<span data-ttu-id="b93bd-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="b93bd-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b93bd-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


