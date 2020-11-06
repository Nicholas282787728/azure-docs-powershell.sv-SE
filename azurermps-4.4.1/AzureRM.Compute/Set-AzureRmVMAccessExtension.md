---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573673"
---
# <span data-ttu-id="bb3e1-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bb3e1-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="bb3e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb3e1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3e1-103">Lägger till VMAccess-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb3e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb3e1-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb3e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb3e1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb3e1-106">Cmdleten **set-AzureRmVMAccessExtension** lägger till tillägget virtuell dator åtkomst (VMAccess) för virtuell dator till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="bb3e1-107">VMAccess kan återställa den virtuella datorns användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="bb3e1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb3e1-108">EXAMPLES</span></span>

### <span data-ttu-id="bb3e1-109">Exempel 1: lägga till ett VMAccess-tillägg</span><span class="sxs-lookup"><span data-stu-id="bb3e1-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="bb3e1-110">Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="bb3e1-111">Kommandot anger namn och typ av hanterarmappning för VMAccess.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="bb3e1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb3e1-112">PARAMETERS</span></span>

### <span data-ttu-id="bb3e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3e1-113">-DefaultProfile</span></span>
<span data-ttu-id="bb3e1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb3e1-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bb3e1-115">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="bb3e1-116">-ForceRerun</span></span>
<span data-ttu-id="bb3e1-117">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="bb3e1-118">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="bb3e1-119">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="bb3e1-120">-Location</span></span>
<span data-ttu-id="bb3e1-121">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-121">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb3e1-122">-Name</span></span>
<span data-ttu-id="bb3e1-123">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-123">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-124">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="bb3e1-124">-Password</span></span>
<span data-ttu-id="bb3e1-125">Anger det nya lösen ordet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-125">Specifies the new password of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb3e1-127">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bb3e1-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bb3e1-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="bb3e1-129">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="bb3e1-130">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="bb3e1-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-131">-UserName</span><span class="sxs-lookup"><span data-stu-id="bb3e1-131">-UserName</span></span>
<span data-ttu-id="bb3e1-132">Anger det nya användar namnet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-132">Specifies the new user name for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="bb3e1-133">-VMName</span></span>
<span data-ttu-id="bb3e1-134">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bb3e1-135">Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb3e1-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb3e1-136">-Confirm</span></span>
<span data-ttu-id="bb3e1-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb3e1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb3e1-138">-WhatIf</span></span>
<span data-ttu-id="bb3e1-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bb3e1-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb3e1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3e1-141">CommonParameters</span></span>
<span data-ttu-id="bb3e1-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3e1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3e1-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3e1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3e1-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb3e1-144">INPUTS</span></span>

## <span data-ttu-id="bb3e1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb3e1-145">OUTPUTS</span></span>

## <span data-ttu-id="bb3e1-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb3e1-146">NOTES</span></span>

## <span data-ttu-id="bb3e1-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb3e1-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb3e1-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bb3e1-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="bb3e1-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bb3e1-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="bb3e1-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="bb3e1-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="bb3e1-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="bb3e1-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


