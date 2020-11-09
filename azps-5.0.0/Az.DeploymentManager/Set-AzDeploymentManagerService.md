---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320096"
---
# <span data-ttu-id="a9482-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="a9482-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="a9482-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9482-102">SYNOPSIS</span></span>
<span data-ttu-id="a9482-103">Uppdaterar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a9482-103">Updates the service.</span></span>

## <span data-ttu-id="a9482-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9482-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9482-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9482-105">DESCRIPTION</span></span>
<span data-ttu-id="a9482-106">Cmdleten **set-AzDeploymentManagerService** uppdaterar en tjänst med det angivna serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="a9482-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="a9482-107">Cmdleten returnerar det uppdaterade serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="a9482-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="a9482-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9482-108">EXAMPLES</span></span>

### <span data-ttu-id="a9482-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9482-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="a9482-110">Det här kommandot uppdaterar en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="a9482-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="a9482-111">Tjänsten uppdateras till de egenskaper som anges i $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="a9482-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="a9482-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9482-112">PARAMETERS</span></span>

### <span data-ttu-id="a9482-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9482-113">-DefaultProfile</span></span>
<span data-ttu-id="a9482-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9482-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9482-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9482-115">-InputObject</span></span>
<span data-ttu-id="a9482-116">Serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="a9482-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9482-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9482-117">-Confirm</span></span>
<span data-ttu-id="a9482-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9482-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9482-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9482-119">-WhatIf</span></span>
<span data-ttu-id="a9482-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9482-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9482-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9482-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9482-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9482-122">CommonParameters</span></span>
<span data-ttu-id="a9482-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9482-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9482-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9482-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9482-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9482-125">INPUTS</span></span>

### <span data-ttu-id="a9482-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a9482-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a9482-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9482-127">OUTPUTS</span></span>

### <span data-ttu-id="a9482-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="a9482-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="a9482-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9482-129">NOTES</span></span>

## <span data-ttu-id="a9482-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9482-130">RELATED LINKS</span></span>
