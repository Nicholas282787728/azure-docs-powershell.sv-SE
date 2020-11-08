---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270337"
---
# <span data-ttu-id="0a57e-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0a57e-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="0a57e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a57e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a57e-103">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="0a57e-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0a57e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a57e-104">SYNTAX</span></span>

### <span data-ttu-id="0a57e-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0a57e-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a57e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a57e-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a57e-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a57e-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a57e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a57e-108">DESCRIPTION</span></span>
<span data-ttu-id="0a57e-109">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="0a57e-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0a57e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a57e-110">EXAMPLES</span></span>

### <span data-ttu-id="0a57e-111">Ta bort ett befintligt hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="0a57e-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="0a57e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a57e-112">PARAMETERS</span></span>

### <span data-ttu-id="0a57e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a57e-113">-AsJob</span></span>
<span data-ttu-id="0a57e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0a57e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a57e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a57e-115">-DefaultProfile</span></span>
<span data-ttu-id="0a57e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a57e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a57e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0a57e-117">-Force</span></span>
<span data-ttu-id="0a57e-118">Ta bort hanterat Kubernetes-kluster utan fråga</span><span class="sxs-lookup"><span data-stu-id="0a57e-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="0a57e-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0a57e-119">-Id</span></span>
<span data-ttu-id="0a57e-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="0a57e-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="0a57e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a57e-121">-InputObject</span></span>
<span data-ttu-id="0a57e-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="0a57e-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="0a57e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a57e-123">-Name</span></span>
<span data-ttu-id="0a57e-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="0a57e-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="0a57e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a57e-125">-PassThru</span></span>
<span data-ttu-id="0a57e-126">Returnerar sant om borttagningen lyckades</span><span class="sxs-lookup"><span data-stu-id="0a57e-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="0a57e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a57e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a57e-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0a57e-128">Resource group name</span></span>

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

### <span data-ttu-id="0a57e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a57e-129">-Confirm</span></span>
<span data-ttu-id="0a57e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a57e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a57e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a57e-131">-WhatIf</span></span>
<span data-ttu-id="0a57e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a57e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a57e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a57e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a57e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a57e-134">CommonParameters</span></span>
<span data-ttu-id="0a57e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a57e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a57e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a57e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a57e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a57e-137">INPUTS</span></span>

### <span data-ttu-id="0a57e-138">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0a57e-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="0a57e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0a57e-139">System.String</span></span>

## <span data-ttu-id="0a57e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a57e-140">OUTPUTS</span></span>

### <span data-ttu-id="0a57e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a57e-141">System.Boolean</span></span>

## <span data-ttu-id="0a57e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a57e-142">NOTES</span></span>

## <span data-ttu-id="0a57e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a57e-143">RELATED LINKS</span></span>
