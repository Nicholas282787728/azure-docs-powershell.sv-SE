---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: 6387e5a2938bdef99e4aea5e93248a0ecf8e8da7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572532"
---
# <span data-ttu-id="52472-101">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52472-101">Set-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="52472-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52472-102">SYNOPSIS</span></span>
<span data-ttu-id="52472-103">Uppdaterar tjänstens topologi.</span><span class="sxs-lookup"><span data-stu-id="52472-103">Updates the service topology.</span></span>

## <span data-ttu-id="52472-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52472-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52472-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52472-105">DESCRIPTION</span></span>
<span data-ttu-id="52472-106">Cmdleten **set-AzureRmDeploymentManagerServiceTopology** uppdaterar en tjänst topologi med den angivna tjänst Topology-objektet.</span><span class="sxs-lookup"><span data-stu-id="52472-106">The **Set-AzureRmDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="52472-107">Cmdleten returnerar den uppdaterade tjänstens Topology-objekt.</span><span class="sxs-lookup"><span data-stu-id="52472-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="52472-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52472-108">EXAMPLES</span></span>

### <span data-ttu-id="52472-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52472-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="52472-110">Det här kommandot uppdaterar en tjänst sto pol Ogin vars namn och ResourceGroup matchar $serviceTopologyObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="52472-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="52472-111">Kommandot returnerar den uppdaterade tjänstens Topology-objekt.</span><span class="sxs-lookup"><span data-stu-id="52472-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="52472-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52472-112">PARAMETERS</span></span>

### <span data-ttu-id="52472-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52472-113">-DefaultProfile</span></span>
<span data-ttu-id="52472-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52472-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52472-115">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52472-115">-ServiceTopology</span></span>
<span data-ttu-id="52472-116">Objektet tjänst Topology.</span><span class="sxs-lookup"><span data-stu-id="52472-116">The service topology object.</span></span>

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

### <span data-ttu-id="52472-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52472-117">-Confirm</span></span>
<span data-ttu-id="52472-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52472-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52472-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52472-119">-WhatIf</span></span>
<span data-ttu-id="52472-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52472-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52472-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52472-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52472-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52472-122">CommonParameters</span></span>
<span data-ttu-id="52472-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52472-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52472-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52472-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52472-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52472-125">INPUTS</span></span>

### <span data-ttu-id="52472-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="52472-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="52472-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52472-127">OUTPUTS</span></span>

### <span data-ttu-id="52472-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="52472-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="52472-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52472-129">NOTES</span></span>

## <span data-ttu-id="52472-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52472-130">RELATED LINKS</span></span>

[<span data-ttu-id="52472-131">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52472-131">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="52472-132">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52472-132">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="52472-133">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="52472-133">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)