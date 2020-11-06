---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: b04819f61f37b9bb47818a8b17e93db9a7cdb05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571859"
---
# <span data-ttu-id="06120-101">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="06120-101">Set-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="06120-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06120-102">SYNOPSIS</span></span>
<span data-ttu-id="06120-103">Uppdaterar en tjänst.</span><span class="sxs-lookup"><span data-stu-id="06120-103">Updates a service unit.</span></span>

## <span data-ttu-id="06120-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06120-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06120-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06120-105">DESCRIPTION</span></span>
<span data-ttu-id="06120-106">Cmdleten **set-AzureRmDeploymentManagerServiceUnit** uppdaterar en tjänst enhet med det angivna tjänst enhets objektet.</span><span class="sxs-lookup"><span data-stu-id="06120-106">The **Set-AzureRmDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="06120-107">Cmdleten returnerar det uppdaterade tjänst enhets objekt.</span><span class="sxs-lookup"><span data-stu-id="06120-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="06120-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06120-108">EXAMPLES</span></span>

### <span data-ttu-id="06120-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="06120-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="06120-110">Det här kommandot uppdaterar en tjänst enhet vars namn, tjänst namn, namn på tjänste topologi och ResourceGroup matchar namnet, ServiceName, ServiceTopologyName och ResourceGroupName för $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="06120-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="06120-111">Kommandot returnerar det uppdaterade tjänst enhetens objekt.</span><span class="sxs-lookup"><span data-stu-id="06120-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="06120-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06120-112">PARAMETERS</span></span>

### <span data-ttu-id="06120-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06120-113">-DefaultProfile</span></span>
<span data-ttu-id="06120-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="06120-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06120-115">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="06120-115">-ServiceUnit</span></span>
<span data-ttu-id="06120-116">Objektet service enhet.</span><span class="sxs-lookup"><span data-stu-id="06120-116">The service unit object.</span></span>

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

### <span data-ttu-id="06120-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="06120-117">-Confirm</span></span>
<span data-ttu-id="06120-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="06120-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06120-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06120-119">-WhatIf</span></span>
<span data-ttu-id="06120-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="06120-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06120-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="06120-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06120-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06120-122">CommonParameters</span></span>
<span data-ttu-id="06120-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06120-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06120-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06120-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06120-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06120-125">INPUTS</span></span>

### <span data-ttu-id="06120-126">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="06120-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="06120-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06120-127">OUTPUTS</span></span>

### <span data-ttu-id="06120-128">Microsoft. Azure. commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="06120-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="06120-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06120-129">NOTES</span></span>

## <span data-ttu-id="06120-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06120-130">RELATED LINKS</span></span>

[<span data-ttu-id="06120-131">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="06120-131">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="06120-132">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="06120-132">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="06120-133">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="06120-133">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)