---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930269"
---
# <span data-ttu-id="b714d-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b714d-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="b714d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b714d-102">SYNOPSIS</span></span>
<span data-ttu-id="b714d-103">Lägger till VMAccess-tillägget på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b714d-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b714d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b714d-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b714d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b714d-105">DESCRIPTION</span></span>
<span data-ttu-id="b714d-106">Cmdleten **set-AzureRmVMAccessExtension** lägger till den virtuella datorns VMAccess-tillägg till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b714d-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="b714d-107">VMAccess-tillägget kan användas för att ange ett tillfälligt lösen ord och det bör ändras direkt efter att du har loggat in på datorn.</span><span class="sxs-lookup"><span data-stu-id="b714d-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="b714d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b714d-108">EXAMPLES</span></span>

### <span data-ttu-id="b714d-109">Exempel 1: lägga till ett VMAccess-tillägg</span><span class="sxs-lookup"><span data-stu-id="b714d-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="b714d-110">Det här kommandot lägger till ett VMAccess-tillägg för den virtuella datorn med namnet VirtualMachine07 i ResrouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b714d-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="b714d-111">Kommandot anger namn och typ av hanterarmappning för VMAccess.</span><span class="sxs-lookup"><span data-stu-id="b714d-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="b714d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b714d-112">PARAMETERS</span></span>

### <span data-ttu-id="b714d-113">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="b714d-113">-Credential</span></span>
<span data-ttu-id="b714d-114">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b714d-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="b714d-115">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="b714d-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b714d-116">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b714d-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b714d-117">-DefaultProfile</span></span>
<span data-ttu-id="b714d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b714d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b714d-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b714d-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="b714d-120">-ForceRerun</span></span>
<span data-ttu-id="b714d-121">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="b714d-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="b714d-122">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="b714d-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="b714d-123">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="b714d-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="b714d-124">-Location</span></span>
<span data-ttu-id="b714d-125">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b714d-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b714d-126">-Name</span></span>
<span data-ttu-id="b714d-127">Anger namnet på tillägget som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b714d-127">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b714d-128">-ResourceGroupName</span></span>
<span data-ttu-id="b714d-129">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b714d-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b714d-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="b714d-131">Anger vilken version av tillägget som ska användas för den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b714d-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="b714d-132">För att hämta versionen kör du Get-AzureRmVMExtensionImage cmdlet med värdet Microsoft. Compute for the *PublisherName* parameter och VMAccessAgent för parametern *Type* .</span><span class="sxs-lookup"><span data-stu-id="b714d-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="b714d-133">-VMName</span></span>
<span data-ttu-id="b714d-134">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b714d-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b714d-135">Denna cmdlet lägger till VMAccess för den virtuella datorn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b714d-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b714d-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b714d-136">-Confirm</span></span>
<span data-ttu-id="b714d-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b714d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b714d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b714d-138">-WhatIf</span></span>
<span data-ttu-id="b714d-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b714d-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b714d-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b714d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b714d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b714d-141">CommonParameters</span></span>
<span data-ttu-id="b714d-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b714d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b714d-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b714d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b714d-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b714d-144">INPUTS</span></span>

### <span data-ttu-id="b714d-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="b714d-145">None</span></span>
<span data-ttu-id="b714d-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b714d-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b714d-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b714d-147">OUTPUTS</span></span>

### <span data-ttu-id="b714d-148">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b714d-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b714d-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b714d-149">NOTES</span></span>

## <span data-ttu-id="b714d-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b714d-150">RELATED LINKS</span></span>

[<span data-ttu-id="b714d-151">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b714d-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b714d-152">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b714d-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b714d-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b714d-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="b714d-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b714d-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


