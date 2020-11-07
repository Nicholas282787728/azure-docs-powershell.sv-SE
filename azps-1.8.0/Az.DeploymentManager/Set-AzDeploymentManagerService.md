---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 28dc0bd04484823636398b828922fbb79db24672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754202"
---
# <span data-ttu-id="af031-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="af031-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="af031-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af031-102">SYNOPSIS</span></span>
<span data-ttu-id="af031-103">Uppdaterar tjänsten.</span><span class="sxs-lookup"><span data-stu-id="af031-103">Updates the service.</span></span>

## <span data-ttu-id="af031-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af031-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af031-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af031-105">DESCRIPTION</span></span>
<span data-ttu-id="af031-106">Cmdleten **set-AzDeploymentManagerService** uppdaterar en tjänst med det angivna serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="af031-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="af031-107">Cmdleten returnerar det uppdaterade serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="af031-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="af031-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af031-108">EXAMPLES</span></span>

### <span data-ttu-id="af031-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af031-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="af031-110">Det här kommandot uppdaterar en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="af031-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="af031-111">Tjänsten uppdateras till de egenskaper som anges i $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="af031-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="af031-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af031-112">PARAMETERS</span></span>

### <span data-ttu-id="af031-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af031-113">-DefaultProfile</span></span>
<span data-ttu-id="af031-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af031-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af031-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af031-115">-InputObject</span></span>
<span data-ttu-id="af031-116">Serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="af031-116">The service object.</span></span>

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

### <span data-ttu-id="af031-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="af031-117">-Confirm</span></span>
<span data-ttu-id="af031-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="af031-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af031-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af031-119">-WhatIf</span></span>
<span data-ttu-id="af031-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="af031-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af031-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="af031-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af031-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af031-122">CommonParameters</span></span>
<span data-ttu-id="af031-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af031-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af031-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af031-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af031-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="af031-125">INPUTS</span></span>

### <span data-ttu-id="af031-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="af031-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="af031-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af031-127">OUTPUTS</span></span>

### <span data-ttu-id="af031-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="af031-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="af031-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af031-129">NOTES</span></span>

## <span data-ttu-id="af031-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af031-130">RELATED LINKS</span></span>
