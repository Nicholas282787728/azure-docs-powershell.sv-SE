---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571388"
---
# <span data-ttu-id="3d1a3-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3d1a3-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="3d1a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1a3-103">Uppdaterar en tjänst i tjänste sto pol Ogin.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="3d1a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d1a3-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d1a3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="3d1a3-106">Cmdleten **set-AzureRmDeploymentManagerService** uppdaterar en tjänst med det angivna serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="3d1a3-107">Cmdleten returnerar det uppdaterade serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="3d1a3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d1a3-108">EXAMPLES</span></span>

### <span data-ttu-id="3d1a3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d1a3-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="3d1a3-110">Det här kommandot uppdaterar en tjänst vars namn, namn och ResourceGroup matchar namn, ServiceTopologyName och $serviceObject ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="3d1a3-111">Tjänsten uppdateras till de egenskaper som anges i $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="3d1a3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d1a3-112">PARAMETERS</span></span>

### <span data-ttu-id="3d1a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1a3-113">-DefaultProfile</span></span>
<span data-ttu-id="3d1a3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d1a3-115">-Service</span><span class="sxs-lookup"><span data-stu-id="3d1a3-115">-Service</span></span>
<span data-ttu-id="3d1a3-116">Serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-116">The service object.</span></span>

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

### <span data-ttu-id="3d1a3-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d1a3-117">-Confirm</span></span>
<span data-ttu-id="3d1a3-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d1a3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1a3-119">-WhatIf</span></span>
<span data-ttu-id="3d1a3-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d1a3-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d1a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1a3-122">CommonParameters</span></span>
<span data-ttu-id="3d1a3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d1a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1a3-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1a3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d1a3-125">INPUTS</span></span>

### <span data-ttu-id="3d1a3-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3d1a3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3d1a3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d1a3-127">OUTPUTS</span></span>

### <span data-ttu-id="3d1a3-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="3d1a3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3d1a3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d1a3-129">NOTES</span></span>

## <span data-ttu-id="3d1a3-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d1a3-130">RELATED LINKS</span></span>

[<span data-ttu-id="3d1a3-131">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3d1a3-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3d1a3-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3d1a3-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="3d1a3-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3d1a3-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)