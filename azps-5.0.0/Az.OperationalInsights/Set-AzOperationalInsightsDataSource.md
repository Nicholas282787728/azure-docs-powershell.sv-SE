---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: ef90211ccca53a94db2651f17b3a666a725ce8b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323142"
---
# <span data-ttu-id="69518-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="69518-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="69518-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69518-102">SYNOPSIS</span></span>
<span data-ttu-id="69518-103">Uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="69518-103">Updates a data source.</span></span>

## <span data-ttu-id="69518-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69518-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69518-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69518-105">DESCRIPTION</span></span>
<span data-ttu-id="69518-106">Cmdleten **set-AzOperationalInsightsDataSource** uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="69518-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="69518-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69518-107">EXAMPLES</span></span>

## <span data-ttu-id="69518-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69518-108">PARAMETERS</span></span>

### <span data-ttu-id="69518-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="69518-109">-DataSource</span></span>
<span data-ttu-id="69518-110">Anger den data källa som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="69518-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="69518-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69518-111">-DefaultProfile</span></span>
<span data-ttu-id="69518-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69518-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69518-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69518-113">CommonParameters</span></span>
<span data-ttu-id="69518-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69518-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69518-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69518-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69518-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69518-116">INPUTS</span></span>

### <span data-ttu-id="69518-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="69518-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="69518-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69518-118">OUTPUTS</span></span>

### <span data-ttu-id="69518-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="69518-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="69518-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69518-120">NOTES</span></span>
* <span data-ttu-id="69518-121">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="69518-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="69518-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69518-122">RELATED LINKS</span></span>

[<span data-ttu-id="69518-123">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="69518-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="69518-124">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="69518-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


