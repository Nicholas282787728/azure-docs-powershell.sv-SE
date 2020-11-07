---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743473"
---
# <span data-ttu-id="a18ef-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="a18ef-101">Remove-AzAks</span></span>

## <span data-ttu-id="a18ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a18ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a18ef-103">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="a18ef-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a18ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a18ef-104">SYNTAX</span></span>

### <span data-ttu-id="a18ef-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a18ef-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a18ef-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18ef-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a18ef-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a18ef-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a18ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a18ef-108">DESCRIPTION</span></span>
<span data-ttu-id="a18ef-109">Ta bort ett hanterat Kubernetes-kluster.</span><span class="sxs-lookup"><span data-stu-id="a18ef-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a18ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a18ef-110">EXAMPLES</span></span>

### <span data-ttu-id="a18ef-111">Ta bort ett befintligt hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a18ef-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="a18ef-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a18ef-112">PARAMETERS</span></span>

### <span data-ttu-id="a18ef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a18ef-113">-AsJob</span></span>
<span data-ttu-id="a18ef-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a18ef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a18ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a18ef-115">-DefaultProfile</span></span>
<span data-ttu-id="a18ef-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a18ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a18ef-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a18ef-117">-Force</span></span>
<span data-ttu-id="a18ef-118">Ta bort hanterat Kubernetes-kluster utan fråga</span><span class="sxs-lookup"><span data-stu-id="a18ef-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="a18ef-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a18ef-119">-Id</span></span>
<span data-ttu-id="a18ef-120">ID för ett hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a18ef-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a18ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a18ef-121">-InputObject</span></span>
<span data-ttu-id="a18ef-122">Ett PSKubernetesCluster-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a18ef-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a18ef-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a18ef-123">-Name</span></span>
<span data-ttu-id="a18ef-124">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a18ef-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a18ef-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a18ef-125">-PassThru</span></span>
<span data-ttu-id="a18ef-126">Returnerar sant om borttagningen lyckades</span><span class="sxs-lookup"><span data-stu-id="a18ef-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="a18ef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a18ef-127">-ResourceGroupName</span></span>
<span data-ttu-id="a18ef-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a18ef-128">Resource group name</span></span>

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

### <span data-ttu-id="a18ef-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a18ef-129">-Confirm</span></span>
<span data-ttu-id="a18ef-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a18ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a18ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a18ef-131">-WhatIf</span></span>
<span data-ttu-id="a18ef-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a18ef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a18ef-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a18ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a18ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a18ef-134">CommonParameters</span></span>
<span data-ttu-id="a18ef-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a18ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a18ef-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a18ef-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a18ef-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a18ef-137">INPUTS</span></span>

### <span data-ttu-id="a18ef-138">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a18ef-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="a18ef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a18ef-139">System.String</span></span>

## <span data-ttu-id="a18ef-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a18ef-140">OUTPUTS</span></span>

### <span data-ttu-id="a18ef-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a18ef-141">System.Boolean</span></span>

## <span data-ttu-id="a18ef-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a18ef-142">NOTES</span></span>

## <span data-ttu-id="a18ef-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a18ef-143">RELATED LINKS</span></span>
