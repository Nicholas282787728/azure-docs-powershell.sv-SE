---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 28add3b4bffe808be5391de3ddbac759c36f5820
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092658"
---
# <span data-ttu-id="8949e-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8949e-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="8949e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8949e-102">SYNOPSIS</span></span>
<span data-ttu-id="8949e-103">Tar bort metadata från DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="8949e-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="8949e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8949e-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8949e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8949e-105">DESCRIPTION</span></span>
<span data-ttu-id="8949e-106">Cmdleten **Remove-AzAutomationDscNodeConfiguration** tar bort metadata från DSC-nodkonfigurationer (önskad tillstånd Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8949e-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="8949e-107">Automation lagrar DSC-nodkonfigurationer som ett MOF-konfigurationsobjekt (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="8949e-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8949e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8949e-108">EXAMPLES</span></span>

## <span data-ttu-id="8949e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8949e-109">PARAMETERS</span></span>

### <span data-ttu-id="8949e-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8949e-110">-AutomationAccountName</span></span>
<span data-ttu-id="8949e-111">Anger namnet på ett Automation-konto som innehåller DSC-nodkonfigurationer för vilka denna cmdlet tar bort metadata.</span><span class="sxs-lookup"><span data-stu-id="8949e-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8949e-112">-DefaultProfile</span></span>
<span data-ttu-id="8949e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8949e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8949e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8949e-114">-Force</span></span>
<span data-ttu-id="8949e-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="8949e-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="8949e-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="8949e-117">Anger att denna cmdlet ignorerar nodtyper.</span><span class="sxs-lookup"><span data-stu-id="8949e-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8949e-118">-Name</span></span>
<span data-ttu-id="8949e-119">Anger namnet på DSC-nodadressen för vilken denna cmdlet tar bort metadata.</span><span class="sxs-lookup"><span data-stu-id="8949e-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8949e-120">-ResourceGroupName</span></span>
<span data-ttu-id="8949e-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8949e-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8949e-122">Denna cmdlet tar bort metadata för DSC-nodkonfigurationer i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8949e-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8949e-123">-Confirm</span></span>
<span data-ttu-id="8949e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8949e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8949e-125">-WhatIf</span></span>
<span data-ttu-id="8949e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8949e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8949e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8949e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8949e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8949e-128">CommonParameters</span></span>
<span data-ttu-id="8949e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8949e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8949e-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8949e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8949e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8949e-131">INPUTS</span></span>

### <span data-ttu-id="8949e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8949e-132">System.String</span></span>

## <span data-ttu-id="8949e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8949e-133">OUTPUTS</span></span>

### <span data-ttu-id="8949e-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="8949e-134">System.Void</span></span>

## <span data-ttu-id="8949e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8949e-135">NOTES</span></span>

## <span data-ttu-id="8949e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8949e-136">RELATED LINKS</span></span>

[<span data-ttu-id="8949e-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8949e-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8949e-138">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8949e-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="8949e-139">Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8949e-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


