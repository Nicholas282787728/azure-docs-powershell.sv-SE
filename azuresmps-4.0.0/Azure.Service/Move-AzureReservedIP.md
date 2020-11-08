---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099472"
---
# <span data-ttu-id="f0c7f-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="f0c7f-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="f0c7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c7f-103">Migrerar en reserverad IP-adress till Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f0c7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0c7f-104">SYNTAX</span></span>

### <span data-ttu-id="f0c7f-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c7f-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0c7f-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c7f-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0c7f-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c7f-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0c7f-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0c7f-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c7f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0c7f-109">DESCRIPTION</span></span>
<span data-ttu-id="f0c7f-110">Cmdleten **Move-AzureReservedIP** migrerar en reserverad IP-adress till en resurs grupp i Azure Resource Manager-stacken.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="f0c7f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0c7f-111">EXAMPLES</span></span>

### <span data-ttu-id="f0c7f-112">9.1</span><span class="sxs-lookup"><span data-stu-id="f0c7f-112">1:</span></span>
```

```

## <span data-ttu-id="f0c7f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0c7f-113">PARAMETERS</span></span>

### <span data-ttu-id="f0c7f-114">-Avbryt</span><span class="sxs-lookup"><span data-stu-id="f0c7f-114">-Abort</span></span>
<span data-ttu-id="f0c7f-115">Anger att denna cmdlet avbryter den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="f0c7f-116">-Commit</span></span>
<span data-ttu-id="f0c7f-117">Anger att den här cmdleten startar den reserverade IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f0c7f-118">-InformationAction</span></span>
<span data-ttu-id="f0c7f-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f0c7f-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f0c7f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0c7f-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="f0c7f-121">Continue</span></span>
- <span data-ttu-id="f0c7f-122">Över</span><span class="sxs-lookup"><span data-stu-id="f0c7f-122">Ignore</span></span>
- <span data-ttu-id="f0c7f-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="f0c7f-123">Inquire</span></span>
- <span data-ttu-id="f0c7f-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f0c7f-124">SilentlyContinue</span></span>
- <span data-ttu-id="f0c7f-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="f0c7f-125">Stop</span></span>
- <span data-ttu-id="f0c7f-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="f0c7f-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f0c7f-127">-InformationVariable</span></span>
<span data-ttu-id="f0c7f-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-129">-Förbered</span><span class="sxs-lookup"><span data-stu-id="f0c7f-129">-Prepare</span></span>
<span data-ttu-id="f0c7f-130">Anger att denna cmdlet förbereder den reserverade IP-adressen för migrering.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="f0c7f-131">-Profile</span></span>
<span data-ttu-id="f0c7f-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0c7f-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0c7f-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="f0c7f-134">-ReservedIPName</span></span>
<span data-ttu-id="f0c7f-135">Anger namnet på den reserverade IP-adressen som den här cmdleten migrerar.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="f0c7f-136">-Validera</span><span class="sxs-lookup"><span data-stu-id="f0c7f-136">-Validate</span></span>
<span data-ttu-id="f0c7f-137">Anger att denna cmdlet verifierar den reserverade IP-adressen för migrering.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c7f-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0c7f-138">-Confirm</span></span>
<span data-ttu-id="f0c7f-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c7f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c7f-140">-WhatIf</span></span>
<span data-ttu-id="f0c7f-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c7f-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c7f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c7f-143">CommonParameters</span></span>
<span data-ttu-id="f0c7f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c7f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c7f-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c7f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c7f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0c7f-146">INPUTS</span></span>

## <span data-ttu-id="f0c7f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0c7f-147">OUTPUTS</span></span>

## <span data-ttu-id="f0c7f-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0c7f-148">NOTES</span></span>

## <span data-ttu-id="f0c7f-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0c7f-149">RELATED LINKS</span></span>

[<span data-ttu-id="f0c7f-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f0c7f-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="f0c7f-151">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="f0c7f-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="f0c7f-152">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="f0c7f-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="f0c7f-153">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f0c7f-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="f0c7f-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f0c7f-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


