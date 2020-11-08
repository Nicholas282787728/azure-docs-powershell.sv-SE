---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101145"
---
# <span data-ttu-id="55ee0-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ee0-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="55ee0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="55ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="55ee0-103">Tar bort en konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="55ee0-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="55ee0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="55ee0-104">SYNTAX</span></span>

### <span data-ttu-id="55ee0-105">BySucName (standard)</span><span class="sxs-lookup"><span data-stu-id="55ee0-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55ee0-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="55ee0-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55ee0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="55ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="55ee0-108">Denna cmdlet tog bort en konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="55ee0-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="55ee0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="55ee0-109">EXAMPLES</span></span>

### <span data-ttu-id="55ee0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="55ee0-110">Example 1</span></span>
<span data-ttu-id="55ee0-111">Det här exemplet visar hur du tar bort ' MyUpdateConfiguration ' från Automation-konto</span><span class="sxs-lookup"><span data-stu-id="55ee0-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="55ee0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="55ee0-112">PARAMETERS</span></span>

### <span data-ttu-id="55ee0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55ee0-113">-AutomationAccountName</span></span>
<span data-ttu-id="55ee0-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="55ee0-114">The automation account name.</span></span>

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

### <span data-ttu-id="55ee0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ee0-115">-DefaultProfile</span></span>
<span data-ttu-id="55ee0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="55ee0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ee0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="55ee0-117">-Name</span></span>
<span data-ttu-id="55ee0-118">Namn på program uppdaterings konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="55ee0-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="55ee0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55ee0-119">-PassThru</span></span>
<span data-ttu-id="55ee0-120">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="55ee0-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="55ee0-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="55ee0-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55ee0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ee0-122">-ResourceGroupName</span></span>
<span data-ttu-id="55ee0-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="55ee0-123">The resource group name.</span></span>

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

### <span data-ttu-id="55ee0-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ee0-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="55ee0-125">Program uppdaterings konfigurationen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="55ee0-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="55ee0-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="55ee0-126">-Confirm</span></span>
<span data-ttu-id="55ee0-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="55ee0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55ee0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55ee0-128">-WhatIf</span></span>
<span data-ttu-id="55ee0-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="55ee0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55ee0-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="55ee0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55ee0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ee0-131">CommonParameters</span></span>
<span data-ttu-id="55ee0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ee0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ee0-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ee0-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ee0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="55ee0-134">INPUTS</span></span>

### <span data-ttu-id="55ee0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="55ee0-135">System.String</span></span>

### <span data-ttu-id="55ee0-136">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="55ee0-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="55ee0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="55ee0-137">OUTPUTS</span></span>

### <span data-ttu-id="55ee0-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="55ee0-138">System.Void</span></span>

### <span data-ttu-id="55ee0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55ee0-139">System.Boolean</span></span>

## <span data-ttu-id="55ee0-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="55ee0-140">NOTES</span></span>

## <span data-ttu-id="55ee0-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="55ee0-141">RELATED LINKS</span></span>
