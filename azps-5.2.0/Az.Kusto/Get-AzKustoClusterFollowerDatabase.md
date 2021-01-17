---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391976"
---
# <span data-ttu-id="45bd2-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="45bd2-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="45bd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="45bd2-103">Returnerar en lista med databaser som ägs av detta kluster och följs av ett annat kluster.</span><span class="sxs-lookup"><span data-stu-id="45bd2-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="45bd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45bd2-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45bd2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="45bd2-106">Returnerar en lista med databaser som ägs av detta kluster och följs av ett annat kluster.</span><span class="sxs-lookup"><span data-stu-id="45bd2-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="45bd2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="45bd2-108">Exempel 1: lista alla följda databaser</span><span class="sxs-lookup"><span data-stu-id="45bd2-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="45bd2-109">Kommandot ovan visar alla databaser som ägs av detta kluster och följs av ett annat kluster.</span><span class="sxs-lookup"><span data-stu-id="45bd2-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="45bd2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="45bd2-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="45bd2-111">-ClusterName</span></span>
<span data-ttu-id="45bd2-112">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45bd2-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="45bd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45bd2-113">-DefaultProfile</span></span>
<span data-ttu-id="45bd2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45bd2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45bd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45bd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="45bd2-116">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="45bd2-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="45bd2-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45bd2-117">-SubscriptionId</span></span>
<span data-ttu-id="45bd2-118">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="45bd2-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="45bd2-119">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="45bd2-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="45bd2-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45bd2-120">-Confirm</span></span>
<span data-ttu-id="45bd2-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45bd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45bd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45bd2-122">-WhatIf</span></span>
<span data-ttu-id="45bd2-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45bd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45bd2-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45bd2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45bd2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45bd2-125">CommonParameters</span></span>
<span data-ttu-id="45bd2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45bd2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45bd2-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45bd2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45bd2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45bd2-128">INPUTS</span></span>

## <span data-ttu-id="45bd2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45bd2-129">OUTPUTS</span></span>

### <span data-ttu-id="45bd2-130">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="45bd2-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="45bd2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45bd2-131">NOTES</span></span>

<span data-ttu-id="45bd2-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45bd2-132">ALIASES</span></span>

## <span data-ttu-id="45bd2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45bd2-133">RELATED LINKS</span></span>

