---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571856"
---
# <span data-ttu-id="d028a-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="d028a-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="d028a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d028a-102">SYNOPSIS</span></span>
<span data-ttu-id="d028a-103">Uppdaterar ett steg.</span><span class="sxs-lookup"><span data-stu-id="d028a-103">Updates a step.</span></span>

## <span data-ttu-id="d028a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d028a-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d028a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d028a-105">DESCRIPTION</span></span>
<span data-ttu-id="d028a-106">Cmdleten **set-AzureRmDeploymentManagerStep** uppdaterar ett steg med angivet steg-objekt.</span><span class="sxs-lookup"><span data-stu-id="d028a-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="d028a-107">Cmdleten returnerar det uppdaterade steget.</span><span class="sxs-lookup"><span data-stu-id="d028a-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="d028a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d028a-108">EXAMPLES</span></span>

### <span data-ttu-id="d028a-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d028a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="d028a-110">Det här kommandot uppdaterar ett steg vars namn och ResourceGroup matchar $stepObjectens namn och ResourceGroupName-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="d028a-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="d028a-111">Steget uppdateras till de egenskaper som anges i $stepObject.</span><span class="sxs-lookup"><span data-stu-id="d028a-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="d028a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d028a-112">PARAMETERS</span></span>

### <span data-ttu-id="d028a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d028a-113">-DefaultProfile</span></span>
<span data-ttu-id="d028a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d028a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d028a-115">-Steg</span><span class="sxs-lookup"><span data-stu-id="d028a-115">-Step</span></span>
<span data-ttu-id="d028a-116">Steg-objekt.</span><span class="sxs-lookup"><span data-stu-id="d028a-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d028a-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d028a-117">-Confirm</span></span>
<span data-ttu-id="d028a-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d028a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d028a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d028a-119">-WhatIf</span></span>
<span data-ttu-id="d028a-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d028a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d028a-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d028a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d028a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d028a-122">CommonParameters</span></span>
<span data-ttu-id="d028a-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d028a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d028a-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d028a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d028a-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d028a-125">INPUTS</span></span>

### <span data-ttu-id="d028a-126">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="d028a-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d028a-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d028a-127">OUTPUTS</span></span>

### <span data-ttu-id="d028a-128">Microsoft. Azure. commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="d028a-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="d028a-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d028a-129">NOTES</span></span>

## <span data-ttu-id="d028a-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d028a-130">RELATED LINKS</span></span>
