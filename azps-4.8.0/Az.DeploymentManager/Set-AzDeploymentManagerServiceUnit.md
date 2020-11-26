---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262741"
---
# <span data-ttu-id="2f67f-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2f67f-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="2f67f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f67f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f67f-103">Uppdaterar tjänst enheten.</span><span class="sxs-lookup"><span data-stu-id="2f67f-103">Updates the service unit.</span></span>

## <span data-ttu-id="2f67f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f67f-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f67f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f67f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f67f-106">Cmdleten **set-AzDeploymentManagerServiceUnit** uppdaterar en tjänst enhet med det angivna tjänst enhets objektet.</span><span class="sxs-lookup"><span data-stu-id="2f67f-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="2f67f-107">Cmdleten returnerar det uppdaterade tjänst enhets objekt.</span><span class="sxs-lookup"><span data-stu-id="2f67f-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="2f67f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f67f-108">EXAMPLES</span></span>

### <span data-ttu-id="2f67f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f67f-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="2f67f-110">Det här kommandot uppdaterar en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="2f67f-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="2f67f-111">Kommandot returnerar det uppdaterade tjänst enhetens objekt.</span><span class="sxs-lookup"><span data-stu-id="2f67f-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="2f67f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f67f-112">PARAMETERS</span></span>

### <span data-ttu-id="2f67f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f67f-113">-DefaultProfile</span></span>
<span data-ttu-id="2f67f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f67f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f67f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f67f-115">-InputObject</span></span>
<span data-ttu-id="2f67f-116">Objektet service enhet.</span><span class="sxs-lookup"><span data-stu-id="2f67f-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f67f-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f67f-117">-Confirm</span></span>
<span data-ttu-id="2f67f-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f67f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f67f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f67f-119">-WhatIf</span></span>
<span data-ttu-id="2f67f-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f67f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f67f-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f67f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f67f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f67f-122">CommonParameters</span></span>
<span data-ttu-id="2f67f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f67f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f67f-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f67f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f67f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f67f-125">INPUTS</span></span>

### <span data-ttu-id="2f67f-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2f67f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2f67f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f67f-127">OUTPUTS</span></span>

### <span data-ttu-id="2f67f-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2f67f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2f67f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f67f-129">NOTES</span></span>

## <span data-ttu-id="2f67f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f67f-130">RELATED LINKS</span></span>