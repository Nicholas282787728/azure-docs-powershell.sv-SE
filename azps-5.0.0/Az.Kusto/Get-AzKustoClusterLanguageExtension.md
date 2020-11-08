---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272248"
---
# <span data-ttu-id="03764-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="03764-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="03764-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03764-102">SYNOPSIS</span></span>
<span data-ttu-id="03764-103">Returnerar en lista med språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="03764-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="03764-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03764-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="03764-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03764-105">DESCRIPTION</span></span>
<span data-ttu-id="03764-106">Returnerar en lista med språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="03764-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="03764-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03764-107">EXAMPLES</span></span>

### <span data-ttu-id="03764-108">Exempel 1: lista alla språk tillägg som är inställda för ett kluster</span><span class="sxs-lookup"><span data-stu-id="03764-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="03764-109">Kommandot ovan returnerar en lista över språk tillägg som kan köras i Keyword-frågor.</span><span class="sxs-lookup"><span data-stu-id="03764-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="03764-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03764-110">PARAMETERS</span></span>

### <span data-ttu-id="03764-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="03764-111">-ClusterName</span></span>
<span data-ttu-id="03764-112">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="03764-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="03764-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03764-113">-DefaultProfile</span></span>
<span data-ttu-id="03764-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03764-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03764-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03764-115">-ResourceGroupName</span></span>
<span data-ttu-id="03764-116">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="03764-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="03764-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="03764-117">-SubscriptionId</span></span>
<span data-ttu-id="03764-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="03764-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="03764-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="03764-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="03764-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03764-120">-Confirm</span></span>
<span data-ttu-id="03764-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03764-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03764-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03764-122">-WhatIf</span></span>
<span data-ttu-id="03764-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="03764-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03764-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="03764-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03764-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03764-125">CommonParameters</span></span>
<span data-ttu-id="03764-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03764-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03764-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03764-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03764-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03764-128">INPUTS</span></span>

## <span data-ttu-id="03764-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03764-129">OUTPUTS</span></span>

### <span data-ttu-id="03764-130">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="03764-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="03764-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03764-131">NOTES</span></span>

<span data-ttu-id="03764-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="03764-132">ALIASES</span></span>

## <span data-ttu-id="03764-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03764-133">RELATED LINKS</span></span>

