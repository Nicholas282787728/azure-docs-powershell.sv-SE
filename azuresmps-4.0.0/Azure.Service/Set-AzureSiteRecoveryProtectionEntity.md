---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099653"
---
# <span data-ttu-id="3e721-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e721-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="3e721-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e721-102">SYNOPSIS</span></span>
<span data-ttu-id="3e721-103">Anger tillståndet för en entitet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="3e721-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="3e721-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e721-104">SYNTAX</span></span>

### <span data-ttu-id="3e721-105">ByPEObject (standard)</span><span class="sxs-lookup"><span data-stu-id="3e721-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e721-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="3e721-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e721-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e721-107">DESCRIPTION</span></span>
<span data-ttu-id="3e721-108">Cmdleten **set-AzureSiteRecoveryProtectionEntity** aktiverar eller inaktiverar skydd för en Azure Site Recovery-enhet.</span><span class="sxs-lookup"><span data-stu-id="3e721-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="3e721-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e721-109">EXAMPLES</span></span>

### <span data-ttu-id="3e721-110">Exempel 1: Aktivera skydd för objekt i en behållare</span><span class="sxs-lookup"><span data-stu-id="3e721-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="3e721-111">Det första kommandot får behållare för det aktuella Azure Site-valvet med cmdleten **Get-AzureSiteRecoveryProtectionContainer** och lagrar det sedan i $ProtectionContainer variabel.</span><span class="sxs-lookup"><span data-stu-id="3e721-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="3e721-112">Det andra kommandot hämtar de skyddade virtuella datorerna som tillhör behållaren som lagras i $ProtectionContainer genom att använda cmdleten **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="3e721-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="3e721-113">Kommandot lagrar resultaten i variabeln $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="3e721-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="3e721-114">Med kommandot slut aktiverar du skydd för de enheter som lagras i $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="3e721-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="3e721-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e721-115">PARAMETERS</span></span>

### <span data-ttu-id="3e721-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3e721-116">-Force</span></span>
<span data-ttu-id="3e721-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3e721-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e721-118">-ID</span><span class="sxs-lookup"><span data-stu-id="3e721-118">-Id</span></span>
<span data-ttu-id="3e721-119">Anger ID för en skyddad virtuell dator som du vill aktivera eller inaktivera skydd för.</span><span class="sxs-lookup"><span data-stu-id="3e721-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-120">-OS</span><span class="sxs-lookup"><span data-stu-id="3e721-120">-OS</span></span>
<span data-ttu-id="3e721-121">Anger typen av operativ system.</span><span class="sxs-lookup"><span data-stu-id="3e721-121">Specifies the operating system type.</span></span>
<span data-ttu-id="3e721-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3e721-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e721-123">Windows</span><span class="sxs-lookup"><span data-stu-id="3e721-123">Windows</span></span>
- <span data-ttu-id="3e721-124">Linux</span><span class="sxs-lookup"><span data-stu-id="3e721-124">Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="3e721-125">-OSDiskName</span></span>
<span data-ttu-id="3e721-126">Anger namnet på den disk som innehåller operativ systemet.</span><span class="sxs-lookup"><span data-stu-id="3e721-126">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="3e721-127">-Profile</span></span>
<span data-ttu-id="3e721-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3e721-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e721-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3e721-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-130">-Skydd</span><span class="sxs-lookup"><span data-stu-id="3e721-130">-Protection</span></span>
<span data-ttu-id="3e721-131">Anger om skydd ska aktive ras eller inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="3e721-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="3e721-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3e721-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e721-133">Aktivering</span><span class="sxs-lookup"><span data-stu-id="3e721-133">Enable</span></span>
- <span data-ttu-id="3e721-134">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="3e721-134">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="3e721-135">-ProtectionContainerId</span></span>
<span data-ttu-id="3e721-136">Anger ID för en skyddad behållare.</span><span class="sxs-lookup"><span data-stu-id="3e721-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="3e721-137">Med den här cmdleten aktive ras eller inaktive ras skyddet för en virtuell dator som tillhör den behållare som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3e721-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e721-138">-ProtectionEntity</span></span>
<span data-ttu-id="3e721-139">Anger objektet skydd.</span><span class="sxs-lookup"><span data-stu-id="3e721-139">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="3e721-140">-ProtectionProfile</span></span>
<span data-ttu-id="3e721-141">Anger en skydds profil för att aktivera skydd.</span><span class="sxs-lookup"><span data-stu-id="3e721-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="3e721-142">Ange ett **ASRProtectionProfile** -objekt som är en av de tillgängliga skydds profilerna i den associerade skydds behållaren.</span><span class="sxs-lookup"><span data-stu-id="3e721-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3e721-143">-WaitForCompletion</span></span>
<span data-ttu-id="3e721-144">Anger att cmdleten väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="3e721-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="3e721-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e721-145">-Confirm</span></span>
<span data-ttu-id="3e721-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e721-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e721-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e721-147">-WhatIf</span></span>
<span data-ttu-id="3e721-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e721-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e721-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e721-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e721-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e721-150">CommonParameters</span></span>
<span data-ttu-id="3e721-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e721-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e721-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e721-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e721-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e721-153">INPUTS</span></span>

## <span data-ttu-id="3e721-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e721-154">OUTPUTS</span></span>

## <span data-ttu-id="3e721-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e721-155">NOTES</span></span>

## <span data-ttu-id="3e721-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e721-156">RELATED LINKS</span></span>

[<span data-ttu-id="3e721-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3e721-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="3e721-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e721-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="3e721-159">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="3e721-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


