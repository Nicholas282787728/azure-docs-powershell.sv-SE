---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524560"
---
# <span data-ttu-id="2c573-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="2c573-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="2c573-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c573-102">SYNOPSIS</span></span>
<span data-ttu-id="2c573-103">Lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="2c573-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="2c573-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c573-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c573-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c573-105">DESCRIPTION</span></span>
<span data-ttu-id="2c573-106">Cmdleten **Add-AzVmssAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="2c573-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="2c573-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c573-107">EXAMPLES</span></span>

### <span data-ttu-id="2c573-108">Exempel 1: lägga till information i svars filen för obevakad Windows-installation</span><span class="sxs-lookup"><span data-stu-id="2c573-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="2c573-109">Det här kommandot lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="2c573-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="2c573-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c573-110">PARAMETERS</span></span>

### <span data-ttu-id="2c573-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2c573-111">-ComponentName</span></span>
<span data-ttu-id="2c573-112">Anger namnet på den komponent som ska konfigureras med det tillagda innehållet.</span><span class="sxs-lookup"><span data-stu-id="2c573-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="2c573-113">Det enda tillåtna värdet är Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="2c573-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c573-114">-Innehåll</span><span class="sxs-lookup"><span data-stu-id="2c573-114">-Content</span></span>
<span data-ttu-id="2c573-115">Anger det XML-formaterade innehåll som läggs till i unattend.xml filen för den angivna sökvägen och komponenten.</span><span class="sxs-lookup"><span data-stu-id="2c573-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c573-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c573-116">-DefaultProfile</span></span>
<span data-ttu-id="2c573-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c573-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c573-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="2c573-118">-PassName</span></span>
<span data-ttu-id="2c573-119">Anger namnet på det pass som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="2c573-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="2c573-120">Det enda tillåtna värdet är oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="2c573-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c573-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="2c573-121">-SettingName</span></span>
<span data-ttu-id="2c573-122">Anger namnet på den inställning som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="2c573-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="2c573-123">De acceptabla värdena för den här parametern är::</span><span class="sxs-lookup"><span data-stu-id="2c573-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="2c573-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="2c573-124">FirstLogonCommands</span></span>
- <span data-ttu-id="2c573-125">Automatisk inloggning</span><span class="sxs-lookup"><span data-stu-id="2c573-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c573-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c573-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2c573-127">Ange den virtuella datorns **skal uppsättnings** objekt.</span><span class="sxs-lookup"><span data-stu-id="2c573-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="2c573-128">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="2c573-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c573-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c573-129">-Confirm</span></span>
<span data-ttu-id="2c573-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c573-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c573-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c573-131">-WhatIf</span></span>
<span data-ttu-id="2c573-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c573-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c573-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c573-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c573-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c573-134">CommonParameters</span></span>
<span data-ttu-id="2c573-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c573-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c573-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c573-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c573-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c573-137">INPUTS</span></span>

### <span data-ttu-id="2c573-138">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c573-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2c573-139">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. PassNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2c573-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2c573-140">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ComponentNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2c573-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2c573-141">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. SettingNames, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2c573-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2c573-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2c573-142">System.String</span></span>

## <span data-ttu-id="2c573-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c573-143">OUTPUTS</span></span>

### <span data-ttu-id="2c573-144">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c573-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2c573-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c573-145">NOTES</span></span>

## <span data-ttu-id="2c573-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c573-146">RELATED LINKS</span></span>

[<span data-ttu-id="2c573-147">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2c573-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
