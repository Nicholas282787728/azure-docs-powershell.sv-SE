---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271308"
---
# <span data-ttu-id="b4590-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="b4590-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="b4590-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4590-102">SYNOPSIS</span></span>
<span data-ttu-id="b4590-103">länka tjänst för arbets yta</span><span class="sxs-lookup"><span data-stu-id="b4590-103">link service for workspace</span></span>

## <span data-ttu-id="b4590-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4590-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4590-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4590-105">DESCRIPTION</span></span>
<span data-ttu-id="b4590-106">länka tjänst för arbets yta</span><span class="sxs-lookup"><span data-stu-id="b4590-106">link service for workspace</span></span>

## <span data-ttu-id="b4590-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4590-107">EXAMPLES</span></span>

### <span data-ttu-id="b4590-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4590-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="b4590-109">länka kluster för arbets yta</span><span class="sxs-lookup"><span data-stu-id="b4590-109">link cluster for workspace</span></span>

## <span data-ttu-id="b4590-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4590-110">PARAMETERS</span></span>

### <span data-ttu-id="b4590-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4590-111">-AsJob</span></span>
<span data-ttu-id="b4590-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b4590-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4590-113">-DefaultProfile</span></span>
<span data-ttu-id="b4590-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4590-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b4590-115">-LinkedServiceName</span></span>
<span data-ttu-id="b4590-116">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="b4590-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4590-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4590-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b4590-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4590-119">-ResourceId</span></span>
<span data-ttu-id="b4590-120">Resurs-ID för resursen som ska länkas till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="b4590-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="b4590-121">Detta bör användas för att länka resurser som kräver Läs åtkomst</span><span class="sxs-lookup"><span data-stu-id="b4590-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-122">-Taggar</span><span class="sxs-lookup"><span data-stu-id="b4590-122">-Tags</span></span>
<span data-ttu-id="b4590-123">Taggen.</span><span class="sxs-lookup"><span data-stu-id="b4590-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4590-124">-WorkspaceName</span></span>
<span data-ttu-id="b4590-125">Arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="b4590-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="b4590-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="b4590-127">Resurs-ID för resursen som ska länkas till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="b4590-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="b4590-128">Detta bör användas för att länka resurser som kräver skriv åtkomst.</span><span class="sxs-lookup"><span data-stu-id="b4590-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="b4590-129">Klustret måste ha etablerings status "lyckades" och giltiga egenskaper för valv.</span><span class="sxs-lookup"><span data-stu-id="b4590-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4590-130">-Confirm</span></span>
<span data-ttu-id="b4590-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4590-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4590-132">-WhatIf</span></span>
<span data-ttu-id="b4590-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4590-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4590-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4590-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4590-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4590-135">CommonParameters</span></span>
<span data-ttu-id="b4590-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4590-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4590-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4590-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4590-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4590-138">INPUTS</span></span>

### <span data-ttu-id="b4590-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4590-139">System.String</span></span>

## <span data-ttu-id="b4590-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4590-140">OUTPUTS</span></span>

### <span data-ttu-id="b4590-141">Microsoft. Azure. commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b4590-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="b4590-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4590-142">NOTES</span></span>

## <span data-ttu-id="b4590-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4590-143">RELATED LINKS</span></span>
