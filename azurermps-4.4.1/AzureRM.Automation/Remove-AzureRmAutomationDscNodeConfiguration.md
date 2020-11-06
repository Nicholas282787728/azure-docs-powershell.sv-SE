---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 56ceba33845061af4e0ccdf3247bab16e079e90c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578516"
---
# <span data-ttu-id="f47fa-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f47fa-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="f47fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f47fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f47fa-103">Tar bort metadata från DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="f47fa-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f47fa-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47fa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f47fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f47fa-106">Cmdleten **Remove-AzureRmAutomationDscNodeConfiguration** tar bort metadata från DSC-nodkonfigurationer (önskad tillstånd Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f47fa-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="f47fa-107">Automation lagrar DSC-nodkonfigurationer som ett MOF-konfigurationsobjekt (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="f47fa-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="f47fa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f47fa-108">EXAMPLES</span></span>

## <span data-ttu-id="f47fa-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f47fa-109">PARAMETERS</span></span>

### <span data-ttu-id="f47fa-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f47fa-110">-AutomationAccountName</span></span>
<span data-ttu-id="f47fa-111">Anger namnet på ett Automation-konto som innehåller DSC-nodkonfigurationer för vilka denna cmdlet tar bort metadata.</span><span class="sxs-lookup"><span data-stu-id="f47fa-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="f47fa-112">-Force</span><span class="sxs-lookup"><span data-stu-id="f47fa-112">-Force</span></span>
<span data-ttu-id="f47fa-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="f47fa-113">ps_force</span></span>

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

### <span data-ttu-id="f47fa-114">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="f47fa-114">-IgnoreNodeMappings</span></span>
<span data-ttu-id="f47fa-115">Anger att denna cmdlet ignorerar nodtyper.</span><span class="sxs-lookup"><span data-stu-id="f47fa-115">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="f47fa-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f47fa-116">-Name</span></span>
<span data-ttu-id="f47fa-117">Anger namnet på DSC-nodadressen för vilken denna cmdlet tar bort metadata.</span><span class="sxs-lookup"><span data-stu-id="f47fa-117">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="f47fa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47fa-118">-ResourceGroupName</span></span>
<span data-ttu-id="f47fa-119">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f47fa-119">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f47fa-120">Denna cmdlet tar bort metadata för DSC-nodkonfigurationer i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f47fa-120">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f47fa-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f47fa-121">-Confirm</span></span>
<span data-ttu-id="f47fa-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f47fa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47fa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47fa-123">-WhatIf</span></span>
<span data-ttu-id="f47fa-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f47fa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47fa-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f47fa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47fa-126">-DefaultProfile</span></span>
<span data-ttu-id="f47fa-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f47fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47fa-128">CommonParameters</span></span>
<span data-ttu-id="f47fa-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47fa-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47fa-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f47fa-131">INPUTS</span></span>

## <span data-ttu-id="f47fa-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f47fa-132">OUTPUTS</span></span>

## <span data-ttu-id="f47fa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f47fa-133">NOTES</span></span>

## <span data-ttu-id="f47fa-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f47fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="f47fa-135">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f47fa-135">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f47fa-136">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f47fa-136">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f47fa-137">Azure Automation-cmdletar</span><span class="sxs-lookup"><span data-stu-id="f47fa-137">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


