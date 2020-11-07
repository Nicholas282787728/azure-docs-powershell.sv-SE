---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: f84d9f823d97872d8ad2491a2ab45ef3bb5a22a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925294"
---
# <span data-ttu-id="32811-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="32811-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="32811-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="32811-102">SYNOPSIS</span></span>
<span data-ttu-id="32811-103">Lägger till ett diagnostikverktyg i VMSS.</span><span class="sxs-lookup"><span data-stu-id="32811-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="32811-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="32811-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32811-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="32811-105">DESCRIPTION</span></span>
<span data-ttu-id="32811-106">Cmdleten **Add-AzVmssDiagnosticsExtension** lägger till ett Diagnostics-tillägg till instansen för virtuell dator Scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="32811-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="32811-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="32811-107">EXAMPLES</span></span>

### <span data-ttu-id="32811-108">Exempel 1: lägga till ett tillägg i VMSS</span><span class="sxs-lookup"><span data-stu-id="32811-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="32811-109">Det här kommandot lägger till ett diagnostiktest i VMSS.</span><span class="sxs-lookup"><span data-stu-id="32811-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="32811-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="32811-110">PARAMETERS</span></span>

### <span data-ttu-id="32811-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="32811-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="32811-112">Anger om den här cmdleten gör att Azure gästs agenten automatiskt kan uppdatera tillägget till en nyare del version.</span><span class="sxs-lookup"><span data-stu-id="32811-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32811-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32811-113">-DefaultProfile</span></span>
<span data-ttu-id="32811-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="32811-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32811-115">-Force</span><span class="sxs-lookup"><span data-stu-id="32811-115">-Force</span></span>
<span data-ttu-id="32811-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="32811-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32811-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="32811-117">-Name</span></span>
<span data-ttu-id="32811-118">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="32811-118">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32811-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="32811-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="32811-120">Anger sökvägen till den privata konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="32811-120">Specifies the path of the private configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32811-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="32811-121">-SettingFilePath</span></span>
<span data-ttu-id="32811-122">Anger sökvägen till den offentliga konfigurations filen.</span><span class="sxs-lookup"><span data-stu-id="32811-122">Specifies the path of the public configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32811-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="32811-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="32811-124">Anger vilken version av tillägget som ska användas för denna VMSS.</span><span class="sxs-lookup"><span data-stu-id="32811-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="32811-125">För att få tag i versionen kör du cmdleten [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) med värdet Microsoft. Azure. Diagnostics för parametern *PublisherName* och IaaSDiagnostics för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="32811-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32811-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32811-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="32811-127">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="32811-127">Specify the VMSS object.</span></span>
<span data-ttu-id="32811-128">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="32811-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="32811-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="32811-129">-Confirm</span></span>
<span data-ttu-id="32811-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="32811-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32811-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32811-131">-WhatIf</span></span>
<span data-ttu-id="32811-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="32811-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32811-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="32811-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32811-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32811-134">CommonParameters</span></span>
<span data-ttu-id="32811-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32811-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32811-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32811-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32811-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="32811-137">INPUTS</span></span>

### <span data-ttu-id="32811-138">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32811-138">VirtualMachineScaleSet</span></span>
<span data-ttu-id="32811-139">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="32811-139">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="32811-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="32811-140">OUTPUTS</span></span>

###  
<span data-ttu-id="32811-141">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="32811-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="32811-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="32811-142">NOTES</span></span>

## <span data-ttu-id="32811-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="32811-143">RELATED LINKS</span></span>

[<span data-ttu-id="32811-144">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="32811-144">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="32811-145">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="32811-145">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="32811-146">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="32811-146">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
