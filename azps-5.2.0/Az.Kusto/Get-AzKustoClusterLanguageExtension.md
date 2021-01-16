---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399136"
---
# <span data-ttu-id="4e414-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4e414-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="4e414-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e414-102">SYNOPSIS</span></span>
<span data-ttu-id="4e414-103">Returnerar en lista med språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="4e414-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e414-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e414-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e414-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e414-105">DESCRIPTION</span></span>
<span data-ttu-id="4e414-106">Returnerar en lista med språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="4e414-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e414-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e414-107">EXAMPLES</span></span>

### <span data-ttu-id="4e414-108">Exempel 1: lista alla språk tillägg som är inställda för ett kluster</span><span class="sxs-lookup"><span data-stu-id="4e414-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="4e414-109">Kommandot ovan returnerar en lista över språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="4e414-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="4e414-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e414-110">PARAMETERS</span></span>

### <span data-ttu-id="4e414-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="4e414-111">-ClusterName</span></span>
<span data-ttu-id="4e414-112">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="4e414-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e414-113">-DefaultProfile</span></span>
<span data-ttu-id="4e414-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e414-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e414-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e414-116">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="4e414-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e414-117">-SubscriptionId</span></span>
<span data-ttu-id="4e414-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4e414-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e414-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="4e414-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e414-120">-Confirm</span></span>
<span data-ttu-id="4e414-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e414-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e414-122">-WhatIf</span></span>
<span data-ttu-id="4e414-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e414-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e414-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e414-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e414-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e414-125">CommonParameters</span></span>
<span data-ttu-id="4e414-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e414-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e414-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e414-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e414-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e414-128">INPUTS</span></span>

## <span data-ttu-id="4e414-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e414-129">OUTPUTS</span></span>

### <span data-ttu-id="4e414-130">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="4e414-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="4e414-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e414-131">NOTES</span></span>

<span data-ttu-id="4e414-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4e414-132">ALIASES</span></span>

## <span data-ttu-id="4e414-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e414-133">RELATED LINKS</span></span>

