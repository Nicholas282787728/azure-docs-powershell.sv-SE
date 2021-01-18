---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524457"
---
# <span data-ttu-id="fa54c-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fa54c-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="fa54c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa54c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa54c-103">Lägger till ett AD-domännamn till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="fa54c-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="fa54c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa54c-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa54c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa54c-105">DESCRIPTION</span></span>
<span data-ttu-id="fa54c-106">Cmdleten **set-AzVMADDomainExtension** lägger till en virtuell dator i Azure Active Directory (AD)-domän</span><span class="sxs-lookup"><span data-stu-id="fa54c-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="fa54c-107">Det här tillägget gör att den virtuella datorn kan anslutas till en domän.</span><span class="sxs-lookup"><span data-stu-id="fa54c-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="fa54c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa54c-108">EXAMPLES</span></span>

## <span data-ttu-id="fa54c-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa54c-109">PARAMETERS</span></span>

### <span data-ttu-id="fa54c-110">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="fa54c-110">-Credential</span></span>
<span data-ttu-id="fa54c-111">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fa54c-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="fa54c-112">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fa54c-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fa54c-113">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fa54c-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="fa54c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa54c-114">-DefaultProfile</span></span>
<span data-ttu-id="fa54c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa54c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa54c-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fa54c-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fa54c-117">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="fa54c-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="fa54c-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="fa54c-118">-DomainName</span></span>
<span data-ttu-id="fa54c-119">Anger namnet på domänen.</span><span class="sxs-lookup"><span data-stu-id="fa54c-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="fa54c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fa54c-120">-ForceRerun</span></span>
<span data-ttu-id="fa54c-121">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="fa54c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="fa54c-122">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="fa54c-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="fa54c-123">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="fa54c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="fa54c-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="fa54c-124">-JoinOption</span></span>
<span data-ttu-id="fa54c-125">Anger alternativet för koppling.</span><span class="sxs-lookup"><span data-stu-id="fa54c-125">Specifies the join option.</span></span> <span data-ttu-id="fa54c-126">För kopplings alternativ se [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="fa54c-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="fa54c-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="fa54c-127">-Location</span></span>
<span data-ttu-id="fa54c-128">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fa54c-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="fa54c-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa54c-129">-Name</span></span>
<span data-ttu-id="fa54c-130">Anger namnet på den domän som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="fa54c-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="fa54c-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fa54c-131">-NoWait</span></span>
<span data-ttu-id="fa54c-132">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="fa54c-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="fa54c-133">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="fa54c-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="fa54c-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="fa54c-134">-OUPath</span></span>
<span data-ttu-id="fa54c-135">Anger en organisationsenhet (OU) för domän kontot.</span><span class="sxs-lookup"><span data-stu-id="fa54c-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="fa54c-136">Ange ORGANISATIONSENHETens fullständiga unika namn inom citat tecken.</span><span class="sxs-lookup"><span data-stu-id="fa54c-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="fa54c-137">Standardvärdet är standard-OU för dator objekt i domänen.</span><span class="sxs-lookup"><span data-stu-id="fa54c-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="fa54c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa54c-138">-ResourceGroupName</span></span>
<span data-ttu-id="fa54c-139">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fa54c-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fa54c-140">-Starta om</span><span class="sxs-lookup"><span data-stu-id="fa54c-140">-Restart</span></span>
<span data-ttu-id="fa54c-141">Anger att den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fa54c-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="fa54c-142">En omstart krävs ofta för att ändringen ska träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="fa54c-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="fa54c-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fa54c-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="fa54c-144">Anger domän tilläggets version.</span><span class="sxs-lookup"><span data-stu-id="fa54c-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="fa54c-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="fa54c-145">-VMName</span></span>
<span data-ttu-id="fa54c-146">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fa54c-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fa54c-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa54c-147">-Confirm</span></span>
<span data-ttu-id="fa54c-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa54c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa54c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa54c-149">-WhatIf</span></span>
<span data-ttu-id="fa54c-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa54c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa54c-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa54c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa54c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa54c-152">CommonParameters</span></span>
<span data-ttu-id="fa54c-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa54c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa54c-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa54c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa54c-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa54c-155">INPUTS</span></span>

### <span data-ttu-id="fa54c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="fa54c-156">System.String</span></span>

### <span data-ttu-id="fa54c-157">System. Nullable ' 1 [[system. UInt32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fa54c-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fa54c-158">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="fa54c-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="fa54c-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa54c-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa54c-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa54c-160">OUTPUTS</span></span>

### <span data-ttu-id="fa54c-161">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fa54c-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fa54c-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa54c-162">NOTES</span></span>

## <span data-ttu-id="fa54c-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa54c-163">RELATED LINKS</span></span>

[<span data-ttu-id="fa54c-164">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fa54c-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)
