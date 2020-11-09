---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320087"
---
# <span data-ttu-id="635cc-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="635cc-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="635cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="635cc-102">SYNOPSIS</span></span>
<span data-ttu-id="635cc-103">Uppdaterar tjänstens topologi.</span><span class="sxs-lookup"><span data-stu-id="635cc-103">Updates the service topology.</span></span>

## <span data-ttu-id="635cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="635cc-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="635cc-105">DESCRIPTION</span></span>
<span data-ttu-id="635cc-106">Cmdleten **set-AzDeploymentManagerServiceTopology** uppdaterar en tjänst topologi med den angivna tjänst Topology-objektet.</span><span class="sxs-lookup"><span data-stu-id="635cc-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="635cc-107">Cmdleten returnerar den uppdaterade tjänstens Topology-objekt.</span><span class="sxs-lookup"><span data-stu-id="635cc-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="635cc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="635cc-108">EXAMPLES</span></span>

### <span data-ttu-id="635cc-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="635cc-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="635cc-110">Det här kommandot uppdaterar en tjänst sto pol Ogin vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="635cc-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="635cc-111">Kommandot returnerar den uppdaterade tjänstens Topology-objekt.</span><span class="sxs-lookup"><span data-stu-id="635cc-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="635cc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="635cc-112">PARAMETERS</span></span>

### <span data-ttu-id="635cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635cc-113">-DefaultProfile</span></span>
<span data-ttu-id="635cc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="635cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="635cc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="635cc-115">-InputObject</span></span>
<span data-ttu-id="635cc-116">Objektet tjänst Topology.</span><span class="sxs-lookup"><span data-stu-id="635cc-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="635cc-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="635cc-117">-Confirm</span></span>
<span data-ttu-id="635cc-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="635cc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="635cc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635cc-119">-WhatIf</span></span>
<span data-ttu-id="635cc-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="635cc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="635cc-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="635cc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="635cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635cc-122">CommonParameters</span></span>
<span data-ttu-id="635cc-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="635cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635cc-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="635cc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635cc-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="635cc-125">INPUTS</span></span>

### <span data-ttu-id="635cc-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="635cc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="635cc-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="635cc-127">OUTPUTS</span></span>

### <span data-ttu-id="635cc-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="635cc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="635cc-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="635cc-129">NOTES</span></span>

## <span data-ttu-id="635cc-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="635cc-130">RELATED LINKS</span></span>
