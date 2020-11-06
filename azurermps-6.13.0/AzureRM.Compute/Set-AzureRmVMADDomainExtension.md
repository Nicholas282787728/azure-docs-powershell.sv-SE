---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585040"
---
# <span data-ttu-id="64da0-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="64da0-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="64da0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64da0-102">SYNOPSIS</span></span>
<span data-ttu-id="64da0-103">Lägger till ett AD-domännamn till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="64da0-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64da0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64da0-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64da0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64da0-105">DESCRIPTION</span></span>
<span data-ttu-id="64da0-106">Cmdleten **set-AzureRmVMADDomainExtension** lägger till en virtuell dator i Azure Active Directory (AD)-domän</span><span class="sxs-lookup"><span data-stu-id="64da0-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="64da0-107">Det här tillägget gör att den virtuella datorn kan anslutas till en domän.</span><span class="sxs-lookup"><span data-stu-id="64da0-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="64da0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64da0-108">EXAMPLES</span></span>

## <span data-ttu-id="64da0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64da0-109">PARAMETERS</span></span>

### <span data-ttu-id="64da0-110">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="64da0-110">-Credential</span></span>
<span data-ttu-id="64da0-111">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="64da0-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="64da0-112">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="64da0-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="64da0-113">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="64da0-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="64da0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64da0-114">-DefaultProfile</span></span>
<span data-ttu-id="64da0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64da0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64da0-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="64da0-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="64da0-117">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="64da0-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="64da0-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="64da0-118">-DomainName</span></span>
<span data-ttu-id="64da0-119">Anger namnet på domänen.</span><span class="sxs-lookup"><span data-stu-id="64da0-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="64da0-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="64da0-120">-ForceRerun</span></span>
<span data-ttu-id="64da0-121">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="64da0-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="64da0-122">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="64da0-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="64da0-123">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="64da0-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="64da0-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="64da0-124">-JoinOption</span></span>
<span data-ttu-id="64da0-125">Anger alternativet för koppling.</span><span class="sxs-lookup"><span data-stu-id="64da0-125">Specifies the join option.</span></span> <span data-ttu-id="64da0-126">För kopplings alternativ se [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="64da0-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="64da0-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="64da0-127">-Location</span></span>
<span data-ttu-id="64da0-128">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64da0-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="64da0-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="64da0-129">-Name</span></span>
<span data-ttu-id="64da0-130">Anger namnet på den domän som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="64da0-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="64da0-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="64da0-131">-OUPath</span></span>
<span data-ttu-id="64da0-132">Anger en organisationsenhet (OU) för domän kontot.</span><span class="sxs-lookup"><span data-stu-id="64da0-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="64da0-133">Ange ORGANISATIONSENHETens fullständiga unika namn inom citat tecken.</span><span class="sxs-lookup"><span data-stu-id="64da0-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="64da0-134">Standardvärdet är standard-OU för dator objekt i domänen.</span><span class="sxs-lookup"><span data-stu-id="64da0-134">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="64da0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64da0-135">-ResourceGroupName</span></span>
<span data-ttu-id="64da0-136">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64da0-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64da0-137">-Starta om</span><span class="sxs-lookup"><span data-stu-id="64da0-137">-Restart</span></span>
<span data-ttu-id="64da0-138">Anger att den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64da0-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="64da0-139">En omstart krävs ofta för att ändringen ska träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="64da0-139">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="64da0-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="64da0-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="64da0-141">Anger domän tilläggets version.</span><span class="sxs-lookup"><span data-stu-id="64da0-141">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="64da0-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="64da0-142">-VMName</span></span>
<span data-ttu-id="64da0-143">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="64da0-143">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="64da0-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64da0-144">-Confirm</span></span>
<span data-ttu-id="64da0-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64da0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64da0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64da0-146">-WhatIf</span></span>
<span data-ttu-id="64da0-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64da0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64da0-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64da0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64da0-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64da0-149">CommonParameters</span></span>
<span data-ttu-id="64da0-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64da0-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64da0-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64da0-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64da0-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64da0-152">INPUTS</span></span>

### <span data-ttu-id="64da0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="64da0-153">System.String</span></span>

### <span data-ttu-id="64da0-154">System. Nullable ' 1 [[system. UInt32, mscorlib, version = 4.0.0.0; Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="64da0-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="64da0-155">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="64da0-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="64da0-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="64da0-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="64da0-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64da0-157">OUTPUTS</span></span>

### <span data-ttu-id="64da0-158">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="64da0-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="64da0-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64da0-159">NOTES</span></span>

## <span data-ttu-id="64da0-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64da0-160">RELATED LINKS</span></span>

[<span data-ttu-id="64da0-161">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="64da0-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
