---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259546"
---
# <span data-ttu-id="746bb-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="746bb-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="746bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="746bb-102">SYNOPSIS</span></span>
<span data-ttu-id="746bb-103">Tar bort ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="746bb-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="746bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="746bb-104">SYNTAX</span></span>

### <span data-ttu-id="746bb-105">ByIntegrationAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="746bb-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746bb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="746bb-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="746bb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="746bb-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746bb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="746bb-108">DESCRIPTION</span></span>
<span data-ttu-id="746bb-109">Cmdleten **Remove-AzIntegrationAccountAssembly** tar bort en sammansättning från ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="746bb-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="746bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="746bb-110">EXAMPLES</span></span>

### <span data-ttu-id="746bb-111">Exempel 1: ta bort en montering efter parametrar</span><span class="sxs-lookup"><span data-stu-id="746bb-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="746bb-112">Tar bort sammansättningen "sampleAssembly" som finns i integrations kontot "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="746bb-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="746bb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="746bb-113">PARAMETERS</span></span>

### <span data-ttu-id="746bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746bb-114">-DefaultProfile</span></span>
<span data-ttu-id="746bb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="746bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746bb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="746bb-116">-InputObject</span></span>
<span data-ttu-id="746bb-117">Ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="746bb-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="746bb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="746bb-118">-Name</span></span>
<span data-ttu-id="746bb-119">Namnet på integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="746bb-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746bb-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="746bb-120">-ParentName</span></span>
<span data-ttu-id="746bb-121">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="746bb-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746bb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746bb-122">-PassThru</span></span>
<span data-ttu-id="746bb-123">Returnera om kommandot lyckades eller inte.</span><span class="sxs-lookup"><span data-stu-id="746bb-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="746bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="746bb-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="746bb-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="746bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="746bb-126">-ResourceId</span></span>
<span data-ttu-id="746bb-127">ID för sammansättningen för integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="746bb-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746bb-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="746bb-128">-Confirm</span></span>
<span data-ttu-id="746bb-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="746bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746bb-130">-WhatIf</span></span>
<span data-ttu-id="746bb-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="746bb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="746bb-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="746bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746bb-133">CommonParameters</span></span>
<span data-ttu-id="746bb-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746bb-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="746bb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746bb-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="746bb-136">INPUTS</span></span>

### <span data-ttu-id="746bb-137">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="746bb-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="746bb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="746bb-138">System.String</span></span>

## <span data-ttu-id="746bb-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="746bb-139">OUTPUTS</span></span>

### <span data-ttu-id="746bb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="746bb-140">System.Boolean</span></span>

## <span data-ttu-id="746bb-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="746bb-141">NOTES</span></span>

## <span data-ttu-id="746bb-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="746bb-142">RELATED LINKS</span></span>