---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssAdditionalUnattendContent.md
ms.openlocfilehash: de61efcbabb2e5acd7d82bf7a1cec8341fe06433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575721"
---
# <span data-ttu-id="1514a-101">Add-AzureRmVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="1514a-101">Add-AzureRmVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="1514a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1514a-102">SYNOPSIS</span></span>
<span data-ttu-id="1514a-103">Lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="1514a-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1514a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1514a-104">SYNTAX</span></span>

```
Add-AzureRmVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1514a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1514a-105">DESCRIPTION</span></span>
<span data-ttu-id="1514a-106">Cmdleten **Add-AzureRmVmssAdditionalUnattendContent** lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="1514a-106">The **Add-AzureRmVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1514a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1514a-107">EXAMPLES</span></span>

### <span data-ttu-id="1514a-108">Exempel 1: lägga till information i svars filen för obevakad Windows-installation</span><span class="sxs-lookup"><span data-stu-id="1514a-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzureRmVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="1514a-109">Det här kommandot lägger till information i svars filen för obevakad Windows-installation.</span><span class="sxs-lookup"><span data-stu-id="1514a-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="1514a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1514a-110">PARAMETERS</span></span>

### <span data-ttu-id="1514a-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="1514a-111">-ComponentName</span></span>
<span data-ttu-id="1514a-112">Anger namnet på den komponent som ska konfigureras med det tillagda innehållet.</span><span class="sxs-lookup"><span data-stu-id="1514a-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="1514a-113">Det enda tillåtna värdet är Microsoft-Windows-Shell-Setup.</span><span class="sxs-lookup"><span data-stu-id="1514a-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: ComponentNames
Parameter Sets: (All)
Aliases: 
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-114">-Innehåll</span><span class="sxs-lookup"><span data-stu-id="1514a-114">-Content</span></span>
<span data-ttu-id="1514a-115">Anger det XML-formaterade innehåll som läggs till i unattend.xml filen för den angivna sökvägen och komponenten.</span><span class="sxs-lookup"><span data-stu-id="1514a-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-116">-PassName</span><span class="sxs-lookup"><span data-stu-id="1514a-116">-PassName</span></span>
<span data-ttu-id="1514a-117">Anger namnet på det pass som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="1514a-117">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="1514a-118">Det enda tillåtna värdet är oobeSystem.</span><span class="sxs-lookup"><span data-stu-id="1514a-118">The only allowable value is oobeSystem.</span></span>

```yaml
Type: PassNames
Parameter Sets: (All)
Aliases: 
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-119">-SettingName</span><span class="sxs-lookup"><span data-stu-id="1514a-119">-SettingName</span></span>
<span data-ttu-id="1514a-120">Anger namnet på den inställning som innehållet gäller för.</span><span class="sxs-lookup"><span data-stu-id="1514a-120">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="1514a-121">De acceptabla värdena för den här parametern är::</span><span class="sxs-lookup"><span data-stu-id="1514a-121">The acceptable values for this parameter are::</span></span>

- <span data-ttu-id="1514a-122">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="1514a-122">FirstLogonCommands</span></span>
- <span data-ttu-id="1514a-123">Automatisk inloggning</span><span class="sxs-lookup"><span data-stu-id="1514a-123">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1514a-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1514a-125">Ange den virtuella datorns **skal uppsättnings** objekt.</span><span class="sxs-lookup"><span data-stu-id="1514a-125">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="1514a-126">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="1514a-126">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1514a-127">-Confirm</span></span>
<span data-ttu-id="1514a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1514a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1514a-129">-WhatIf</span></span>
<span data-ttu-id="1514a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1514a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1514a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1514a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1514a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1514a-132">CommonParameters</span></span>
<span data-ttu-id="1514a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1514a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1514a-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1514a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1514a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1514a-135">INPUTS</span></span>

### <span data-ttu-id="1514a-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="1514a-136">None</span></span>
<span data-ttu-id="1514a-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1514a-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1514a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1514a-138">OUTPUTS</span></span>

## <span data-ttu-id="1514a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1514a-139">NOTES</span></span>

## <span data-ttu-id="1514a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1514a-140">RELATED LINKS</span></span>

[<span data-ttu-id="1514a-141">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1514a-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
