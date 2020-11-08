---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101207"
---
# <span data-ttu-id="48ad3-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48ad3-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="48ad3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="48ad3-103">Hämta Application Insights Linked Storage-konto</span><span class="sxs-lookup"><span data-stu-id="48ad3-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="48ad3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48ad3-104">SYNTAX</span></span>

### <span data-ttu-id="48ad3-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="48ad3-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48ad3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ad3-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48ad3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48ad3-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48ad3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48ad3-108">DESCRIPTION</span></span>
<span data-ttu-id="48ad3-109">Hämta Application Insights Linked Storage-konto</span><span class="sxs-lookup"><span data-stu-id="48ad3-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="48ad3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48ad3-110">EXAMPLES</span></span>

### <span data-ttu-id="48ad3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="48ad3-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="48ad3-112">Få ett länkat lagrings konto associerat med komponenten "componentName"</span><span class="sxs-lookup"><span data-stu-id="48ad3-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="48ad3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48ad3-113">PARAMETERS</span></span>

### <span data-ttu-id="48ad3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="48ad3-114">-ComponentName</span></span>
<span data-ttu-id="48ad3-115">Komponent namn</span><span class="sxs-lookup"><span data-stu-id="48ad3-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ad3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ad3-116">-DefaultProfile</span></span>
<span data-ttu-id="48ad3-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48ad3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48ad3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48ad3-118">-InputObject</span></span>
<span data-ttu-id="48ad3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="48ad3-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48ad3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ad3-120">-ResourceGroupName</span></span>
<span data-ttu-id="48ad3-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="48ad3-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ad3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48ad3-122">-ResourceId</span></span>
<span data-ttu-id="48ad3-123">Komponent-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48ad3-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48ad3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ad3-124">CommonParameters</span></span>
<span data-ttu-id="48ad3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ad3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ad3-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48ad3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ad3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48ad3-127">INPUTS</span></span>

### <span data-ttu-id="48ad3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="48ad3-128">System.String</span></span>

### <span data-ttu-id="48ad3-129">Microsoft. Azure. commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="48ad3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="48ad3-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48ad3-130">OUTPUTS</span></span>

### <span data-ttu-id="48ad3-131">Microsoft. Azure. commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="48ad3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="48ad3-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48ad3-132">NOTES</span></span>

## <span data-ttu-id="48ad3-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48ad3-133">RELATED LINKS</span></span>
