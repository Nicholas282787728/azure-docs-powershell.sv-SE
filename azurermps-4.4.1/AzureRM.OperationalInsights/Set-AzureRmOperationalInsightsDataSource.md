---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 13d8be80411e39124ab29d9a31e44edd0ebd95e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574556"
---
# <span data-ttu-id="7bd04-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="7bd04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bd04-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd04-103">Uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="7bd04-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bd04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bd04-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd04-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bd04-105">DESCRIPTION</span></span>
<span data-ttu-id="7bd04-106">Cmdleten **set-AzureRmOperationalInsightsDataSource** uppdaterar en data källa.</span><span class="sxs-lookup"><span data-stu-id="7bd04-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="7bd04-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bd04-107">EXAMPLES</span></span>

## <span data-ttu-id="7bd04-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bd04-108">PARAMETERS</span></span>

### <span data-ttu-id="7bd04-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-109">-DataSource</span></span>
<span data-ttu-id="7bd04-110">Anger den data källa som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="7bd04-110">Specifies the data source that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7bd04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd04-111">-DefaultProfile</span></span>
<span data-ttu-id="7bd04-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bd04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bd04-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd04-113">CommonParameters</span></span>
<span data-ttu-id="7bd04-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd04-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd04-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd04-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd04-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bd04-116">INPUTS</span></span>

### <span data-ttu-id="7bd04-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-117">PSDataSource</span></span>
<span data-ttu-id="7bd04-118">Parametern ' DataSource ' godkänner värdet för typen ' PSDataSource ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7bd04-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="7bd04-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bd04-119">OUTPUTS</span></span>

### <span data-ttu-id="7bd04-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7bd04-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bd04-121">NOTES</span></span>
* <span data-ttu-id="7bd04-122">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="7bd04-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7bd04-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bd04-123">RELATED LINKS</span></span>

[<span data-ttu-id="7bd04-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="7bd04-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bd04-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


