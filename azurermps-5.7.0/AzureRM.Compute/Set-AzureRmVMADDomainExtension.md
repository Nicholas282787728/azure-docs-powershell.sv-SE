---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573516"
---
# <span data-ttu-id="62345-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="62345-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="62345-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62345-102">SYNOPSIS</span></span>
<span data-ttu-id="62345-103">Lägger till ett AD-domännamn till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="62345-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62345-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62345-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62345-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62345-105">DESCRIPTION</span></span>
<span data-ttu-id="62345-106">Cmdleten **set-AzureRmVMADDomainExtension** lägger till en virtuell dator i Azure Active Directory (AD)-domän</span><span class="sxs-lookup"><span data-stu-id="62345-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="62345-107">Det här tillägget gör att den virtuella datorn kan anslutas till en domän.</span><span class="sxs-lookup"><span data-stu-id="62345-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="62345-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62345-108">EXAMPLES</span></span>

## <span data-ttu-id="62345-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62345-109">PARAMETERS</span></span>

### <span data-ttu-id="62345-110">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="62345-110">-Credential</span></span>
<span data-ttu-id="62345-111">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62345-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="62345-112">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="62345-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="62345-113">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="62345-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="62345-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="62345-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="62345-115">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="62345-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="62345-116">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="62345-116">-DomainName</span></span>
<span data-ttu-id="62345-117">Anger namnet på domänen.</span><span class="sxs-lookup"><span data-stu-id="62345-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62345-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="62345-118">-ForceRerun</span></span>
<span data-ttu-id="62345-119">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="62345-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="62345-120">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="62345-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="62345-121">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="62345-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="62345-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="62345-122">-JoinOption</span></span>
<span data-ttu-id="62345-123">Anger alternativet för koppling.</span><span class="sxs-lookup"><span data-stu-id="62345-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62345-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="62345-124">-Location</span></span>
<span data-ttu-id="62345-125">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="62345-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="62345-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="62345-126">-Name</span></span>
<span data-ttu-id="62345-127">Anger namnet på den domän som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="62345-127">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="62345-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="62345-128">-OUPath</span></span>
<span data-ttu-id="62345-129">Anger en organisationsenhet (OU) för domän kontot.</span><span class="sxs-lookup"><span data-stu-id="62345-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="62345-130">Ange ORGANISATIONSENHETens fullständiga unika namn inom citat tecken.</span><span class="sxs-lookup"><span data-stu-id="62345-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="62345-131">Standardvärdet är standard-OU för dator objekt i domänen.</span><span class="sxs-lookup"><span data-stu-id="62345-131">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="62345-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62345-132">-ResourceGroupName</span></span>
<span data-ttu-id="62345-133">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="62345-133">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="62345-134">-Starta om</span><span class="sxs-lookup"><span data-stu-id="62345-134">-Restart</span></span>
<span data-ttu-id="62345-135">Anger att den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="62345-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="62345-136">En omstart krävs ofta för att ändringen ska träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="62345-136">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="62345-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="62345-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="62345-138">Anger domän tilläggets version.</span><span class="sxs-lookup"><span data-stu-id="62345-138">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="62345-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="62345-139">-VMName</span></span>
<span data-ttu-id="62345-140">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="62345-140">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="62345-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62345-141">-Confirm</span></span>
<span data-ttu-id="62345-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62345-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62345-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62345-143">-WhatIf</span></span>
<span data-ttu-id="62345-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62345-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="62345-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62345-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62345-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62345-146">CommonParameters</span></span>
<span data-ttu-id="62345-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62345-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62345-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62345-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62345-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62345-149">INPUTS</span></span>

### <span data-ttu-id="62345-150">Ingen</span><span class="sxs-lookup"><span data-stu-id="62345-150">None</span></span>
<span data-ttu-id="62345-151">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="62345-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62345-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62345-152">OUTPUTS</span></span>

## <span data-ttu-id="62345-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62345-153">NOTES</span></span>

## <span data-ttu-id="62345-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62345-154">RELATED LINKS</span></span>

[<span data-ttu-id="62345-155">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="62345-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
