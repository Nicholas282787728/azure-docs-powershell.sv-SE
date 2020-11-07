---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: fed235e3c628ab245ae74299cf395e4501b141f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744959"
---
# <span data-ttu-id="77000-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="77000-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="77000-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77000-102">SYNOPSIS</span></span>
<span data-ttu-id="77000-103">Lägger till ett AD-domännamn till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="77000-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="77000-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77000-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77000-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77000-105">DESCRIPTION</span></span>
<span data-ttu-id="77000-106">Cmdleten **set-AzVMADDomainExtension** lägger till en virtuell dator i Azure Active Directory (AD)-domän</span><span class="sxs-lookup"><span data-stu-id="77000-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="77000-107">Det här tillägget gör att den virtuella datorn kan anslutas till en domän.</span><span class="sxs-lookup"><span data-stu-id="77000-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="77000-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77000-108">EXAMPLES</span></span>

## <span data-ttu-id="77000-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77000-109">PARAMETERS</span></span>

### <span data-ttu-id="77000-110">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="77000-110">-Credential</span></span>
<span data-ttu-id="77000-111">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="77000-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="77000-112">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="77000-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="77000-113">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="77000-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77000-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77000-114">-DefaultProfile</span></span>
<span data-ttu-id="77000-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77000-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77000-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="77000-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="77000-117">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="77000-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="77000-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="77000-118">-DomainName</span></span>
<span data-ttu-id="77000-119">Anger namnet på domänen.</span><span class="sxs-lookup"><span data-stu-id="77000-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77000-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="77000-120">-ForceRerun</span></span>
<span data-ttu-id="77000-121">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="77000-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="77000-122">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="77000-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="77000-123">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="77000-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="77000-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="77000-124">-JoinOption</span></span>
<span data-ttu-id="77000-125">Anger alternativet för koppling.</span><span class="sxs-lookup"><span data-stu-id="77000-125">Specifies the join option.</span></span> <span data-ttu-id="77000-126">För kopplings alternativ se [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="77000-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77000-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="77000-127">-Location</span></span>
<span data-ttu-id="77000-128">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="77000-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="77000-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="77000-129">-Name</span></span>
<span data-ttu-id="77000-130">Anger namnet på den domän som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="77000-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="77000-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="77000-131">-NoWait</span></span>
<span data-ttu-id="77000-132">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="77000-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="77000-133">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="77000-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="77000-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="77000-134">-OUPath</span></span>
<span data-ttu-id="77000-135">Anger en organisationsenhet (OU) för domän kontot.</span><span class="sxs-lookup"><span data-stu-id="77000-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="77000-136">Ange ORGANISATIONSENHETens fullständiga unika namn inom citat tecken.</span><span class="sxs-lookup"><span data-stu-id="77000-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="77000-137">Standardvärdet är standard-OU för dator objekt i domänen.</span><span class="sxs-lookup"><span data-stu-id="77000-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="77000-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77000-138">-ResourceGroupName</span></span>
<span data-ttu-id="77000-139">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="77000-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="77000-140">-Starta om</span><span class="sxs-lookup"><span data-stu-id="77000-140">-Restart</span></span>
<span data-ttu-id="77000-141">Anger att den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="77000-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="77000-142">En omstart krävs ofta för att ändringen ska träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="77000-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="77000-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="77000-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="77000-144">Anger domän tilläggets version.</span><span class="sxs-lookup"><span data-stu-id="77000-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="77000-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="77000-145">-VMName</span></span>
<span data-ttu-id="77000-146">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="77000-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="77000-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="77000-147">-Confirm</span></span>
<span data-ttu-id="77000-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="77000-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77000-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77000-149">-WhatIf</span></span>
<span data-ttu-id="77000-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="77000-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77000-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="77000-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77000-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77000-152">CommonParameters</span></span>
<span data-ttu-id="77000-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77000-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77000-154">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77000-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77000-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77000-155">INPUTS</span></span>

### <span data-ttu-id="77000-156">System. String</span><span class="sxs-lookup"><span data-stu-id="77000-156">System.String</span></span>

### <span data-ttu-id="77000-157">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77000-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77000-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="77000-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="77000-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77000-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77000-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77000-160">OUTPUTS</span></span>

### <span data-ttu-id="77000-161">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="77000-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="77000-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77000-162">NOTES</span></span>

## <span data-ttu-id="77000-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77000-163">RELATED LINKS</span></span>

[<span data-ttu-id="77000-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="77000-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
