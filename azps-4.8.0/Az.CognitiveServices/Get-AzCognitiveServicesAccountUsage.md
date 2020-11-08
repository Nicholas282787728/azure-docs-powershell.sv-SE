---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102369"
---
# <span data-ttu-id="9fd11-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="9fd11-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="9fd11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9fd11-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd11-103">Hämta aktuella användnings områden för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="9fd11-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="9fd11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9fd11-104">SYNTAX</span></span>

### <span data-ttu-id="9fd11-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9fd11-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fd11-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fd11-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fd11-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fd11-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fd11-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9fd11-108">DESCRIPTION</span></span>
<span data-ttu-id="9fd11-109">Cmdleten **Get-AzCognitiveServicesAccountUsage** hämtar aktuella användnings områden för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="9fd11-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="9fd11-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9fd11-110">EXAMPLES</span></span>

### <span data-ttu-id="9fd11-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9fd11-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="9fd11-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9fd11-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="9fd11-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9fd11-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="9fd11-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9fd11-114">PARAMETERS</span></span>

### <span data-ttu-id="9fd11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd11-115">-DefaultProfile</span></span>
<span data-ttu-id="9fd11-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9fd11-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fd11-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fd11-117">-InputObject</span></span>
<span data-ttu-id="9fd11-118">Konto objekt för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="9fd11-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd11-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9fd11-119">-Name</span></span>
<span data-ttu-id="9fd11-120">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="9fd11-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd11-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fd11-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9fd11-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd11-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fd11-123">-ResourceId</span></span>
<span data-ttu-id="9fd11-124">Resurs-ID för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="9fd11-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd11-125">CommonParameters</span></span>
<span data-ttu-id="9fd11-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd11-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fd11-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd11-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9fd11-128">INPUTS</span></span>

### <span data-ttu-id="9fd11-129">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9fd11-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="9fd11-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9fd11-130">System.String</span></span>

## <span data-ttu-id="9fd11-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9fd11-131">OUTPUTS</span></span>

### <span data-ttu-id="9fd11-132">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="9fd11-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="9fd11-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9fd11-133">NOTES</span></span>

## <span data-ttu-id="9fd11-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9fd11-134">RELATED LINKS</span></span>
