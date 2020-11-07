---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 140f1ccdedd6f3b3402601a8a844092bf3d7ab0e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931025"
---
# <span data-ttu-id="1064f-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1064f-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="1064f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1064f-102">SYNOPSIS</span></span>
<span data-ttu-id="1064f-103">Lägger till ett AD-domännamn till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="1064f-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1064f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1064f-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1064f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1064f-105">DESCRIPTION</span></span>
<span data-ttu-id="1064f-106">Cmdleten **set-AzureRmVMADDomainExtension** lägger till en virtuell dator i Azure Active Directory (AD)-domän</span><span class="sxs-lookup"><span data-stu-id="1064f-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="1064f-107">Det här tillägget gör att den virtuella datorn kan anslutas till en domän.</span><span class="sxs-lookup"><span data-stu-id="1064f-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="1064f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1064f-108">EXAMPLES</span></span>

## <span data-ttu-id="1064f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1064f-109">PARAMETERS</span></span>

### <span data-ttu-id="1064f-110">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="1064f-110">-Credential</span></span>
<span data-ttu-id="1064f-111">Anger användar namn och lösen ord för den virtuella datorn som ett **PSCredential** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1064f-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1064f-112">För att få en autentiseringsuppgift, Använd cmdleten Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="1064f-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1064f-113">Om du vill ha mer information skriver du `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1064f-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="1064f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1064f-114">-DefaultProfile</span></span>
<span data-ttu-id="1064f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1064f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1064f-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1064f-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1064f-117">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="1064f-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="1064f-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="1064f-118">-DomainName</span></span>
<span data-ttu-id="1064f-119">Anger namnet på domänen.</span><span class="sxs-lookup"><span data-stu-id="1064f-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="1064f-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1064f-120">-ForceRerun</span></span>
<span data-ttu-id="1064f-121">Anger att denna cmdlet tvingar fram försök med samma tilläggs konfiguration på den virtuella datorn utan att avinstallera och installera om tillägget.</span><span class="sxs-lookup"><span data-stu-id="1064f-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1064f-122">Värdet kan vara en annan sträng än det aktuella värdet.</span><span class="sxs-lookup"><span data-stu-id="1064f-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="1064f-123">Om forceUpdateTag inte ändras används uppdateringarna för offentliga eller skyddade inställningar fortfarande av hanteraren.</span><span class="sxs-lookup"><span data-stu-id="1064f-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1064f-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="1064f-124">-JoinOption</span></span>
<span data-ttu-id="1064f-125">Anger alternativet för koppling.</span><span class="sxs-lookup"><span data-stu-id="1064f-125">Specifies the join option.</span></span>

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

### <span data-ttu-id="1064f-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="1064f-126">-Location</span></span>
<span data-ttu-id="1064f-127">Anger platsen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1064f-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1064f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1064f-128">-Name</span></span>
<span data-ttu-id="1064f-129">Anger namnet på den domän som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="1064f-129">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="1064f-130">-OUPath</span><span class="sxs-lookup"><span data-stu-id="1064f-130">-OUPath</span></span>
<span data-ttu-id="1064f-131">Anger en organisationsenhet (OU) för domän kontot.</span><span class="sxs-lookup"><span data-stu-id="1064f-131">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="1064f-132">Ange ORGANISATIONSENHETens fullständiga unika namn inom citat tecken.</span><span class="sxs-lookup"><span data-stu-id="1064f-132">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="1064f-133">Standardvärdet är standard-OU för dator objekt i domänen.</span><span class="sxs-lookup"><span data-stu-id="1064f-133">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="1064f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1064f-134">-ResourceGroupName</span></span>
<span data-ttu-id="1064f-135">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1064f-135">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1064f-136">-Starta om</span><span class="sxs-lookup"><span data-stu-id="1064f-136">-Restart</span></span>
<span data-ttu-id="1064f-137">Anger att den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1064f-137">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="1064f-138">En omstart krävs ofta för att ändringen ska träda i kraft.</span><span class="sxs-lookup"><span data-stu-id="1064f-138">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="1064f-139">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1064f-139">-TypeHandlerVersion</span></span>
<span data-ttu-id="1064f-140">Anger domän tilläggets version.</span><span class="sxs-lookup"><span data-stu-id="1064f-140">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="1064f-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="1064f-141">-VMName</span></span>
<span data-ttu-id="1064f-142">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1064f-142">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1064f-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1064f-143">-Confirm</span></span>
<span data-ttu-id="1064f-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1064f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1064f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1064f-145">-WhatIf</span></span>
<span data-ttu-id="1064f-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1064f-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1064f-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1064f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1064f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1064f-148">CommonParameters</span></span>
<span data-ttu-id="1064f-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1064f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1064f-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1064f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1064f-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1064f-151">INPUTS</span></span>

### <span data-ttu-id="1064f-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="1064f-152">None</span></span>
<span data-ttu-id="1064f-153">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1064f-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1064f-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1064f-154">OUTPUTS</span></span>

### <span data-ttu-id="1064f-155">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1064f-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1064f-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1064f-156">NOTES</span></span>

## <span data-ttu-id="1064f-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1064f-157">RELATED LINKS</span></span>

[<span data-ttu-id="1064f-158">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1064f-158">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)
