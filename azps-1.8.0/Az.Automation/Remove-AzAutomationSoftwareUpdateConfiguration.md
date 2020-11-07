---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 3b608feb9ed496be72d1d74f4a5a2be0569714de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754753"
---
# <span data-ttu-id="2f42c-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f42c-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2f42c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f42c-102">SYNOPSIS</span></span>
<span data-ttu-id="2f42c-103">Tar bort en konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="2f42c-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="2f42c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f42c-104">SYNTAX</span></span>

### <span data-ttu-id="2f42c-105">BySucName (standard)</span><span class="sxs-lookup"><span data-stu-id="2f42c-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f42c-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="2f42c-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f42c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f42c-107">DESCRIPTION</span></span>
<span data-ttu-id="2f42c-108">Denna cmdlet tog bort en konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="2f42c-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="2f42c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f42c-109">EXAMPLES</span></span>

### <span data-ttu-id="2f42c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f42c-110">Example 1</span></span>
<span data-ttu-id="2f42c-111">Det här exemplet visar hur du tar bort ' MyUpdateConfiguration ' från Automation-konto</span><span class="sxs-lookup"><span data-stu-id="2f42c-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="2f42c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f42c-112">PARAMETERS</span></span>

### <span data-ttu-id="2f42c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2f42c-113">-AutomationAccountName</span></span>
<span data-ttu-id="2f42c-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="2f42c-114">The automation account name.</span></span>

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

### <span data-ttu-id="2f42c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f42c-115">-DefaultProfile</span></span>
<span data-ttu-id="2f42c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f42c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f42c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f42c-117">-Name</span></span>
<span data-ttu-id="2f42c-118">Namn på program uppdaterings konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2f42c-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f42c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f42c-119">-PassThru</span></span>
<span data-ttu-id="2f42c-120">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2f42c-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2f42c-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2f42c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f42c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f42c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f42c-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2f42c-123">The resource group name.</span></span>

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

### <span data-ttu-id="2f42c-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f42c-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="2f42c-125">Program uppdaterings konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="2f42c-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f42c-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f42c-126">-Confirm</span></span>
<span data-ttu-id="2f42c-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f42c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f42c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f42c-128">-WhatIf</span></span>
<span data-ttu-id="2f42c-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f42c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f42c-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f42c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f42c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f42c-131">CommonParameters</span></span>
<span data-ttu-id="2f42c-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f42c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f42c-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f42c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f42c-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f42c-134">INPUTS</span></span>

### <span data-ttu-id="2f42c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2f42c-135">System.String</span></span>

### <span data-ttu-id="2f42c-136">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f42c-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2f42c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f42c-137">OUTPUTS</span></span>

### <span data-ttu-id="2f42c-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="2f42c-138">System.Void</span></span>

### <span data-ttu-id="2f42c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f42c-139">System.Boolean</span></span>

## <span data-ttu-id="2f42c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f42c-140">NOTES</span></span>

## <span data-ttu-id="2f42c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f42c-141">RELATED LINKS</span></span>