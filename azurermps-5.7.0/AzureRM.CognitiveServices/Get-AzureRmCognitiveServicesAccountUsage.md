---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573549"
---
# <span data-ttu-id="747f7-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="747f7-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="747f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="747f7-102">SYNOPSIS</span></span>
<span data-ttu-id="747f7-103">Hämta aktuella användnings områden för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="747f7-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="747f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="747f7-104">SYNTAX</span></span>

### <span data-ttu-id="747f7-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="747f7-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="747f7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="747f7-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="747f7-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="747f7-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="747f7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="747f7-108">DESCRIPTION</span></span>
<span data-ttu-id="747f7-109">Cmdleten **Get-AzureRmCognitiveServicesAccountUsage** hämtar aktuella användnings områden för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="747f7-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="747f7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="747f7-110">EXAMPLES</span></span>

### <span data-ttu-id="747f7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="747f7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="747f7-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="747f7-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="747f7-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="747f7-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="747f7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="747f7-114">PARAMETERS</span></span>

### <span data-ttu-id="747f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747f7-115">-DefaultProfile</span></span>
<span data-ttu-id="747f7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="747f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="747f7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="747f7-117">-InputObject</span></span>
<span data-ttu-id="747f7-118">Konto objekt för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="747f7-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="747f7-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="747f7-119">-Name</span></span>
<span data-ttu-id="747f7-120">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="747f7-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="747f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="747f7-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="747f7-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="747f7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747f7-123">-ResourceId</span></span>
<span data-ttu-id="747f7-124">Resurs-ID för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="747f7-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="747f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747f7-125">CommonParameters</span></span>
<span data-ttu-id="747f7-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747f7-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747f7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747f7-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="747f7-128">INPUTS</span></span>

### <span data-ttu-id="747f7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="747f7-129">System.String</span></span>

## <span data-ttu-id="747f7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="747f7-130">OUTPUTS</span></span>

### <span data-ttu-id="747f7-131">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="747f7-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="747f7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="747f7-132">NOTES</span></span>

## <span data-ttu-id="747f7-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="747f7-133">RELATED LINKS</span></span>
