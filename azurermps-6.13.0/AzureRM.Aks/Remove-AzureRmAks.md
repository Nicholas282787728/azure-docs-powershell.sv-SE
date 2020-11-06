---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 909121a78d09db7d15591a93db9479d0ccc8381b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580895"
---
# <span data-ttu-id="50f92-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="50f92-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="50f92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50f92-102">SYNOPSIS</span></span>
<span data-ttu-id="50f92-103">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="50f92-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50f92-104">SYNTAX</span></span>

### <span data-ttu-id="50f92-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="50f92-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f92-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f92-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50f92-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50f92-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50f92-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50f92-108">DESCRIPTION</span></span>
<span data-ttu-id="50f92-109">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="50f92-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="50f92-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50f92-110">EXAMPLES</span></span>

### <span data-ttu-id="50f92-111">Ta bort ett befintligt hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="50f92-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="50f92-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50f92-112">PARAMETERS</span></span>

### <span data-ttu-id="50f92-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50f92-113">-AsJob</span></span>
<span data-ttu-id="50f92-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="50f92-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f92-115">-DefaultProfile</span></span>
<span data-ttu-id="50f92-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50f92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50f92-117">-Force</span><span class="sxs-lookup"><span data-stu-id="50f92-117">-Force</span></span>
<span data-ttu-id="50f92-118">Ta bort hanterat Kubernetes-kluster utan fråga</span><span class="sxs-lookup"><span data-stu-id="50f92-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-119">-ID</span><span class="sxs-lookup"><span data-stu-id="50f92-119">-Id</span></span>
<span data-ttu-id="50f92-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="50f92-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50f92-121">-InputObject</span></span>
<span data-ttu-id="50f92-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="50f92-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="50f92-123">-Name</span></span>
<span data-ttu-id="50f92-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="50f92-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50f92-125">-PassThru</span></span>
<span data-ttu-id="50f92-126">Returnerar sant om borttagningen lyckades</span><span class="sxs-lookup"><span data-stu-id="50f92-126">Returns true if deletion is successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f92-127">-ResourceGroupName</span></span>
<span data-ttu-id="50f92-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="50f92-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50f92-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50f92-129">-Confirm</span></span>
<span data-ttu-id="50f92-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50f92-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50f92-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50f92-131">-WhatIf</span></span>
<span data-ttu-id="50f92-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="50f92-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50f92-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="50f92-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50f92-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f92-134">CommonParameters</span></span>
<span data-ttu-id="50f92-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f92-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f92-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f92-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f92-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50f92-137">INPUTS</span></span>

### <span data-ttu-id="50f92-138">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="50f92-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="50f92-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50f92-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="50f92-140">System. String</span><span class="sxs-lookup"><span data-stu-id="50f92-140">System.String</span></span>

## <span data-ttu-id="50f92-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50f92-141">OUTPUTS</span></span>

### <span data-ttu-id="50f92-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50f92-142">System.Boolean</span></span>

## <span data-ttu-id="50f92-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50f92-143">NOTES</span></span>

## <span data-ttu-id="50f92-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50f92-144">RELATED LINKS</span></span>
